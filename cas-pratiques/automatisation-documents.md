# Cas Pratique : Automatisation Traitement Documents

> Retour d'expérience sur l'automatisation de l'extraction d'informations depuis des documents (factures, contrats).

---

## Contexte

**Entreprise :** Cabinet de conseil (150 employés)
**Département :** Finance / Comptabilité
**Durée projet :** 8 mois (Mars - Octobre 2024)
**Budget total :** 95k€

---

## Le Problème Initial

### Situation Avant Projet

**Processus actuel :**
- Réception de 500 factures fournisseurs/mois
- 3 comptables dédiés à la saisie
- Temps moyen : 8 min/facture
- Volume mensuel : 67 heures de saisie pure

**Douleurs identifiées :**
1. **Tâche répétitive** : Copier/coller des champs identiques
2. **Erreurs de saisie** : 4% des factures avec erreurs
3. **Délais** : Retards de paiement fréquents
4. **Coûts** : 45k€/an pour la saisie seule
5. **Frustration équipe** : Tâche sans valeur ajoutée

**Impact business :**
- Pénalités de retard : 8k€/an
- Erreurs comptables : 12k€/an de corrections
- Moral équipe : Faible sur ces tâches

---

## La Solution Proposée

### Objectif

Automatiser l'extraction des informations clés des factures PDF (fournisseur, montant, TVA, date, etc.) pour injection automatique dans l'ERP.

### Type d'IA Choisi

**Architecture :** OCR + NLP + Extraction structurée

**Stack technique :**
- OCR : Azure Document Intelligence
- Extraction : Modèle custom fine-tuné
- Validation : Règles métier + vérification humaine
- Intégration : API vers ERP (SAP)

**Pourquoi ce choix :**
- Documents structurés (factures) = patterns identifiables
- OCR mature et fiable
- Possibilité de fine-tuning sur nos formats
- ROI calculable précisément

---

## Déroulement du Projet

### Phase 1 : Cadrage (3 semaines) - 8k€

**Activités :**
- Audit des factures existantes (formats, fournisseurs)
- Identification des champs à extraire
- Analyse des cas complexes
- Business case et ROI

**Découvertes clés :**
- 80% des factures viennent de 30 fournisseurs
- 12 formats différents principaux
- Champs critiques : Date, Montant HT, TVA, IBAN, Réf fournisseur
- 15% des factures sont des scans de mauvaise qualité

**Équipe :**
- 1 Chef de projet (30%)
- 1 Responsable comptable (20%)
- 1 Consultant ML (externe, 40%)

---

### Phase 2 : POC (6 semaines) - 32k€

**Objectif POC :** Démontrer l'extraction fiable sur les 5 fournisseurs principaux (50% du volume).

**Activités :**
- Collecte de 500 factures pour entraînement
- Annotation manuelle des champs (3 personnes, 2 semaines)
- Setup Azure Document Intelligence
- Fine-tuning du modèle d'extraction
- Tests sur 100 factures non vues

**Résultats POC :**

| Champ | Précision | Objectif | Verdict |
|-------|-----------|----------|---------|
| Date facture | 96% | > 95% | ✅ |
| Montant HT | 94% | > 95% | ⚠️ |
| Montant TVA | 92% | > 95% | ❌ |
| Fournisseur | 98% | > 95% | ✅ |
| IBAN | 88% | > 95% | ❌ |
| Référence | 91% | > 90% | ✅ |

**Problèmes identifiés :**
- TVA mal extraite quand plusieurs taux
- IBAN difficile sur scans basse qualité
- Formats manuscrits non gérés

**Décision :** GO Pilote avec améliorations sur TVA et IBAN

---

### Phase 3 : Pilote (10 semaines) - 40k€

**Améliorations apportées :**
- Logique spécifique pour TVA multiple
- Pré-traitement images (amélioration qualité scan)
- Validation croisée des champs (cohérence)
- Interface de correction humaine

**Déploiement :**
- Mois 1 : 100 factures/mois (20% volume) - validation 100% humaine
- Mois 2 : 250 factures/mois - validation 50% humaine (échantillonnage)
- Mois 3 : 500 factures/mois - validation 20% humaine

**Résultats Pilote :**

| Métrique | Mois 1 | Mois 2 | Mois 3 | Cible |
|----------|--------|--------|--------|-------|
| Extraction correcte | 89% | 93% | 95% | > 95% |
| Besoin correction | 11% | 7% | 5% | < 10% |
| Temps/facture | 3 min | 2 min | 1.5 min | < 2 min |
| Rejet (non traitable) | 8% | 5% | 3% | < 5% |

**Workflow final :**
1. Facture PDF reçue
2. IA extrait les champs
3. Score de confiance calculé
4. Si confiance > 90% : validation automatique
5. Si confiance 70-90% : vérification rapide humaine
6. Si confiance < 70% : traitement manuel
7. Injection dans ERP

**Incidents notables :**
- Format facture d'un gros fournisseur changé → réentraînement nécessaire
- Factures avec avoir négatif mal gérées → règles ajoutées

---

### Phase 4 : Production - 15k€ setup + 12k€/an maintenance

**Configuration production :**
- 100% des factures passent par l'IA
- 85% traitées automatiquement (confiance > 90%)
- 10% vérification rapide (confiance 70-90%)
- 5% manuel (complexes ou mauvaise qualité)

**Maintenance :**
- Monitoring mensuel des performances
- Ajout de nouveaux fournisseurs dans le modèle
- Ré-entraînement trimestriel si nécessaire

---

## Résultats Business

### Comparaison Avant/Après

| KPI | Avant | Après | Amélioration |
|-----|-------|-------|--------------|
| Temps/facture | 8 min | 1.5 min | **-81%** |
| Heures saisie/mois | 67h | 12.5h | **-81%** |
| Taux d'erreur | 4% | 0.8% | **-80%** |
| Délai traitement | 5 jours | 1 jour | **-80%** |
| Pénalités retard | 8k€/an | 1k€/an | **-87%** |

### Impact Équipe

**Comptables :**
- Temps libéré : 55h/mois (3 personnes × 18h)
- Réaffectation : Analyse financière, contrôle de gestion
- Satisfaction : Augmentée (tâches plus intéressantes)

**Pas de réduction d'effectif** : Les comptables font maintenant du travail à plus forte valeur (analyse, conseil interne).

### ROI Réel

**Coûts totaux :**
- Développement : 80k€
- Setup production : 15k€
- **Total Y1 : 95k€**

**Maintenance annuelle (Y2+) :** 12k€/an

**Gains annuels :**
- Temps économisé : 55h/mois × 12 × 50€/h = 33k€
- Erreurs évitées : 10k€
- Pénalités évitées : 7k€
- Travail à valeur ajoutée (difficile à chiffrer) : ~20k€
- **Total gains : ~70k€/an**

**Calcul ROI :**
```
Y1 : Gains 70k€ - Coûts 95k€ = -25k€
Y2 : Gains 70k€ - Coûts 12k€ = +58k€
Y3 : Gains 70k€ - Coûts 12k€ = +58k€

Total 3 ans : 70×3 - 95 - 12 - 12 = 91k€
ROI 3 ans = 91k€ / 119k€ = 76%
Payback = 95k€ / 70k€ = 16 mois
```

**Note :** ROI plus faible qu'un chatbot car :
- Volume plus faible (500/mois vs 800/jour)
- Gains unitaires moins importants
- Mais qualité de vie équipe nettement améliorée

---

## Leçons Apprises

### Ce qui a bien fonctionné ✅

1. **Périmètre limité** : Focus sur factures seulement (pas contrats, devis, etc.)
2. **Validation humaine conservée** : Filet de sécurité sur la comptabilité
3. **Amélioration continue** : Ajout progressif de fournisseurs
4. **Implication comptables** : Ils ont annoté et validé
5. **Métriques business claires** : Temps économisé mesurable

### Ce qui aurait pu être mieux 🔧

1. **Qualité des scans** : Auraient dû forcer des standards dès le départ
   - Solution : Scanner haute qualité + politique de réception

2. **Formats qui changent** : Pas prévu que les fournisseurs changent leurs factures
   - Solution : Monitoring des drifts + budget ré-entraînement

3. **Cas limites** : Avoirs, factures rectificatives mal anticipés
   - Solution : Meilleure analyse initiale des cas complexes

4. **Documentation fournisseurs** : Pas assez de coordination
   - Solution : Demander formats standards aux gros fournisseurs

### Conseils pour Reproduction

1. **Commencez par un type de document** : Ne faites pas tout en même temps
2. **Investissez dans l'annotation** : Qualité des exemples = qualité du modèle
3. **Gardez la validation humaine** : Surtout pour la comptabilité
4. **Mesurez le temps réel** : Avant et après, précisément
5. **Prévoyez la maintenance** : Les documents évoluent
6. **Impliquez les utilisateurs finaux** : Ce sont eux qui connaissent les pièges

---

## Évolutions Prévues (V2)

**Court terme (6 mois) :**
- Extension aux bons de commande
- Réconciliation automatique facture/BC
- Alertes sur anomalies (prix différent, quantités)

**Moyen terme (12 mois) :**
- Traitement des contrats (extraction clauses clés)
- Analyse prédictive des cash flows
- Dashboard fournisseurs intelligent

**Budget V2 :** 50k€ estimé

---

## Conclusion

L'automatisation du traitement documentaire via IA est un cas d'usage **solide mais moins spectaculaire** qu'un chatbot :

**Points forts :**
- ROI mesurable et garanti
- Amélioration qualité de vie équipe
- Réduction erreurs significative
- Accélération des processus

**Points d'attention :**
- ROI plus long à atteindre (16 mois vs 5 mois pour chatbot)
- Nécessite investissement en annotation
- Maintenance continue (formats qui changent)
- Volume critique nécessaire pour rentabilité

**Recommandé si :**
- Volume > 200 documents/mois
- Processus répétitif et structuré
- Erreurs coûteuses à corriger
- Équipe frustrée par les tâches répétitives

---

*Cas pratique automatisation documents | Nov 2025*
