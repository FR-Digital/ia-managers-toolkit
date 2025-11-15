# Grille d'Évaluation IA

> Template pour scorer les tests et la performance d'un système IA.

---

## 1. Évaluation Niveau 1 : Performance Technique

### Test des 100 Cas

**Date du test :** [JJ/MM/AAAA]
**Testeur :** [Nom]
**Version du modèle :** [X.X]

#### Répartition des Cas

| Type de Cas | Nombre | Description |
|-------------|--------|-------------|
| Cas normaux | 70 | Requêtes standard, cas fréquents |
| Cas limites | 20 | Requêtes difficiles, edge cases |
| Cas pièges | 10 | Hors périmètre, tentatives de manipulation |
| **Total** | **100** | |

#### Grille de Notation

Pour chaque cas, notez :
- ✅ **Correct (1 pt)** : Réponse exacte et complète
- ⚠️ **Partiel (0.5 pt)** : Réponse incomplète mais utile
- ❌ **Faux (0 pt)** : Réponse incorrecte ou hallucination
- 🚫 **Hors sujet (0 pt)** : Ne comprend pas la requête

---

### Tableau de Test

| # | Catégorie | Question/Input | Réponse Attendue | Réponse IA | Note | Commentaire |
|---|-----------|----------------|------------------|------------|------|-------------|
| 1 | Normal | [Question] | [Réponse attendue] | [Réponse obtenue] | [0/0.5/1] | [Notes] |
| 2 | Normal | | | | | |
| 3 | Normal | | | | | |
| ... | ... | | | | | |
| 71 | Limite | | | | | |
| ... | ... | | | | | |
| 91 | Piège | | | | | |
| ... | ... | | | | | |
| 100 | Piège | | | | | |

---

### Calcul du Score

| Métrique | Calcul | Résultat |
|----------|--------|----------|
| Score Cas Normaux | [X] / 70 × 100 | [X]% |
| Score Cas Limites | [X] / 20 × 100 | [X]% |
| Score Cas Pièges | [X] / 10 × 100 | [X]% |
| **Score Global** | **[X] / 100 × 100** | **[X]%** |

### Interprétation

| Score | Verdict | Action |
|-------|---------|--------|
| > 80% | ✅ PASS | Passer au Niveau 2 |
| 60-80% | ⚠️ À AMÉLIORER | Identifier et corriger les erreurs |
| < 60% | ❌ FAIL | Retour en développement |

**Score obtenu : [X]% → [VERDICT]**

---

### Analyse des Erreurs

#### Types d'Erreurs Identifiés

| Type d'Erreur | Occurrences | % du Total | Exemples | Gravité |
|---------------|-------------|------------|----------|---------|
| Hallucination (invente) | [X] | [X]% | [Ex] | CRITIQUE |
| Incompréhension | [X] | [X]% | [Ex] | HAUTE |
| Réponse incomplète | [X] | [X]% | [Ex] | MOYENNE |
| Hors périmètre non géré | [X] | [X]% | [Ex] | HAUTE |
| Temps dépassé | [X] | [X]% | [Ex] | MOYENNE |

#### Actions Correctives

| Erreur | Cause Probable | Action Corrective | Responsable | Deadline |
|--------|---------------|-------------------|-------------|----------|
| [Type] | [Cause] | [Action] | [Nom] | [Date] |
| | | | | |
| | | | | |

---

## 2. Évaluation Niveau 2 : Adoption Utilisateur

### Métriques d'Adoption

**Période d'évaluation :** [Date début] → [Date fin]
**Nombre utilisateurs pilotes :** [X]

| Métrique | Semaine 1 | Semaine 2 | Semaine 3 | Semaine 4 | Cible |
|----------|-----------|-----------|-----------|-----------|-------|
| Utilisateurs actifs | [X] | [X] | [X] | [X] | > 50% |
| Utilisations/jour moyen | [X] | [X] | [X] | [X] | [X] |
| Taux d'abandon session | [X]% | [X]% | [X]% | [X]% | < 30% |
| Feedback positif (pouce haut) | [X]% | [X]% | [X]% | [X]% | > 60% |

### Sondage Satisfaction

**Nombre de répondants :** [X] / [X] (taux réponse : [X]%)

| Question | Score Moyen (1-5) | Commentaires Fréquents |
|----------|-------------------|------------------------|
| L'IA est facile à utiliser | [X]/5 | [Résumé] |
| Les réponses sont utiles | [X]/5 | [Résumé] |
| Je fais confiance aux réponses | [X]/5 | [Résumé] |
| Je préfère l'IA à l'ancienne méthode | [X]/5 | [Résumé] |
| Je recommande l'IA à mes collègues | [X]/5 | [Résumé] |
| **Score Global** | **[X]/5** | |

### Verdict Niveau 2

| Métrique | Résultat | Seuil | Verdict |
|----------|----------|-------|---------|
| Adoption | [X]% | > 50% | [PASS/FAIL] |
| Satisfaction | [X]/5 | > 3.5/5 | [PASS/FAIL] |
| Feedback positif | [X]% | > 60% | [PASS/FAIL] |
| Abandon | [X]% | < 30% | [PASS/FAIL] |

**Verdict Global Niveau 2 : [PASS / FAIL / À AMÉLIORER]**

---

## 3. Évaluation Niveau 3 : Impact Business

### Comparaison Avant/Après (ou A/B Test)

**Période de mesure :** [Date début] → [Date fin]
**Méthode :** [Avant/Après] ou [A/B Test avec groupe témoin]

| KPI | Baseline (avant/sans IA) | Avec IA | Amélioration | Objectif |
|-----|--------------------------|---------|--------------|----------|
| [KPI 1 - ex: temps traitement] | [X] | [X] | [X]% | [X]% |
| [KPI 2 - ex: satisfaction client] | [X] | [X] | [X]pts | [X]pts |
| [KPI 3 - ex: volume traité] | [X] | [X] | [X]% | [X]% |
| [KPI 4 - ex: taux erreur] | [X] | [X] | [X]% | [X]% |
| [KPI 5 - ex: coût unitaire] | [X]€ | [X]€ | [X]% | [X]% |

### Calcul ROI Réel

**Gains Mensuels Mesurés :**

| Bénéfice | Calcul | Montant |
|----------|--------|---------|
| Temps économisé | [X]h × [X]€/h | [X]€ |
| Erreurs évitées | [X] cas × [X]€ | [X]€ |
| Volume additionnel | [X] unités × [X]€ | [X]€ |
| **Total Mensuel** | | **[X]€** |
| **Total Annuel (×12)** | | **[X]k€** |

**Coûts Mensuels Réels :**

| Coût | Montant |
|------|---------|
| Infrastructure | [X]€ |
| APIs/Services | [X]€ |
| Maintenance (X ETP) | [X]€ |
| **Total Mensuel** | **[X]€** |

**ROI Réel :**
```
Gains annuels : [X]k€
Coûts annuels : [X]k€
ROI = ([X] - [X]) / [X] × 100 = [X]%
```

**ROI Projeté vs Réel :**
- ROI Projeté (business case) : [X]%
- ROI Réel mesuré : [X]%
- Écart : [X] points

### Verdict Niveau 3

| Critère | Résultat | Seuil | Verdict |
|---------|----------|-------|---------|
| ROI | [X]% | > 0% | [PASS/FAIL] |
| KPIs métier améliorés | [X] sur [X] | Majorité | [PASS/FAIL] |
| Écart vs projection | [X]% | < 30% | [ACCEPTABLE/NON] |

**Verdict Global Niveau 3 : [PASS / FAIL / OPTIMISER]**

---

## 4. Synthèse Globale

### Résumé des 3 Niveaux

| Niveau | Score/Métrique | Verdict | Action |
|--------|----------------|---------|--------|
| 1. Performance Technique | [X]% | [PASS/FAIL] | [Action] |
| 2. Adoption Utilisateur | [X]/5 satisfaction | [PASS/FAIL] | [Action] |
| 3. Impact Business | [X]% ROI | [PASS/FAIL] | [Action] |

### Recommandation Finale

**[GO PRODUCTION / AMÉLIORER ET RÉÉVALUER / PIVOTER / ARRÊTER]**

**Justification :**
[Explication en 3-4 phrases de la recommandation basée sur les données ci-dessus]

### Actions Suivantes

| Action | Responsable | Deadline | Priorité |
|--------|-------------|----------|----------|
| [Action 1] | [Nom] | [Date] | [Haute/Moyenne/Basse] |
| [Action 2] | [Nom] | [Date] | |
| [Action 3] | [Nom] | [Date] | |

---

## 5. Annexes

### A. Détail des Tests Niveau 1
[Joindre fichier Excel avec les 100 cas testés]

### B. Verbatims Utilisateurs
[Citations des feedbacks qualitatifs importants]

### C. Graphiques de Tendance
[Évolution des métriques dans le temps]

---

**Document préparé par :** [Nom]
**Date :** [JJ/MM/AAAA]
**Prochaine évaluation prévue :** [JJ/MM/AAAA]

---

*Template Grille d'Évaluation | v1.0 | Nov 2025*
