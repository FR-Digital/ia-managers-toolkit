# Framework d'Évaluation IA en 3 Niveaux

> **Évaluer une IA, ce n'est pas juste vérifier si "ça marche".**

## Le Principe

Évaluer une IA, c'est répondre à **3 questions dans l'ordre** :

1. **Niveau 1 : Est-ce que ça marche ?** (Tests techniques basiques)
2. **Niveau 2 : Est-ce que les utilisateurs l'utilisent ?** (Engagement)
3. **Niveau 3 : Est-ce que ça a un impact business ?** (ROI)

**IMPORTANT :** Ne passez au niveau suivant que si le niveau précédent est validé.

---

## Niveau 1 : Est-ce que Ça Marche ? 🔧

### Objectif

Vérifier que l'IA fait ce qu'on lui demande techniquement.

### Questions Clés

- L'IA répond-elle aux requêtes ?
- Les réponses sont-elles correctes ?
- Le temps de réponse est-il acceptable ?

### Comment Tester : Méthode des 100 Cas

**Étape 1 : Préparez 100 questions types** (avec réponses attendues)

- 70 cas "normaux" (questions courantes)
- 20 cas "limites" (questions difficiles)
- 10 cas "pièges" (hors périmètre)

**Étape 2 : Posez-les à l'IA**

**Étape 3 : Notez chaque réponse**

| Note | Signification | Points |
|------|---------------|--------|
| ✅ **Correcte** | Bonne réponse | 1 point |
| ⚠️ **Partielle** | Réponse incomplète mais utile | 0.5 point |
| ❌ **Fausse** | Erreur ou hallucination | 0 point |
| 🚫 **Hors sujet** | Ne comprend pas la question | 0 point |

**Étape 4 : Calculez le score**

| Score | Interprétation | Action |
|-------|----------------|--------|
| **> 80%** | ✅ Niveau 1 validé | Passez au Niveau 2 |
| **60-80%** | ⚠️ Améliorations nécessaires | Corrigez avant de continuer |
| **< 60%** | ❌ Échec | Retour en développement |

### Exemple : Chatbot SAV

**Cas normal :**
```
Q: "Quel est votre délai de livraison ?"
R attendue: "3-5 jours ouvrés en France métropolitaine"
R IA: "Nos livraisons prennent généralement 3 à 5 jours ouvrés"
Note: ✅ 1 point
```

**Cas limite :**
```
Q: "Je n'ai pas reçu ma commande de mardi dernier"
R attendue: Demander numéro commande + proposer suivi
R IA: "Je vais avoir besoin de votre numéro de commande pour vérifier le statut"
Note: ✅ 1 point
```

**Cas piège :**
```
Q: "Quel est le meilleur concurrent ?"
R attendue: Refuser poliment (hors périmètre)
R IA: "Je ne peux vous renseigner que sur nos produits et services"
Note: ✅ 1 point
```

### Métriques Techniques à Demander

Vous n'avez pas à calculer ça vous-même, mais demandez ces chiffres à votre équipe :

| Métrique | Seuil Minimum | Idéal | Ce que ça mesure |
|----------|---------------|-------|------------------|
| **Précision** | > 70% | > 90% | % de réponses correctes |
| **Temps réponse** | < 5 sec | < 2 sec | Rapidité du système |
| **Taux d'erreur** | < 10% | < 5% | % de bugs/plantages |
| **Disponibilité** | > 95% | > 99% | % du temps accessible |

### Checklist Niveau 1

- [ ] 100 cas de test préparés (70 normaux, 20 limites, 10 pièges)
- [ ] Tests exécutés et documentés
- [ ] Score global > 80%
- [ ] Pas d'erreurs critiques (hallucinations graves, données fausses)
- [ ] Temps réponse acceptable (< 5 sec)
- [ ] L'IA refuse poliment les questions hors périmètre
- [ ] Métriques techniques demandées et dans les seuils

**Si tout est ✅ → Passez au Niveau 2**

---

## Niveau 2 : Est-ce que les Utilisateurs l'Utilisent ? 👥

### Objectif

Vérifier que l'IA est utilisable et utile pour les vrais utilisateurs.

### Questions Clés

- Les utilisateurs adoptent-ils l'IA ?
- Sont-ils satisfaits ?
- Préfèrent-ils l'IA à l'ancienne méthode ?

### Comment Tester : Beta Test (2-4 Semaines)

**Étape 1 : Sélectionnez 20-50 utilisateurs pilotes**

- Mix de profils (novices + experts)
- Volontaires motivés
- Représentatifs de votre cible

**Étape 2 : Laissez-les utiliser l'IA librement**

- Pas de consignes strictes
- En situation réelle de travail
- Pendant 2-4 semaines minimum

**Étape 3 : Collectez les Données**

**Métriques Quantitatives (automatiques) :**

- Nombre d'utilisations par utilisateur/jour
- Temps moyen par session
- Taux d'abandon (% de sessions interrompues)
- Feedback "pouce haut/pouce bas" après chaque réponse

**Métriques Qualitatives (manuelles) :**

- Sondage satisfaction (échelle 1-5)
- Entretiens utilisateurs (5-10 personnes)
- Questions ouvertes : "Qu'avez-vous aimé/détesté ?"

### Critères de Succès Niveau 2

| Métrique | Seuil Minimum | Idéal | Ce que ça mesure |
|----------|---------------|-------|------------------|
| **Taux d'adoption** | > 50% utilisent 1×/semaine | > 80% | L'IA est utilisée |
| **Satisfaction** | > 3.5/5 | > 4/5 | Les gens sont contents |
| **Pouce haut** | > 60% | > 80% | Les réponses sont utiles |
| **Taux d'abandon** | < 30% | < 15% | Les sessions vont au bout |

### Signaux d'Alerte 🚨

**Taux d'adoption < 30%** → Les gens n'utilisent pas l'IA
- Causes possibles : Pas utile, trop compliquée, pas promue, habitudes ancrées

**Satisfaction < 3/5** → Les gens n'aiment pas l'IA
- Causes possibles : Réponses fausses, lente, frustrante, pas intuitive

**Taux abandon > 50%** → Les gens arrêtent en cours d'utilisation
- Causes possibles : Ne trouve pas la réponse, trop de tours de dialogue, bugs

### Checklist Niveau 2

- [ ] 20+ utilisateurs en beta test
- [ ] 2+ semaines d'utilisation réelle
- [ ] Taux d'adoption > 50%
- [ ] Satisfaction moyenne > 3.5/5
- [ ] Taux de pouce haut > 60%
- [ ] Feedback qualitatif collecté (entretiens)
- [ ] Principales frustrations identifiées
- [ ] Plan d'amélioration défini

**Si tout est ✅ → Passez au Niveau 3**

---

## Niveau 3 : Est-ce que Ça a un Impact Business ? 💰

### Objectif

Mesurer si l'IA génère de la valeur business mesurable.

### Questions Clés

- L'IA fait-elle gagner du temps/argent ?
- Les KPIs métier s'améliorent-ils ?
- Le ROI est-il positif ?

### Comment Mesurer : A/B Test (1-3 Mois)

**Étape 1 : Divisez les utilisateurs en 2 groupes**

- **Groupe A** : Utilise l'IA
- **Groupe B** : Utilise l'ancienne méthode (groupe témoin)

**Étape 2 : Comparez les KPIs après 1-3 mois**

### Exemple : Chatbot SAV

| KPI | Groupe A (avec IA) | Groupe B (sans IA) | Amélioration |
|-----|-------------------|-------------------|--------------|
| Temps réponse moyen | 4h | 24h | **-83%** ✅ |
| Satisfaction client | 82% | 68% | **+14 pts** ✅ |
| Volume traité/agent | 150/jour | 50/jour | **+200%** ✅ |
| Taux résolution 1er contact | 75% | 60% | **+15 pts** ✅ |

**Étape 3 : Calculez le ROI**

**Formule Simple :**

```
ROI = (Gains annuels - Coûts annuels) / Coûts annuels × 100
```

**Exemple Concret :**

**Gains annuels :** 180k€
- 2.5 ETP économisés × 72k€/an = 180k€

**Coûts annuels :** 105k€
- POC : 30k€
- Licence IA : 25k€
- Infrastructure : 20k€
- Maintenance : 30k€

**Calcul :**
```
ROI = (180k€ - 105k€) / 105k€ × 100 = 71%
```

**Interprétation :** Pour chaque euro investi, vous récupérez 1,71€. Projet rentable !

### Critères de Succès Niveau 3

| Critère | Minimum | Idéal | Ce que ça signifie |
|---------|---------|-------|---------------------|
| **ROI** | > 0% (rentable) | > 100% | L'IA rapporte plus qu'elle coûte |
| **Payback** | < 18 mois | < 12 mois | Temps pour récupérer l'investissement |
| **KPI métier** | +10% vs baseline | +30% | Amélioration mesurable |

### Checklist Niveau 3

- [ ] KPIs métier définis AVANT lancement
- [ ] Groupe témoin pour comparaison (si possible)
- [ ] Mesure sur 1-3 mois minimum
- [ ] ROI calculé et positif
- [ ] Payback < 18 mois
- [ ] Impact business documenté
- [ ] Rapport présenté à la direction

**Si tout est ✅ → Déploiement Production OK**

---

## Quand Arrêter un Projet

### 🔴 Arrêtez si Niveau 1 Échoue

**Signal :** Score < 60% sur tests basiques

**Raison :** L'IA ne fonctionne pas techniquement. Pas la peine de continuer.

**Action :** Retour en développement ou abandon du projet.

---

### 🟡 Améliorez si Niveau 2 Échoue

**Signal :** Adoption < 30% ou Satisfaction < 3/5

**Raison :** L'IA marche techniquement mais n'est pas utilisable.

**Actions possibles :**
- Simplifier l'interface
- Former les utilisateurs
- Améliorer les prompts/réponses
- Revoir le périmètre fonctionnel

**Donnez-vous :** 1-2 mois pour corriger. Si toujours < 30%, abandonnez.

---

### 🟢 Optimisez si Niveau 3 Décevant

**Signal :** ROI < 0% ou KPIs stagnent

**Raison :** L'IA est utilisée mais ne génère pas assez de valeur.

**Actions possibles :**
- Réduire coûts (optimiser API, infrastructure)
- Augmenter volume (plus d'utilisateurs)
- Élargir périmètre (plus de cas d'usage)
- Améliorer précision (moins d'escalades humaines)

**Donnez-vous :** 3-6 mois pour optimiser. Si ROI toujours négatif, arrêtez.

---

## Résumé Visuel

```
Niveau 1 : ÇA MARCHE ?
│
├─ OUI (>80%) ─────────────────┐
│                               │
└─ NON (<60%) ──> STOP         │
                                ▼
                       Niveau 2 : C'EST UTILISÉ ?
                       │
                       ├─ OUI (adoption >50%) ──────┐
                       │                             │
                       └─ NON (<30%) ──> AMÉLIORER   │
                                         ou STOP     │
                                                     ▼
                                            Niveau 3 : ÇA RAPPORTE ?
                                            │
                                            ├─ OUI (ROI >0%) ──> PROD ✅
                                            │
                                            └─ NON (ROI <0%) ──> OPTIMISER
                                                                 ou STOP
```

---

## Templates Associés

- **[Grille d'évaluation Niveau 1](../templates/grille-evaluation.md)** - Scoring des 100 cas
- **[Sondage satisfaction Niveau 2](../templates/feedback-utilisateur.md)** - Questionnaire utilisateurs
- **[Rapport qualité](../templates/rapport-qualite.md)** - Documentation des résultats

---

## Pour Aller Plus Loin

- **[Questions à poser à votre équipe technique](../guides/questions-equipe-technique.md)** - 30 questions business-friendly
- **[Critères go/no-go production](../guides/criteres-go-production.md)** - Matrice de décision
- **[Exemple complet : Chatbot SAV](../examples/evaluation-chatbot.md)** - Les 3 niveaux en pratique

---

*Dernière MAJ : Novembre 2025 | Inspiré par [CGD Framework](https://www.cgdev.org/blog/ai-evaluation-framework-for-the-development-sector)*
