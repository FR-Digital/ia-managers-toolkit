# Métriques Business vs Métriques Techniques

> Traduire le jargon data en indicateurs business compréhensibles.

## Le Problème

Votre équipe data vous dit : "Le modèle a 92% de précision !"

Vous vous demandez : "Ça veut dire quoi pour mon business ?"

Ce guide vous aide à **traduire** les métriques techniques en impact business réel.

---

## Métriques Techniques Décryptées

### Précision (Accuracy)

**Ce que ça veut dire :**
% de bonnes réponses sur l'ensemble des prédictions.

**Piège :**
Peut être trompeuse si les classes sont déséquilibrées.

**Exemple :**
Si 95% de vos emails sont normaux, une IA qui dit "pas spam" à tout a 95% de précision. Mais elle rate tous les vrais spams !

**Question business :**
"Sur 100 prédictions, combien sont correctes ?"

---

### Recall (Rappel/Sensibilité)

**Ce que ça veut dire :**
Parmi tous les vrais cas positifs, combien l'IA en a trouvé.

**Quand c'est critique :**
Quand manquer un cas coûte cher.

**Exemples business :**
- Fraude : Recall bas = fraudes non détectées = pertes financières
- Diagnostic médical : Recall bas = maladies non détectées = risque patient
- Churn : Recall bas = clients perdus qu'on aurait pu sauver

**Question business :**
"Sur tous les cas qui nécessitent action, combien l'IA en trouve ?"

---

### Precision (Précision du Positif)

**Ce que ça veut dire :**
Parmi ce que l'IA prédit comme positif, combien le sont vraiment.

**Quand c'est critique :**
Quand les faux positifs coûtent cher.

**Exemples business :**
- Fraude : Precision bas = trop de fausses alertes = équipe débordée
- Email important : Precision bas = emails normaux en spam = perte d'infos
- Lead scoring : Precision bas = commerciaux perdent du temps

**Question business :**
"Sur tout ce que l'IA signale comme critique, combien sont vraiment critiques ?"

---

## Traduire en Impact Business

### Table de Traduction

| Métrique Technique | Question Business | Impact si Mauvais |
|-------------------|-------------------|-------------------|
| Précision 85% | "Sur 100 décisions, 85 sont correctes" | 15% d'erreurs quelconques |
| Recall 70% | "Sur 100 vrais cas, on en trouve 70" | 30% de cas importants ratés |
| Precision 80% | "Sur 100 alertes, 80 sont justifiées" | 20% de temps perdu sur faux positifs |
| Latence 3s | "L'utilisateur attend 3 secondes" | Frustration, abandon |
| Uptime 99% | "3.65 jours d'indisponibilité/an" | Perte service pendant pannes |

---

## Métriques Business par Cas d'Usage

### Chatbot Service Client

| Métrique Tech | Métrique Business | Cible |
|---------------|-------------------|-------|
| Précision réponse | Taux de résolution 1er contact | > 70% |
| Recall intentions | Questions comprises correctement | > 85% |
| Latence | Temps de réponse | < 3s |
| Taux hallucination | Réponses factuellement fausses | < 2% |

**KPIs Business à Suivre :**
- Satisfaction client (NPS)
- Temps moyen de résolution
- Coût par interaction
- Taux d'escalade vers humain

---

### Détection de Fraude

| Métrique Tech | Métrique Business | Cible |
|---------------|-------------------|-------|
| Recall | % de fraudes détectées | > 95% |
| Precision | % d'alertes justifiées | > 60% |
| Latence | Temps de détection | < 1min |

**KPIs Business à Suivre :**
- Montant frauduleux évité
- Coût des faux positifs (investigation)
- Temps de traitement des alertes
- Taux de fraude global

**Calcul d'Impact :**
```
Si Recall passe de 90% à 95%
= 5% de fraudes supplémentaires détectées
= Sur 10M€ de fraude annuelle : 500k€ économisés
```

---

### Prédiction de Churn

| Métrique Tech | Métrique Business | Cible |
|---------------|-------------------|-------|
| Recall | % clients à risque identifiés | > 80% |
| Precision | % des alertes qui churnent vraiment | > 50% |
| AUC-ROC | Capacité à discriminer | > 0.8 |

**KPIs Business à Suivre :**
- Taux de rétention
- Revenue sauvé
- Coût d'acquisition vs coût de rétention
- ROI des actions de rétention

**Calcul d'Impact :**
```
1000 clients à risque identifiés
Precision 60% = 600 vrais churners
Action de rétention : 40% sauvés
= 240 clients conservés
Si LTV = 1000€ par client
= 240k€ de revenue préservé
```

---

### Automatisation Documents (OCR)

| Métrique Tech | Métrique Business | Cible |
|---------------|-------------------|-------|
| Précision extraction | Champs correctement extraits | > 95% |
| Recall | Champs trouvés | > 98% |
| Taux d'erreur | Documents à retraiter manuellement | < 5% |

**KPIs Business à Suivre :**
- Temps de traitement par document
- Coût par document
- Taux d'intervention humaine
- Volume traité par jour

---

## Framework de Conversion

### Étape 1 : Identifier le Coût de l'Erreur

**Faux Négatif (cas raté) :**
- Fraude non détectée → Perte financière directe
- Client à risque non identifié → Perte de revenue
- Défaut qualité non vu → Rappel produit coûteux

**Faux Positif (fausse alerte) :**
- Transaction légitime bloquée → Client frustré
- Alert inutile → Temps équipe gaspillé
- Email normal en spam → Information manquée

### Étape 2 : Quantifier en Euros

```
Impact Erreur = Volume × Taux d'erreur × Coût unitaire
```

**Exemple Fraude :**
- Volume transactions : 1M/mois
- Taux fraude : 0.5% = 5000 fraudes/mois
- Montant moyen : 200€
- Recall 90% = 10% non détectées = 500 fraudes
- Perte : 500 × 200€ = 100k€/mois

### Étape 3 : Comparer les Scénarios

| Scénario | Recall | Fraudes Manquées | Perte Mensuelle |
|----------|--------|------------------|-----------------|
| Actuel | 85% | 750 | 150k€ |
| Nouvelle IA | 95% | 250 | 50k€ |
| **Gain** | +10pts | -500 | **100k€/mois** |

---

## Tableau de Bord Business Recommandé

### Métriques Quotidiennes
- Volume de requêtes
- Temps de réponse moyen
- Taux d'erreur détecté
- Alertes critiques

### Métriques Hebdomadaires
- Satisfaction utilisateur
- Taux d'adoption
- Tickets support liés à l'IA
- Coût cumulé (API, infra)

### Métriques Mensuelles
- ROI cumulé
- Tendance performance (drift ?)
- KPIs métier vs baseline
- Feedback utilisateurs qualitatif

---

## Questions à Poser pour Chaque Métrique

1. **"Qu'est-ce que ça coûte quand l'IA se trompe ?"**
   - Financier (perte directe, coût d'opportunité)
   - Opérationnel (temps perdu, process bloqué)
   - Réputationnel (client insatisfait, image)

2. **"Quel niveau d'erreur est acceptable ?"**
   - Basé sur le coût ci-dessus
   - Comparé à la solution actuelle
   - Conforme aux régulations

3. **"Comment mesure-t-on l'amélioration ?"**
   - Baseline avant IA
   - Mesures après IA
   - Groupe témoin si possible

---

## Anti-Patterns à Éviter

### "Notre précision est de 99% !"
**Méfiance si :**
- Pas de détail sur recall et precision
- Testé sur données d'entraînement
- Classe déséquilibrée non mentionnée

### "L'IA est meilleure qu'un humain"
**Vérifiez :**
- Sur quels cas précis ?
- Dans quelles conditions ?
- Avec quel coût ?

### "On optimise la précision"
**Attention :**
- Précision seule est insuffisante
- Parfois recall ou precision plus important
- Dépend du coût des erreurs

---

## Ressources

- [Framework 3 niveaux](framework-3-niveaux.md) - Évaluation complète
- [Questions équipe tech](questions-equipe-tech.md) - Creuser les métriques
- [Budget et ROI](../pilotage/budget-et-roi.md) - Calculer le ROI

---

*Métriques business vs tech | Dernière MAJ : Nov 2025*
