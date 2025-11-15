# Exemple Complet : Évaluation Chatbot SAV

> **Un cas réel documenté, du Niveau 1 au Niveau 3**

## Contexte

**Entreprise :** E-commerce mode (anonymisé)
**Projet :** Chatbot IA pour service après-vente
**Objectif :** Automatiser 60% des demandes clients niveau 1
**Budget :** 150k€ sur 18 mois
**Timeline :** 6 mois POC + 12 mois production

---

## Niveau 1 : Est-ce que Ça Marche ?

### Méthodologie

**Période :** Semaine 1-2 du POC
**Testeurs :** 3 experts métier SAV
**Nombre de cas :** 100 (70 normaux, 20 limites, 10 pièges)

### Résultats des Tests

| Catégorie | Cas | Points | % |
|-----------|-----|--------|---|
| Normaux | 70 | 61.5 | 87.8% |
| Limites | 20 | 14 | 70.0% |
| Pièges | 10 | 8.5 | 85.0% |
| **TOTAL** | **100** | **84** | **84.0%** ✅ |

### Analyse par Thématique

| Thème | % Correct | Commentaire |
|-------|-----------|-------------|
| Suivi livraison | 92% | Excellent |
| Retours/Remboursements | 88% | Bon |
| Produits/Tailles | 85% | Bon |
| Facturation | 75% | À améliorer |
| Cas complexes | 65% | Limite acceptable |

### Erreurs Identifiées

**Erreur #1 : Hallucination sur les délais promotionnels**
- Fréquence : 3/100 cas
- Gravité : 🔴 Critique
- Exemple : "Pendant les soldes, livraison en 24h garantie" (FAUX)
- Correction : Retrait des données promo obsolètes

**Erreur #2 : Incompréhension questions multi-langues**
- Fréquence : 4/100 cas
- Gravité : 🟡 Moyenne
- Exemple : Question en franglais mal interprétée
- Correction : Entraînement sur données mixtes

**Erreur #3 : Réponses incomplètes sur remboursements**
- Fréquence : 6/100 cas
- Gravité : 🟢 Faible
- Exemple : Oublie de mentionner délai de remboursement
- Correction : Enrichissement des templates

### Métriques Techniques

| Métrique | Valeur | Seuil | Status |
|----------|--------|-------|--------|
| Précision globale | 84% | > 80% | ✅ |
| Temps réponse moyen | 1.8 sec | < 5 sec | ✅ |
| Disponibilité | 99.2% | > 95% | ✅ |
| Taux d'erreur système | 0.8% | < 10% | ✅ |

### Décision Niveau 1

**VALIDÉ** ✅ (Score : 84%)

**Actions avant Niveau 2 :**
1. Corriger hallucinations (délais promo)
2. Améliorer réponses facturation
3. Documenter les limites connues

---

## Niveau 2 : Est-ce que les Utilisateurs l'Utilisent ?

### Méthodologie

**Période :** Semaines 3-6 (4 semaines)
**Participants :** 35 conseillers SAV
**Profils :** 20 juniors (< 1 an), 15 seniors (> 3 ans)
**Utilisation :** En parallèle de leur travail habituel

### Résultats Quantitatifs

| Métrique | Semaine 1 | Semaine 2 | Semaine 3 | Semaine 4 | Cible |
|----------|-----------|-----------|-----------|-----------|-------|
| Taux adoption | 45% | 58% | 65% | 72% | > 50% ✅ |
| Sessions/utilisateur/jour | 3.2 | 5.1 | 6.8 | 8.2 | - |
| Thumbs up | 52% | 61% | 68% | 74% | > 60% ✅ |
| Taux abandon | 35% | 28% | 22% | 18% | < 30% ✅ |

### Satisfaction Utilisateur (Semaine 4)

**Sondage sur 35 participants :**

| Question | Note /5 | Commentaire |
|----------|---------|-------------|
| Facilité d'utilisation | 4.2 | Interface intuitive |
| Qualité des réponses | 3.8 | Bon mais perfectible |
| Gain de temps | 4.5 | Principal avantage |
| Recommanderiez-vous ? | 3.9 | Oui avec réserves |
| **MOYENNE** | **4.1** | **> 3.5** ✅ |

### Entretiens Qualitatifs (10 personnes)

**Ce qui est apprécié :**
- "Me fait gagner 30% de temps sur les questions basiques"
- "Les réponses sont bien formulées, je copie-colle directement"
- "Aide beaucoup les nouveaux qui ne connaissent pas tout"

**Ce qui est critiqué :**
- "Parfois trop générique, manque de personnalisation"
- "Ne comprend pas quand le client est énervé"
- "J'aurais aimé pouvoir corriger directement les erreurs"

**Suggestions :**
- Intégrer le ton du client (détection sentiment)
- Permettre feedback en un clic
- Ajouter les cas spécifiques produits saisonniers

### Signaux d'Alerte Détectés

**Alerte 1 : Différence juniors vs seniors**
- Juniors : 82% adoption, 4.3/5 satisfaction
- Seniors : 58% adoption, 3.8/5 satisfaction
- Action : Formation spécifique seniors sur les cas complexes

**Alerte 2 : Pic d'abandon sur questions complexes**
- 45% d'abandon si question complexe
- Cause : L'IA ne dit pas assez clairement quand elle ne sait pas
- Action : Améliorer la détection des limites

### Décision Niveau 2

**VALIDÉ** ✅ avec améliorations

**Métriques finales :**
- Adoption : 72% (cible 50%) ✅
- Satisfaction : 4.1/5 (cible 3.5) ✅
- Thumbs up : 74% (cible 60%) ✅
- Abandon : 18% (cible < 30%) ✅

**Améliorations intégrées avant Niveau 3 :**
1. Détection du ton client (basique)
2. Message explicite quand hors périmètre
3. Formation complémentaire équipe

---

## Niveau 3 : Est-ce que Ça Rapporte ?

### Méthodologie

**Période :** Mois 2-4 (3 mois de mesure)
**Design :** A/B Test
- Groupe A (avec IA) : 40 conseillers
- Groupe B (sans IA) : 20 conseillers (groupe témoin)

### Résultats A/B Test

| KPI | Groupe A (IA) | Groupe B (sans IA) | Delta | Cible |
|-----|--------------|-------------------|-------|-------|
| Temps réponse moyen | 4h | 18h | **-78%** | -50% ✅ |
| Tickets/conseiller/jour | 85 | 52 | **+63%** | +30% ✅ |
| Satisfaction client (NPS) | 72 | 65 | **+7 pts** | +5 pts ✅ |
| Résolution 1er contact | 78% | 64% | **+14 pts** | +10 pts ✅ |
| Temps moyen traitement | 4.2 min | 7.8 min | **-46%** | -30% ✅ |

### Calcul ROI

**Gains Annuels :**

| Poste | Calcul | Montant |
|-------|--------|---------|
| Productivité agents | +63% × 40 agents × 45k€ = ~1.1M€ en capacité libérée | 280k€ réalloués |
| Réduction turnover | -15% turnover × coût remplacement | 25k€ |
| Satisfaction client | +7 NPS × impact rétention | 45k€ estimé |
| **TOTAL GAINS** | | **350k€/an** |

**Coûts Annuels :**

| Poste | Montant |
|-------|---------|
| Licence IA | 48k€/an |
| Infrastructure cloud | 24k€/an |
| Maintenance (0.5 ETP) | 36k€/an |
| Mise à jour contenu | 12k€/an |
| **TOTAL COÛTS** | **120k€/an** |

**ROI :**

```
ROI = (350k€ - 120k€) / 120k€ × 100 = 192% ✅
```

**Payback :**

```
Investissement initial : 150k€ (POC + setup)
Gain net annuel : 230k€
Payback = 150k€ / 230k€ = 7.8 mois ✅
```

### Impact Non-Financier

**Qualité de vie au travail :**
- 85% des agents disent "moins de tâches répétitives"
- Temps libéré utilisé pour cas complexes (plus valorisant)

**Formation :**
- Nouveaux agents opérationnels 40% plus vite
- L'IA sert de base de connaissances

**Scalabilité :**
- Capacité à absorber +50% de volume sans recrutement
- Prêt pour expansion internationale

### Décision Niveau 3

**VALIDÉ POUR PRODUCTION** ✅

**Résumé :**
- ROI : 192% (cible > 0%) ✅
- Payback : 7.8 mois (cible < 18 mois) ✅
- KPIs métier : +14 à +78% selon métrique (cible +10%) ✅

---

## Bilan Final

### Timeline Réelle vs Prévue

| Phase | Prévu | Réel | Commentaire |
|-------|-------|------|-------------|
| POC (Niveau 1) | 2 semaines | 3 semaines | +1 sem pour corrections |
| Beta (Niveau 2) | 4 semaines | 5 semaines | +1 sem formation seniors |
| Pilote (Niveau 3) | 3 mois | 3 mois | Dans les temps |
| **TOTAL** | **18 semaines** | **21 semaines** | **+17%** |

### Budget Réel vs Prévu

| Poste | Prévu | Réel | Delta |
|-------|-------|------|-------|
| Développement POC | 80k€ | 92k€ | +15% |
| Licence IA (année 1) | 48k€ | 48k€ | 0% |
| Infrastructure | 20k€ | 24k€ | +20% |
| Formation | 5k€ | 12k€ | +140% |
| **TOTAL** | **153k€** | **176k€** | **+15%** |

**Cause du dépassement :** Sous-estimation de la formation et des corrections post-Niveau 1.

### Leçons Apprises

**Ce qui a bien marché :**
1. Approche progressive (3 niveaux) → évite les mauvaises surprises
2. Impliquer les seniors tôt → réduit la résistance au changement
3. Métriques claires dès le départ → décisions objectives

**Ce qu'on ferait différemment :**
1. Prévoir +20% de budget formation (pas juste technique)
2. Tester les cas limites plus tôt (hallucinations)
3. Communiquer davantage sur les limites de l'IA

**Conseils pour votre projet :**
- Ne sautez pas les étapes, même si le Niveau 1 est bon
- Les utilisateurs seniors sont votre plus grand risque (et votre meilleur allié)
- Le ROI réel dépasse souvent les prévisions si l'adoption est bonne

---

## Métriques de Suivi Post-Déploiement

**Tableau de bord mensuel :**

| Métrique | M1 | M2 | M3 | M4 | M5 | M6 |
|----------|----|----|----|----|----|----|
| Précision | 84% | 85% | 86% | 86% | 87% | 87% |
| Adoption | 72% | 78% | 82% | 85% | 86% | 88% |
| Satisfaction | 4.1 | 4.2 | 4.2 | 4.3 | 4.3 | 4.4 |
| Tickets/jour | 85 | 88 | 91 | 93 | 95 | 98 |

**Tendance :** Amélioration continue grâce au feedback et aux mises à jour.

---

*Cas documenté par LaFabriqAI | Données anonymisées | Novembre 2025*
