# Quand Arrêter un Projet IA

> Savoir dire stop : le signe d'un bon manager.

## Pourquoi C'est Difficile

Arrêter un projet IA est émotionnellement et politiquement difficile :
- Investissement déjà conséquent (temps, argent, énergie)
- Peur d'admettre l'échec
- Pression de la hiérarchie ("on a dit qu'on ferait de l'IA")
- Espoir que "ça va s'améliorer"

Mais continuer un projet voué à l'échec coûte plus cher que l'arrêter.

---

## Les 5 Signaux d'Alarme

### Signal 1 : Performance Technique Insuffisante

**Symptômes :**
- Score < 60% sur tests basiques
- Temps de réponse inacceptable (> 10s)
- Taux d'erreur critique élevé
- Hallucinations fréquentes

**Seuil critique :**
Après 2-3 itérations d'amélioration, toujours < 70% de précision.

**Action recommandée :**
- **Si POC :** Retour en R&D ou abandon
- **Si déjà en pilote :** Retour en POC ou abandon
- **Délai :** 1-2 mois max pour améliorer

**Questions à poser :**
- "Le problème est-il fondamentalement solvable par l'IA ?"
- "Avons-nous les bonnes données ?"
- "L'équipe a-t-elle les compétences ?"

---

### Signal 2 : Adoption Utilisateur Trop Faible

**Symptômes :**
- Taux d'adoption < 30%
- Satisfaction < 3/5
- Utilisateurs contournent l'IA
- Plaintes récurrentes

**Seuil critique :**
Après 1 mois de corrections, toujours < 40% d'adoption.

**Action recommandée :**
- Investiguer les causes (UX ? Confiance ? Utilité ?)
- Former les utilisateurs
- Simplifier l'interface
- **Si toujours < 30% après 2 mois → Abandonnez**

**Questions à poser :**
- "Les utilisateurs comprennent-ils la valeur ?"
- "L'IA résout-elle un vrai problème pour eux ?"
- "Y a-t-il des résistances au changement ?"

---

### Signal 3 : ROI Durablement Négatif

**Symptômes :**
- Coûts > bénéfices après 6 mois
- Payback > 24 mois
- Pas d'amélioration de KPIs business

**Seuil critique :**
ROI négatif après 6 mois d'optimisation.

**Action recommandée :**
- Réduire les coûts (API moins chère, optimiser infra)
- Augmenter le volume (plus d'utilisateurs)
- Élargir le périmètre (plus de cas d'usage)
- **Si ROI toujours < -20% après 6 mois → Abandonnez**

**Questions à poser :**
- "Peut-on réduire significativement les coûts ?"
- "Le marché/contexte a-t-il changé ?"
- "L'IA était-elle vraiment la bonne solution ?"

---

### Signal 4 : Coûts de Maintenance Explosifs

**Symptômes :**
- Ré-entraînement trop fréquent (> 1×/mois)
- Bugs constants en production
- Équipe passant plus de temps à maintenir qu'à développer
- Infrastructure coûteuse et instable

**Seuil critique :**
Coût maintenance > 50% du budget annuel projet.

**Action recommandée :**
- Simplifier l'architecture
- Automatiser le monitoring et ré-entraînement
- **Si impossible à stabiliser → Abandonnez**

**Questions à poser :**
- "Le modèle est-il trop complexe pour notre organisation ?"
- "Avons-nous les compétences pour maintenir ?"
- "Une solution plus simple ferait-elle l'affaire ?"

---

### Signal 5 : Risques Éthiques/Légaux Inacceptables

**Symptômes :**
- Biais discriminatoires détectés
- Non-conformité RGPD
- Décisions inexplicables sur cas sensibles
- Incidents de sécurité ou de confidentialité

**Seuil critique :**
Un seul incident grave ou risque avéré de non-conformité.

**Action recommandée :**
- **Stop immédiat** si risque légal/éthique majeur
- Audit complet avant reprise
- Consultation juridique obligatoire

**Questions à poser :**
- "Pouvons-nous corriger le biais ?"
- "Sommes-nous conformes aux réglementations ?"
- "Le risque réputationnel est-il acceptable ?"

---

## Matrice de Décision

| Signal | Gravité | Délai Action | Action Recommandée |
|--------|---------|--------------|-------------------|
| Performance < 60% | CRITIQUE | 1-2 mois | Retour R&D ou STOP |
| Adoption < 30% | HAUTE | 2 mois | Fix UX ou STOP |
| ROI < 0% après 6 mois | HAUTE | 3-6 mois | Optimiser ou STOP |
| Maintenance > 50% budget | MOYENNE | 3 mois | Simplifier ou STOP |
| Risque éthique/légal | CRITIQUE | IMMÉDIAT | STOP et audit |

---

## Comment Arrêter Proprement

### 1. Documenter les Apprentissages

**À capturer :**
- Ce qui a fonctionné
- Ce qui n'a pas fonctionné
- Hypothèses invalidées
- Recommandations pour l'avenir

**Template :**
```markdown
# Post-Mortem Projet IA [Nom]

## Contexte
- Objectif initial
- Durée du projet
- Investissement total

## Ce qui a fonctionné
-

## Ce qui n'a pas fonctionné
-

## Raisons de l'arrêt
-

## Leçons apprises
-

## Recommandations
-
```

### 2. Communiquer avec les Parties Prenantes

**Messages clés :**
- Décision factuelle, pas émotionnelle
- Coût de continuer > coût d'arrêter
- Apprentissages capitalisés
- Redirection des ressources vers projets à impact

**Évitez :**
- Blâmer l'équipe
- Cacher les vrais chiffres
- Minimiser l'investissement perdu

### 3. Préserver les Actifs

**À conserver :**
- Données nettoyées et annotées
- Documentation technique
- Code réutilisable
- Connaissances de l'équipe

**À archiver proprement :**
- Modèles entraînés
- Configurations
- Historique des expérimentations

### 4. Redéployer les Ressources

**Équipe :**
- Vers d'autres projets IA plus prometteurs
- Vers des projets où ils peuvent apporter leur expertise

**Budget restant :**
- Vers des quick wins plus certains
- Vers de la formation
- Vers de l'infrastructure data

---

## Alternatives à l'Arrêt Total

### Pivot du Périmètre
Réduire l'ambition pour avoir un cas d'usage viable.

**Exemple :**
Au lieu d'un chatbot généraliste → chatbot FAQ sur 10 questions top.

### Mise en Pause
Attendre que les conditions soient meilleures (plus de données, meilleure techno).

**Critères de reprise :**
- Nouvelles données disponibles
- Budget supplémentaire alloué
- Technologie plus mature

### Externalisation
Confier à un prestataire spécialisé si on manque de compétences internes.

**Attention :** Ne résout pas les problèmes de données ou d'adoption.

---

## Cas Réels d'Arrêt (Anonymisés)

### Cas 1 : Chatbot RH - Arrêt après 4 mois

**Contexte :** Chatbot pour répondre aux questions RH des employés.

**Raisons de l'arrêt :**
- Précision 55% (trop de réponses incorrectes sur politique RH)
- Risque juridique si mauvais conseil
- Coût API supérieur au temps économisé

**Leçons :**
- Les sujets sensibles (RH, légal, médical) nécessitent précision > 95%
- Mieux vaut une FAQ statique qu'un chatbot qui se trompe

---

### Cas 2 : Prédiction Stock - Pivot après 8 mois

**Contexte :** Prédire les ruptures de stock.

**Problème initial :**
- ROI négatif (coûts infra + équipe > économies)
- Complexité des patterns saisonniers

**Pivot :**
- Réduit au top 20 produits les plus vendus
- ROI positif sur ce périmètre réduit

**Leçons :**
- Commencer petit, prouver la valeur, puis étendre
- 80% de la valeur sur 20% du périmètre

---

### Cas 3 : Analyse Sentiment - Arrêt définitif

**Contexte :** Analyser le sentiment des avis clients.

**Raisons de l'arrêt :**
- Performance comparable à des règles simples (mots-clés)
- Pas de valeur ajoutée vs solution basique
- Équipe surdimensionnée pour le problème

**Leçons :**
- Toujours comparer avec une baseline simple
- L'IA n'est pas toujours la meilleure solution

---

## Check-List avant d'Arrêter

- [ ] Performance mesurée objectivement (chiffres, pas impressions)
- [ ] Plusieurs tentatives d'amélioration faites
- [ ] Causes racines identifiées
- [ ] Alternatives évaluées (pivot, pause, externalisation)
- [ ] Coût de continuation vs arrêt calculé
- [ ] Parties prenantes consultées
- [ ] Apprentissages documentés
- [ ] Plan de transition défini
- [ ] Communication préparée

---

## Le Mot de la Fin

Arrêter un projet n'est pas un échec si :
- Vous l'arrêtez pour les bonnes raisons (data-driven)
- Vous capitalisez sur les apprentissages
- Vous redirigez les ressources efficacement
- Vous appliquez les leçons aux projets suivants

**Un bon manager sait dire non. Un excellent manager sait dire stop.**

---

## Ressources

- [Framework 3 niveaux](framework-3-niveaux.md) - Critères objectifs d'évaluation
- [Budget et ROI](../pilotage/budget-et-roi.md) - Calculer le vrai coût
- [Risques et éthique](../pilotage/risques-et-ethique.md) - Identifier les risques

---

*Savoir arrêter un projet | Dernière MAJ : Nov 2025*
