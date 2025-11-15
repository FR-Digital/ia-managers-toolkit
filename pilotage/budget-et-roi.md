# Budget et ROI d'un Projet IA

> Comprendre les vrais coûts et calculer le retour sur investissement.

## Les Coûts Cachés de l'IA

Un projet IA coûte **2 à 3 fois plus cher** que l'estimation initiale. Voici pourquoi.

---

## Décomposition des Coûts

### 1. Coûts de Développement (40-50% du total)

**Équipe type POC (2-3 mois) :**
- 1 Data Scientist senior (10-15k€/mois)
- 0.5 Data Engineer (5-7k€/mois)
- 0.2 ML Engineer (2-3k€/mois)
- **Total POC : 30-80k€**

**Équipe type Production (6-12 mois) :**
- 1-2 Data Scientists
- 1 Data Engineer
- 1 ML Engineer
- 0.5 DevOps/Infra
- 0.3 Product Owner
- **Total : 150-400k€**

**Coûts cachés :**
- Recrutement (agence : 20-30% salaire annuel)
- Formation équipe existante
- Temps management projet (10-15% en plus)

### 2. Coûts Infrastructure (15-25% du total)

**Cloud (AWS, GCP, Azure) :**
- GPU pour entraînement : 500-5000€/mois
- Stockage données : 100-500€/mois
- Compute inférence : 200-2000€/mois
- Networking : 100-500€/mois

**Exemple budget cloud annuel :**
- Petit projet : 15-30k€/an
- Projet moyen : 50-100k€/an
- Gros projet : 200-500k€/an

**On-premise :**
- Serveur GPU : 10-30k€ (investissement)
- Maintenance : 20% par an
- Électricité : 500-2000€/mois

### 3. Coûts API et Services (10-20% du total)

**APIs LLM (par million de tokens) :**
- GPT-4 : 30-60€
- GPT-3.5 : 1-2€
- Claude : 15-75€
- Open source (hébergé) : 0€ mais coûts infra

**Exemple coût mensuel chatbot :**
- 1000 conversations/jour
- 10 000 tokens/conversation
- 300M tokens/mois
- GPT-3.5 : ~600€/mois
- GPT-4 : ~15k€/mois (!)

**Services annexes :**
- Annotation données : 500-2000€/mois (si externalisé)
- MLOps plateforme : 200-1000€/mois
- Monitoring : 100-500€/mois

### 4. Coûts d'Intégration (10-15% du total)

**Développement connexion systèmes :**
- API vers applications métier : 10-30k€
- Sécurité et authentification : 5-15k€
- Tests d'intégration : 5-10k€

**Coûts cachés :**
- Temps des équipes IT internes
- Refactoring systèmes existants
- Documentation et formation

### 5. Coûts Accompagnement (5-10% du total)

**Formation utilisateurs :**
- Création contenu : 5-10k€
- Sessions de formation : 2-5k€
- Support niveau 1 : 1-2k€/mois

**Change management :**
- Communication interne
- Gestion des résistances
- Collecte feedback

### 6. Coûts de Maintenance (20-30% annuel)

**Opérationnel :**
- Monitoring quotidien : 0.2 ETP
- Support utilisateurs : 0.3-0.5 ETP
- Correction bugs : 0.2 ETP

**Évolutif :**
- Ré-entraînement modèle : 1-2 semaines/trimestre
- Amélioration continue : 10-20% du temps équipe
- Mise à jour dépendances : mensuel

**Budget maintenance annuel :**
Prévoir **20-30% du coût initial du projet** chaque année.

---

## Exemple Budget Complet

### Projet Chatbot SAV - Estimation Réaliste

**Phase 1 - POC (3 mois) : 45k€**
- Équipe : 35k€
- Infra cloud : 3k€
- API OpenAI : 5k€
- Outils : 2k€

**Phase 2 - Pilote (4 mois) : 85k€**
- Équipe : 60k€
- Infra cloud : 10k€
- API OpenAI : 10k€
- Intégration : 5k€

**Phase 3 - Production (setup) : 50k€**
- Équipe : 30k€
- Infra cloud : 10k€
- Sécurité/conformité : 10k€

**Année 1 Total : 180k€**
- Développement : 180k€
- Maintenance Y1 : inclus

**Maintenance annuelle (Y2+) : 45k€/an**
- Équipe (0.5 ETP) : 30k€
- Infra : 10k€
- API : 5k€

**Coût total sur 3 ans : ~270k€**

---

## Calculer le ROI

### Formule de Base

```
ROI = (Gains totaux - Coûts totaux) / Coûts totaux × 100
```

### Identifier les Gains

**Gains directs :**
- Temps économisé × coût horaire
- Reduction ETP × salaire chargé
- Volume traité en plus × marge

**Gains indirects :**
- Satisfaction client améliorée → rétention
- Erreurs évitées → coûts évités
- Rapidité → avantage compétitif

### Exemple Calcul ROI Chatbot SAV

**Situation avant :**
- 10 agents SAV
- 500 tickets/jour
- 50 tickets/agent/jour
- Coût : 10 × 50k€ = 500k€/an

**Avec IA :**
- Chatbot gère 70% des tickets automatiquement
- 350 tickets/jour automatisés
- 150 tickets/jour pour agents
- Besoin : 3 agents au lieu de 10

**Calcul gains :**
- Économie : 7 agents × 50k€ = 350k€/an
- Amélioration satisfaction : +10% rétention → 50k€/an
- **Total gains : 400k€/an**

**Calcul coûts :**
- Année 1 : 180k€
- Année 2 : 45k€
- Année 3 : 45k€
- **Total 3 ans : 270k€**

**ROI sur 3 ans :**
```
Gains 3 ans = 400k × 3 = 1200k€
Coûts 3 ans = 270k€
ROI = (1200k - 270k) / 270k × 100 = 344%
```

**Payback period :**
```
180k€ / 400k€ = 0.45 ans = ~5.5 mois
```

---

## Grille de Décision ROI

| ROI Projeté | Payback | Décision |
|-------------|---------|----------|
| > 200% | < 12 mois | GO sans hésiter |
| 100-200% | 12-18 mois | GO si stratégique |
| 50-100% | 18-24 mois | GO avec prudence |
| 0-50% | > 24 mois | Reconsidérer |
| < 0% | Never | NO GO |

---

## Pièges à Éviter

### 1. Sous-estimer les Coûts de Données

**Réalité :**
- 40-60% du temps projet = travail sur les données
- Annotation manuelle coûteuse
- Nettoyage long et fastidieux

**Solution :**
Multiplier l'estimation data par 2.

### 2. Ignorer les Coûts d'Échelle

**Problème :**
- POC avec 100 requêtes/jour
- Production avec 10 000 requêtes/jour
- Coûts × 100, pas × 10 (pas linéaire)

**Solution :**
Tester les coûts à différentes échelles avant la prod.

### 3. Oublier la Maintenance

**Erreur classique :**
"Le modèle est déployé, c'est fini !"

**Réalité :**
- Data drift nécessite ré-entraînement
- Bugs en prod à corriger
- Utilisateurs à supporter
- Infra à maintenir

**Budget :** 20-30% du coût initial par an.

### 4. Sur-estimer les Gains

**Piège :**
Calculer les gains sur 100% d'adoption immédiate.

**Réalité :**
- Adoption progressive (30% → 60% → 80%)
- Résistances au changement
- Cas limites non gérés par l'IA

**Solution :**
Appliquer un facteur de prudence de 0.6-0.7 sur les gains projetés.

### 5. Ignorer le Coût d'Opportunité

**Question :**
"Que feraient ces développeurs s'ils n'étaient pas sur ce projet IA ?"

**Réflexion :**
- Autres projets à plus forte valeur ?
- Maintenance de l'existant ?
- Innovation sur le cœur de métier ?

---

## Template Business Case

```markdown
# Business Case - [Nom Projet]

## Résumé Exécutif
Projet IA pour [objectif] avec ROI projeté de X% sur 3 ans.

## Problème Business
- Douleur : [description]
- Impact actuel : [coût/perte en €]
- Personnes affectées : [nombre/rôle]

## Solution Proposée
- Type d'IA : [ML, NLP, GenAI...]
- Approche : [description technique simplifiée]
- Différenciation : pourquoi l'IA vs autre solution

## Budget Détaillé

### Phase POC (X mois)
- Équipe : X€
- Infrastructure : X€
- Outils/Services : X€
- **Total POC : X€**

### Phase Pilote (X mois)
- Équipe : X€
- Infrastructure : X€
- Intégration : X€
- **Total Pilote : X€**

### Production (Année 1)
- Équipe : X€
- Infrastructure : X€
- API/Services : X€
- **Total Y1 : X€**

### Maintenance (Annuel, Y2+)
- **Total Maintenance : X€/an**

### Total sur 3 ans : X€

## Bénéfices Attendus

### Gains Directs
- Économie temps : X ETP × Xk€ = X€/an
- Volume additionnel : X× plus = X€/an
- Erreurs évitées : X cas × X€ = X€/an

### Gains Indirects
- Satisfaction client : +X% → X€
- Time to market : -X jours → X€
- Avantage compétitif : [qualitatif]

### Total Gains : X€/an

## Calcul ROI

| Année | Coûts | Gains | Cumulé |
|-------|-------|-------|--------|
| Y1 | X€ | X€ | -X€ |
| Y2 | X€ | X€ | +X€ |
| Y3 | X€ | X€ | +X€ |

**ROI sur 3 ans : X%**
**Payback : X mois**

## Risques

1. **Technique** : [risque] → mitigation
2. **Adoption** : [risque] → mitigation
3. **Budget** : [risque] → mitigation

## Recommandation

GO / NO-GO avec justification.

## Prochaines Étapes

1. [Action] - [Date] - [Responsable]
2. [Action] - [Date] - [Responsable]
```

---

## Ressources

- [Lancer un projet IA](lancer-projet-ia.md) - Phases détaillées
- [Framework évaluation](../evaluation/framework-3-niveaux.md) - Mesurer le succès
- [Template business case](../templates/business-case-ia.md) - Document complet

---

*Budget et ROI projet IA | Dernière MAJ : Nov 2025*
