# Organiser des Tests Utilisateurs

> **Beta test en 4 étapes simples**

## Pourquoi Tester avec de Vrais Utilisateurs ?

Les tests techniques (Niveau 1) ne suffisent pas. Une IA peut être "correcte" techniquement mais inutilisable en pratique. Les tests utilisateurs révèlent :
- Si l'IA est vraiment utile au quotidien
- Les frustrations non anticipées
- Les vrais besoins vs les besoins supposés

---

## Étape 1 : Recruter les Testeurs (1 semaine)

### Combien de Testeurs ?

| Taille équipe | Nb testeurs | Raison |
|---------------|-------------|--------|
| < 20 personnes | 5-10 | Feedback qualitatif |
| 20-100 personnes | 10-25 | Mix quali + quanti |
| > 100 personnes | 25-50 | Données statistiques fiables |

### Profils à Inclure

**Équilibre essentiel :**
- 50% **Novices** (< 1 an d'expérience)
- 50% **Experts** (> 3 ans d'expérience)

**Diversité importante :**
- Différents départements (si applicable)
- Différents niveaux de comfort avec la technologie
- Différents cas d'usage prévisibles

### Comment Recruter ?

**Email type :**

```
Objet : Participez au test de notre nouvelle IA !

Bonjour,

Nous lançons un nouvel outil IA pour [objectif] et nous avons besoin de votre feedback.

Ce que ça implique :
- Utiliser l'IA pendant 2-4 semaines
- 30 minutes de votre temps pour un sondage final
- Optionnel : 20 min d'entretien

Ce que vous y gagnez :
- Influence sur l'outil final
- Formation prioritaire
- [Autre incitatif si budget]

Intéressé(e) ? Répondez à cet email avant [date].

Merci !
[Votre nom]
```

### Critères de Sélection

✅ **Bon candidat :**
- Volontaire et motivé
- Disponible sur la période
- Représentatif de l'usage cible
- Capable de donner du feedback constructif

❌ **Éviter :**
- Personnes opposées au projet (biais négatif)
- Trop d'enthousiastes technophiles (biais positif)
- Personnes souvent absentes (données incomplètes)

---

## Étape 2 : Préparer le Test (1 semaine)

### Définir les Objectifs

**Questions à répondre :**
1. L'IA est-elle facile à utiliser ?
2. Les réponses sont-elles utiles ?
3. L'IA fait-elle gagner du temps ?
4. Quelles sont les frustrations principales ?
5. Les utilisateurs recommanderaient-ils l'IA ?

### Créer le Protocole

**Document à préparer :**

```markdown
# Protocole de Test IA - [Nom du projet]

## Objectif
Évaluer l'utilisabilité et l'utilité de l'IA dans des conditions réelles.

## Durée
[X] semaines, du [date début] au [date fin]

## Participants
[X] testeurs sélectionnés

## Instructions pour les Testeurs

### Ce que vous devez faire :
1. Utiliser l'IA pour vos tâches quotidiennes
2. Pas d'obligation de l'utiliser systématiquement
3. Utiliser le bouton feedback après chaque interaction
4. Noter les problèmes rencontrés

### Ce que vous NE devez PAS faire :
- Tester des cas extrêmes volontairement (sauf si demandé)
- Partager vos résultats avec d'autres testeurs
- Vous forcer à utiliser l'IA si elle n'est pas pertinente

### Support
Contact : [email/slack]
Problème technique : [contact]
Question sur le test : [contact]

## Collecte de Données
- Automatique : logs d'utilisation, thumbs up/down
- Manuelle : sondage de mi-parcours (semaine 2), sondage final
- Optionnel : entretiens individuels

## Confidentialité
Vos données sont anonymisées. Nous analysons les tendances, pas les individus.
```

### Préparer les Outils

**Checklist :**
- [ ] Accès IA configuré pour chaque testeur
- [ ] Tracking d'utilisation activé (respectant vie privée)
- [ ] Bouton feedback intégré (pouce haut/bas)
- [ ] Canal de communication créé (Slack/Teams/Email)
- [ ] Sondage préparé ([Template Feedback Utilisateur](../templates/feedback-utilisateur.md))
- [ ] Calendrier entretiens bloqué

### Briefing des Testeurs

**Réunion de lancement (30 min) :**

1. **Contexte** (5 min)
   - Pourquoi ce projet ?
   - Où en sommes-nous ?

2. **Objectifs du test** (5 min)
   - Ce qu'on cherche à savoir
   - Comment leur feedback sera utilisé

3. **Instructions pratiques** (10 min)
   - Comment utiliser l'IA
   - Comment donner du feedback
   - Qui contacter si problème

4. **Q&A** (10 min)
   - Répondre aux questions
   - Lever les inquiétudes

**Points importants à communiquer :**
- "Ce n'est pas vous qu'on évalue, c'est l'IA"
- "Il n'y a pas de mauvaise façon d'utiliser"
- "Vos critiques sont précieuses, n'hésitez pas"

---

## Étape 3 : Collecter le Feedback (2-4 semaines)

### Semaine 1 : Observation

**Actions :**
- Vérifier que tout le monde a accès
- Répondre aux questions rapidement
- NE PAS intervenir sur les comportements

**Métriques à surveiller :**
- Taux de connexion (tous ont essayé ?)
- Premiers retours spontanés
- Problèmes techniques

**Check-in rapide (email ou message) :**
```
Bonjour à tous,

Une semaine de test ! Quelques questions rapides :
- Avez-vous pu utiliser l'IA ?
- Des problèmes techniques ?
- Premières impressions ?

Répondez en 2 lignes max. Merci !
```

### Semaine 2 : Mi-parcours

**Sondage court (5 questions max) :**
1. Combien de fois avez-vous utilisé l'IA cette semaine ?
2. L'IA vous a-t-elle été utile ? (1-5)
3. Rencontrez-vous des difficultés ? (oui/non + détail)
4. Continuez-vous à l'utiliser ? (oui/non)
5. Un commentaire ?

**Analyse rapide :**
- Qui n'utilise pas ? Pourquoi ?
- Quelles difficultés récurrentes ?
- Faut-il ajuster quelque chose ?

### Semaine 3-4 : Consolidation

**Laisser l'usage se stabiliser.**

Les comportements de la semaine 1 ne sont pas représentatifs (effet nouveauté).
La semaine 3-4 montre l'usage réel.

**Surveiller :**
- L'usage diminue-t-il ? (signe de déception)
- L'usage augmente-t-il ? (signe d'adoption)
- Les mêmes problèmes reviennent-ils ?

### Fin de Test : Collecte Complète

**Sondage final complet** ([Template](../templates/feedback-utilisateur.md))

**Entretiens individuels (optionnel mais recommandé) :**
- 20-30 minutes par personne
- 5-10 entretiens suffisent
- Mix de satisfaits et insatisfaits

**Questions d'entretien :**
1. "Décrivez une situation où l'IA vous a aidé"
2. "Décrivez une situation où l'IA vous a frustré"
3. "Si vous pouviez changer une chose, ce serait quoi ?"
4. "Recommanderiez-vous l'IA à un collègue ? Pourquoi ?"
5. "Continuerez-vous à l'utiliser après le test ?"

---

## Étape 4 : Analyser et Agir (1 semaine)

### Compiler les Données

**Données quantitatives :**
| Métrique | Résultat | Cible | Status |
|----------|----------|-------|--------|
| Taux adoption | [ ]% | > 50% | |
| Satisfaction moyenne | [ ]/5 | > 3.5 | |
| Thumbs up | [ ]% | > 60% | |
| Taux abandon | [ ]% | < 30% | |

**Données qualitatives :**
- Top 3 des points positifs
- Top 3 des frustrations
- Demandes d'amélioration récurrentes

### Identifier les Patterns

**Questions à se poser :**
- Y a-t-il des différences entre profils ?
  - Novices vs experts
  - Par département
  - Par type d'usage

- Quels problèmes sont récurrents ?
  - Cités par > 30% = prioritaire
  - Cités par < 10% = cas particulier

- L'adoption est-elle homogène ?
  - Certains "power users" vs abandons ?

### Prioriser les Actions

**Matrice Impact/Effort :**

| Action | Impact | Effort | Priorité |
|--------|--------|--------|----------|
| [Action 1] | H/M/L | H/M/L | |
| [Action 2] | H/M/L | H/M/L | |
| [Action 3] | H/M/L | H/M/L | |

**Règle :**
- Impact élevé + Effort faible = Faire immédiatement
- Impact élevé + Effort élevé = Planifier
- Impact faible + Effort faible = Faire si temps
- Impact faible + Effort élevé = Ne pas faire

### Communiquer les Résultats

**Aux testeurs :**
```
Objet : Résultats du test et prochaines étapes

Bonjour,

Merci pour votre participation ! Voici ce qu'on a appris :

✅ Points positifs :
- [Point 1]
- [Point 2]

⚠️ Améliorations prévues :
- [Amélioration 1] - Date : [X]
- [Amélioration 2] - Date : [X]

Prochaines étapes :
[Déploiement / Phase 2 / etc.]

Votre feedback compte. Merci !
```

**Au management :**
- Résumé exécutif (1 page)
- Recommandation claire (GO / NO-GO / GO conditionnel)
- Prochaines étapes avec budget/timeline

---

## Erreurs à Éviter

### ❌ Trop Peu de Testeurs
- Problème : Données non significatives
- Solution : Minimum 10 personnes

### ❌ Durée Trop Courte
- Problème : Effet nouveauté biaise les résultats
- Solution : Minimum 2 semaines, idéalement 3-4

### ❌ Que des Enthousiastes
- Problème : Feedback trop positif, non représentatif
- Solution : Inclure des sceptiques (mais pas des opposants)

### ❌ Ne Pas Écouter le Feedback Négatif
- Problème : Améliorations non faites, déception au déploiement
- Solution : Les critiques sont les plus précieuses

### ❌ Trop Intervenir Pendant le Test
- Problème : Biaiser le comportement naturel
- Solution : Observer, noter, mais ne pas corriger en live

---

## Timeline Récapitulative

| Semaine | Activité | Livrables |
|---------|----------|-----------|
| S-1 | Recrutement | Liste testeurs confirmés |
| S0 | Préparation | Protocole, outils, briefing |
| S1 | Test - Observation | Check-in rapide |
| S2 | Test - Mi-parcours | Mini-sondage |
| S3-4 | Test - Consolidation | Usage stabilisé |
| S5 | Collecte finale | Sondage + entretiens |
| S6 | Analyse | Rapport + recommandations |

**Durée totale : 6-7 semaines**

---

## Ressources

- **[Template Feedback Utilisateur](../templates/feedback-utilisateur.md)** - Sondage complet
- **[Framework 3 Niveaux](../frameworks/3-niveaux-evaluation.md)** - Contexte Niveau 2
- **[Exemple Chatbot](../examples/evaluation-chatbot.md)** - Voir la section Niveau 2

---

*Les meilleurs produits sont construits avec les utilisateurs, pas pour eux.*
