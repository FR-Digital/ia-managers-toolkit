# Métriques Business vs Techniques

> **Traduire le jargon data science en langage business**

## Le Problème

Votre équipe data vous dit : *"Le modèle a un F1-score de 0.89 avec une AUC-ROC de 0.94"*

Vous vous demandez : *"OK, mais ça veut dire quoi pour mon business ?"*

Ce guide traduit les métriques techniques en impacts business compréhensibles.

---

## Les 10 Métriques Techniques Essentielles

### 1. Précision (Accuracy)

**Définition technique :**
Pourcentage de prédictions correctes sur l'ensemble des prédictions.

**Ce que ça veut dire business :**
"Sur 100 réponses de l'IA, combien sont justes ?"

**Exemple :**
- Précision 85% = 85 réponses correctes sur 100
- Précision 95% = 95 réponses correctes sur 100

**Quand c'est important :**
Quand toutes les erreurs ont le même coût.

**Piège :**
Si 95% de vos emails sont normaux et 5% urgents, une IA qui dit "normal" à tout aura 95% de précision... mais ratera tous les urgents !

---

### 2. Précision (Precision)

**Définition technique :**
Parmi les cas que l'IA identifie comme positifs, combien le sont vraiment ?

**Ce que ça veut dire business :**
"Quand l'IA dit OUI, a-t-elle raison ?"

**Exemple concret :**
- IA identifie 100 emails comme "urgents"
- 80 sont vraiment urgents, 20 sont normaux
- Précision = 80%

**Impact business :**
Faible précision = beaucoup de fausses alertes = équipe perd confiance et ignore les alertes.

**Quand c'est important :**
Quand les faux positifs coûtent cher (ex: investigation inutile, action non nécessaire).

---

### 3. Rappel (Recall)

**Définition technique :**
Parmi tous les vrais cas positifs, combien l'IA en trouve-t-elle ?

**Ce que ça veut dire business :**
"L'IA rate-t-elle des cas importants ?"

**Exemple concret :**
- Il y a 100 emails vraiment urgents
- L'IA en détecte 70
- Rappel = 70%
- 30 urgents sont ratés !

**Impact business :**
Faible rappel = risque de rater des cas critiques = clients insatisfaits, opportunités manquées.

**Quand c'est important :**
Quand rater un cas est grave (ex: fraude non détectée, client VIP ignoré).

---

### 4. F1-Score

**Définition technique :**
Moyenne harmonique entre Précision et Rappel.

**Ce que ça veut dire business :**
"Équilibre entre ne pas rater de cas et ne pas avoir trop de fausses alertes."

**Interprétation simple :**

| F1-Score | Qualité | Traduction Business |
|----------|---------|---------------------|
| > 0.9 | Excellent | Très fiable |
| 0.8 - 0.9 | Bon | Utilisable en production |
| 0.7 - 0.8 | Moyen | Besoin d'amélioration |
| < 0.7 | Faible | Non recommandé |

**Quand c'est important :**
Quand vous voulez un indicateur unique de qualité équilibrée.

---

### 5. Taux de Faux Positifs (False Positive Rate)

**Définition technique :**
Pourcentage de cas normaux incorrectement identifiés comme problématiques.

**Ce que ça veut dire business :**
"Combien de fausses alertes pour 100 cas normaux ?"

**Exemple :**
- 1000 emails normaux
- L'IA en marque 50 comme "urgents" (faux positifs)
- Taux FP = 5%

**Impact business :**
- 5% FP sur 1000 emails/jour = 50 fausses alertes/jour
- Équipe frustrée, perte de temps

**Seuils typiques :**
- < 1% = Excellent
- 1-5% = Acceptable
- > 10% = Problématique

---

### 6. Taux de Faux Négatifs (False Negative Rate)

**Définition technique :**
Pourcentage de cas problématiques incorrectement identifiés comme normaux.

**Ce que ça veut dire business :**
"Combien de vrais problèmes l'IA rate-t-elle ?"

**Exemple :**
- 100 emails vraiment urgents
- L'IA en rate 15
- Taux FN = 15%

**Impact business :**
15% de clients urgents non traités à temps = insatisfaction, churn potentiel.

**Seuils typiques :**
- < 5% = Bon (selon criticité)
- 5-15% = À surveiller
- > 20% = Risque majeur

---

### 7. Temps de Réponse (Latency)

**Définition technique :**
Temps entre la requête et la réponse de l'IA.

**Ce que ça veut dire business :**
"Combien de temps l'utilisateur attend ?"

**Seuils UX classiques :**

| Temps | Perception utilisateur |
|-------|------------------------|
| < 1 sec | Instantané |
| 1-3 sec | Rapide |
| 3-10 sec | Acceptable |
| > 10 sec | Frustrant |

**Impact business :**
- Latence élevée = abandon utilisateur
- Dans certains cas (trading, sécurité), la latence est critique

---

### 8. Disponibilité (Uptime)

**Définition technique :**
Pourcentage de temps où le système est opérationnel.

**Ce que ça veut dire business :**
"L'IA est-elle accessible quand on en a besoin ?"

**Calcul simple :**

| Disponibilité | Indisponibilité/an | Indisponibilité/mois |
|---------------|---------------------|----------------------|
| 99% | 3.65 jours | 7.3 heures |
| 99.9% | 8.76 heures | 43.8 minutes |
| 99.99% | 52.6 minutes | 4.3 minutes |

**Impact business :**
- 95% dispo = 18 jours d'indisponibilité/an = inacceptable pour outil critique
- 99.9% = standard industrie

---

### 9. Coût par Inférence

**Définition technique :**
Coût pour chaque requête traitée par l'IA.

**Ce que ça veut dire business :**
"Combien me coûte chaque utilisation ?"

**Calcul du coût total :**

```
Coût mensuel = Coût/requête × Nb requêtes/mois

Exemple :
- 0.02€/requête
- 10,000 requêtes/mois
- Coût = 200€/mois
```

**Points d'attention :**
- Les coûts peuvent exploser avec le volume
- Certaines API ont des paliers (moins cher au volume)
- Ne pas oublier : infrastructure, maintenance, personnel

---

### 10. Drift (Dérive)

**Définition technique :**
Dégradation des performances de l'IA au fil du temps.

**Ce que ça veut dire business :**
"L'IA devient-elle moins bonne avec le temps ?"

**Causes typiques :**
- Les données changent (nouveaux produits, comportements clients)
- Le contexte évolue (réglementation, marché)
- Le modèle n'est pas mis à jour

**Impact business :**
- Précision à 90% au lancement
- Précision à 75% après 6 mois sans mise à jour
- Performance dégradée = utilisateurs frustrés

**Prévention :**
- Monitoring continu des métriques
- Alertes si dégradation > X%
- Plan de réentraînement régulier

---

## Tableau de Traduction Rapide

| Terme Technique | Traduction Business | Question à Poser |
|-----------------|---------------------|------------------|
| Accuracy | % de bonnes réponses | "Sur 100 réponses, combien justes ?" |
| Precision | Fiabilité des alertes | "Les alertes sont-elles vraies ?" |
| Recall | Couverture des cas | "Combien de cas rate-t-on ?" |
| F1-Score | Qualité équilibrée | "Est-ce globalement fiable ?" |
| False Positive | Fausse alerte | "Combien de bruit inutile ?" |
| False Negative | Cas raté | "Combien de vrais problèmes ignorés ?" |
| Latency | Temps d'attente | "C'est assez rapide ?" |
| Uptime | Disponibilité | "C'est accessible quand on en a besoin ?" |
| Cost per inference | Prix par utilisation | "Combien ça coûte à chaque fois ?" |
| Drift | Perte de qualité dans le temps | "L'IA reste-t-elle bonne sur la durée ?" |

---

## Cas Pratiques : Choisir les Bonnes Métriques

### Chatbot SAV

**Métriques prioritaires :**
- **Précision des réponses** (>85%) - Éviter les infos fausses
- **Rappel** (élevé) - Ne pas rater de questions
- **Latence** (<3 sec) - Expérience utilisateur fluide

**Métrique secondaire :**
- Coût par requête (contrôler budget)

---

### Détection de Fraude

**Métriques prioritaires :**
- **Rappel** (>95%) - Ne pas rater de fraudes (critique !)
- **Taux de faux positifs** (<5%) - Éviter de bloquer les vrais clients
- **Latence** (<1 sec) - Décision en temps réel

**Trade-off accepté :**
Plus de faux positifs pour garantir de ne rater aucune fraude.

---

### Recommandation Produit

**Métriques prioritaires :**
- **Précision** - Recommandations pertinentes
- **Taux de clic** - Les gens achètent-ils ?
- **Coût par inférence** - ROI positif

**Métrique secondaire :**
- Rappel (moins critique, on peut rater des opportunités)

---

### Classification Documents

**Métriques prioritaires :**
- **Précision globale** (>90%) - Documents bien classés
- **F1-Score par catégorie** - Équilibré sur toutes les classes

**Métrique secondaire :**
- Latence (batch processing OK)

---

## Comment Demander les Bonnes Métriques

### Questions à Poser à Votre Équipe Data

1. **"Quelle est la précision globale ?"**
   - Attendre : un % clair avec intervalle de confiance

2. **"Quel est le taux de faux négatifs sur les cas critiques ?"**
   - Attendre : un % et une analyse d'impact

3. **"Comment la performance évolue-t-elle sur les dernières semaines ?"**
   - Attendre : un graphique montrant la stabilité

4. **"Quel est le temps de réponse au 95ème percentile ?"**
   - Attendre : "95% des requêtes répondues en moins de X secondes"

5. **"Combien coûte l'inférence à notre volume prévu ?"**
   - Attendre : un chiffre mensuel clair

### Red Flags (Signaux d'Alerte)

❌ **"La précision est bonne"** sans chiffre précis
❌ **"On n'a pas mesuré le drift"**
❌ **"Le coût dépend..."** sans estimation
❌ **"On verra en production"** pour des métriques critiques

---

## Template : Rapport de Métriques Business

**Projet :** [Nom]
**Date :** [Date]

### Performance

| Métrique | Valeur | Seuil Min | Status | Impact Business |
|----------|--------|-----------|--------|-----------------|
| Précision | [ ]% | >80% | ✅❌ | [Traduction] |
| Rappel | [ ]% | >[ ]% | ✅❌ | [Traduction] |
| F1-Score | [ ] | >0.8 | ✅❌ | [Traduction] |
| Faux Positifs | [ ]% | <[ ]% | ✅❌ | [Traduction] |
| Faux Négatifs | [ ]% | <[ ]% | ✅❌ | [Traduction] |

### Opérationnel

| Métrique | Valeur | Seuil | Status | Impact Business |
|----------|--------|-------|--------|-----------------|
| Latence P95 | [ ] sec | <[ ] sec | ✅❌ | [Traduction] |
| Disponibilité | [ ]% | >99% | ✅❌ | [Traduction] |
| Coût/mois | [ ]€ | <[ ]€ | ✅❌ | [Traduction] |

### Recommandation

[GO / NO-GO / À AMÉLIORER]

**Raison principale :** [En langage business clair]

---

## Conclusion

**Vous n'avez pas besoin de comprendre les maths derrière les métriques.**

**Vous avez besoin de savoir :**
1. Ce que chaque métrique signifie pour votre business
2. Quel impact si la métrique est mauvaise
3. Quel seuil est acceptable pour votre contexte

Les métriques techniques ne sont que des indicateurs. Votre rôle est de les traduire en décisions business.

---

*Les chiffres ne mentent pas, mais ils ne parlent pas non plus. C'est à vous de leur donner du sens.*
