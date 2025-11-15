# Exemple d'Échec : Évaluation Analyse de Sentiment

> **Un cas instructif où le projet a été arrêté au Niveau 2**

## Contexte

**Entreprise :** Banque retail (anonymisée)
**Projet :** IA d'analyse de sentiment sur emails clients
**Objectif :** Prioriser les emails urgents (clients mécontents) automatiquement
**Budget :** 90k€ sur 12 mois
**Équipe :** 3 analystes service client + 1 manager

---

## Ce Qu'on Voulait Faire

**Problème initial :**
- 500 emails/jour reçus au service client
- Pas de priorisation : traitement FIFO (premier arrivé, premier servi)
- Clients très mécontents traités tardivement
- Risque de churn sur clients à fort potentiel

**Solution proposée :**
- IA analyse le sentiment de chaque email (positif/neutre/négatif/urgent)
- Priorisation automatique : urgents d'abord
- Réduction du temps de traitement clients critiques

**ROI espéré :**
- -50% de churn sur clients mécontents non traités à temps
- Gain estimé : 200k€/an

---

## Niveau 1 : Est-ce que Ça Marche ? ✅

### Résultats des Tests

**Méthodologie :**
- 200 emails historiques annotés manuellement
- 3 niveaux : Négatif/Neutre/Positif
- Sous-catégorie pour "Urgent" (besoin d'escalade immédiate)

**Scores obtenus :**

| Catégorie | Précision | Rappel | F1-Score |
|-----------|-----------|--------|----------|
| Négatif | 85% | 82% | 83% |
| Neutre | 78% | 80% | 79% |
| Positif | 88% | 85% | 86% |
| **Global** | **83%** | **82%** | **82%** |

| Détection "Urgent" | Résultat |
|-------------------|----------|
| Vrais positifs | 78% |
| Faux positifs | 12% |
| Faux négatifs | 22% |

**Décision :** VALIDÉ ✅ (Score global 82% > 80%)

**Réserves notées :**
- 22% de faux négatifs sur "urgent" = risque de rater des clients vraiment en détresse
- Mais considéré acceptable pour un POC

---

## Niveau 2 : Est-ce que les Utilisateurs l'Utilisent ? ❌

### Setup du Test

**Période :** 4 semaines
**Participants :** 3 analystes + 1 manager
**Usage :** L'IA priorise, l'humain valide et traite

### Semaine 1 : Enthousiasme Initial

**Métriques :**
- Adoption : 100% (tous utilisent)
- Satisfaction : 4.2/5
- Emails traités : +15% vs baseline

**Commentaires :**
- "Super, je vois tout de suite les urgences"
- "Enfin un outil intelligent"
- "J'aurais dû avoir ça avant"

**Status :** 🟢 Très prometteur

### Semaine 2 : Premiers Doutes

**Métriques :**
- Adoption : 100%
- Satisfaction : 3.6/5 (-0.6)
- Emails traités : +8% vs baseline

**Problèmes remontés :**

1. **Faux positifs frustrants**
   - Email client "Je suis absolument ravi !" classé "négatif" (ironie non détectée)
   - Client qui dit "Je vais résilier... si vous ne me proposez pas mieux" classé "urgent" (négociation, pas urgence)

2. **Contexte manquant**
   - L'IA ne connaît pas l'historique client
   - Un email "normal" d'un client à fort enjeu traité en basse priorité

**Commentaire analyste :**
> "Je passe plus de temps à corriger l'IA qu'à traiter les emails"

**Status :** 🟡 Points d'attention

### Semaine 3 : Décrochage

**Métriques :**
- Adoption : 67% (1 analyste sur 3 n'utilise plus)
- Satisfaction : 2.9/5 (-0.7)
- Emails traités : -5% vs baseline (PIRE qu'avant !)

**Incident critique :**

Un client VIP (500k€ de CA annuel) envoie un email poli mais ferme :
```
"Bonjour, Je souhaite être rappelé concernant mon compte. Merci."
```

- L'IA classe : "Neutre" → Basse priorité
- Réalité : Client sur le point de partir chez le concurrent
- Traité 48h plus tard (au lieu de 4h normalement pour VIP)
- Client mécontent, menace de résilier

**Réaction du manager :**
> "On ne peut pas se permettre ce genre d'erreur. Un VIP doit être traité immédiatement, peu importe le ton de l'email."

**Status :** 🔴 Problème majeur

### Semaine 4 : Abandon

**Métriques :**
- Adoption : 33% (1 seul analyste utilise encore)
- Satisfaction : 2.1/5
- Emails traités : Retour au processus manuel

**Feedback final :**

**Analyste 1 (n'utilise plus) :**
> "L'IA est bonne pour les cas évidents, mais les emails évidents, je les repère en 2 secondes moi-même. C'est sur les cas ambigus qu'elle se plante, exactement là où j'avais besoin d'aide."

**Analyste 2 (n'utilise plus) :**
> "Je ne fais plus confiance. Chaque email marqué 'neutre' par l'IA, je le vérifie quand même. Double travail."

**Analyste 3 (utilise encore) :**
> "C'est utile pour le premier tri, mais je re-trie derrière. Gain marginal."

**Manager :**
> "L'outil n'apporte pas assez de valeur par rapport au risque de rater un client important. On revient à l'ancien système."

---

## Décision : ARRÊT DU PROJET

### Bilan Niveau 2

| Métrique | Semaine 1 | Semaine 4 | Cible | Status |
|----------|-----------|-----------|-------|--------|
| Adoption | 100% | 33% | > 50% | ❌ |
| Satisfaction | 4.2/5 | 2.1/5 | > 3.5 | ❌ |
| Productivité | +15% | -5% | > 0% | ❌ |

**Verdict :** Le projet échoue au Niveau 2. Pas de passage au Niveau 3.

---

## Pourquoi Ça a Échoué

### Raison #1 : Problème Mal Défini

**Ce qu'on pensait :**
"Il faut détecter les emails négatifs pour les traiter en priorité."

**La réalité :**
"Il faut identifier les clients à risque, ce qui ne se limite pas au sentiment de l'email."

**Leçon :**
Le sentiment d'un email ≠ la priorité business. Un client VIP qui écrit poliment peut être plus urgent qu'un client lambda en colère.

### Raison #2 : Faux Négatifs Coûteux

**Le calcul :**
- 22% de faux négatifs sur "urgent"
- Sur 500 emails/jour, environ 50 sont "urgents"
- 22% de 50 = 11 emails urgents ratés/jour
- Si 1 sur 11 est un VIP... risque inacceptable

**Leçon :**
Dans certains contextes, le coût d'une erreur est trop élevé. 82% de précision semble bon, mais 22% de faux négatifs sur les cas critiques est catastrophique.

### Raison #3 : Manque de Contexte

**Ce que l'IA voit :**
Le texte de l'email, isolé.

**Ce que l'humain sait :**
- Historique du client
- Valeur du client (CA)
- Interactions récentes
- Contrats en cours

**Leçon :**
L'IA sans contexte business est aveugle. Le sentiment n'est qu'une donnée parmi d'autres.

### Raison #4 : Confiance Perdue

**Cycle vicieux :**
1. L'IA fait une erreur visible
2. L'utilisateur perd confiance
3. L'utilisateur vérifie systématiquement
4. Le gain de temps disparaît
5. L'utilisateur abandonne

**Leçon :**
Une IA en support décisionnel doit être presque parfaite sur les cas critiques. Une seule erreur grave détruit la confiance.

---

## Ce Qu'on Aurait Dû Faire

### 1. Mieux Définir le Problème

**Au lieu de :**
"Détecter le sentiment pour prioriser"

**Faire :**
"Identifier les emails nécessitant une action urgente basée sur :
- Sentiment
- Valeur client
- Historique
- Mots-clés critiques (résilier, avocat, concurrent...)
- Contexte contractuel"

### 2. Intégrer les Données Business

**Minimum viable :**
- Croiser avec CRM (valeur client, historique)
- Détecter mots-clés métier (pas juste sentiment)
- Avoir des règles métier (VIP = toujours prioritaire)

### 3. Repenser le Use Case

**Alternatives plus réalistes :**

**Option A : Aide à la rédaction**
- L'IA suggère des réponses, pas des priorités
- L'humain garde le contrôle total
- Moins de risque

**Option B : Pré-catégorisation (pas priorisation)**
- L'IA suggère : "Facturation", "Réclamation", "Information"
- L'humain décide de la priorité
- Valeur ajoutée sans risque

**Option C : Alerte uniquement (pas de tri)**
- L'IA alerte sur mots-clés critiques : "résilier", "avocat"
- Pas de remplacement du jugement humain
- Filet de sécurité, pas décisionnaire

### 4. Être Honnête sur les Limites

**Communiquer clairement :**
"Cette IA détecte le sentiment, mais ne remplace pas votre jugement sur la priorité business. Elle peut rater des urgences."

---

## Coûts de l'Échec

### Financier

| Poste | Montant |
|-------|---------|
| Développement POC | 45k€ |
| Licence IA (3 mois) | 8k€ |
| Temps équipe (tests) | 12k€ |
| **TOTAL PERDU** | **65k€** |

Budget restant non dépensé : 25k€ (heureusement arrêté tôt)

### Immatériel

- **Confiance** : L'équipe est maintenant sceptique sur l'IA
- **Temps** : 4 mois de travail sans résultat
- **Moral** : Frustration des analystes
- **Réputation interne** : Projet "raté"

---

## Bonne Nouvelle : Ce N'est Pas un Échec Total

### Apprentissages Précieux

1. **L'IA n'est pas magique** - Elle a besoin de contexte
2. **Le sentiment seul ne suffit pas** - La priorité est multifactorielle
3. **Tester tôt, échouer vite** - Arrêter au Niveau 2 a évité 25k€ de pertes supplémentaires
4. **Écouter les utilisateurs** - Ils ont vu les limites immédiatement

### Projet Pivot Réussi

6 mois plus tard, l'équipe a lancé un projet différent :

**Nouveau projet :** Chatbot FAQ interne pour les analystes
- Recherche rapide dans la base de connaissances
- L'IA aide à trouver les procédures, pas à prioriser
- Risque faible (pas de décision client)

**Résultat :**
- Adoption 85%
- Satisfaction 4.3/5
- ROI +120%

**Leçon finale :**
Un échec bien analysé mène à un succès futur.

---

## Checklist : Éviter Ce Type d'Échec

Avant de lancer un projet IA similaire, vérifiez :

- [ ] Le problème est-il bien défini (pas juste technique) ?
- [ ] L'IA a-t-elle accès au contexte nécessaire ?
- [ ] Le coût d'une erreur est-il acceptable ?
- [ ] Les utilisateurs font-ils confiance au système ?
- [ ] Y a-t-il un plan B si l'IA se trompe ?
- [ ] Le use case est-il réaliste vs les capacités de l'IA ?

Si vous répondez NON à l'une de ces questions, reconsidérez le projet.

---

## Conclusion

**L'échec n'est pas d'avoir arrêté le projet.**
**L'échec aurait été de continuer malgré les signaux.**

Le framework 3 niveaux a fonctionné parfaitement :
- Niveau 1 validé → Techniquement ça marche
- Niveau 2 échoué → Mais ce n'est pas utilisable
- Niveau 3 non atteint → On n'a pas gaspillé plus d'argent

**Morale :**
Une IA qui "marche" techniquement peut être inutile en pratique. C'est pourquoi le Niveau 2 (tests utilisateurs réels) est crucial avant de parler de ROI.

---

*Cas documenté par LaFabriqAI | Données anonymisées | Novembre 2025*
