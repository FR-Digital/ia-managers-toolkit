# Cas d'Usage : Chatbot SAV pour Enseigne Retail

## Contexte

**Entreprise :** Enseigne retail 50 magasins (ETI, 200M€ CA)
**Secteur :** Distribution spécialisée (électroménager)
**Problématique :** 5000 emails SAV/mois, temps réponse 48h, satisfaction 62%
**Objectif :** Automatiser 70% des requêtes simples, réduire temps à 4h

---

## Solution Mise en Place

### Type d'IA

**Chatbot avec RAG (Génération Augmentée par Récupération)**

**Pourquoi ce choix :**
- Besoin de réponses basées sur documentation produits (fiches techniques, FAQ, garanties)
- Volume moyen (5000 requêtes/mois) → API externe rentable
- Nécessité d'avoir réponses fiables (pas d'hallucinations)

**Alternatives envisagées et rejetées :**
- ❌ Chatbot à règles : Trop rigide, 40% d'échec sur requêtes variées
- ❌ IA générative pure (sans RAG) : Invente des infos fausses sur garanties
- ❌ Fine-tuning GPT : Coût prohibitif (80k€) vs RAG (35k€)

### Données Utilisées

**Sources :**
- 50 000 emails SAV historiques (2 ans)
- FAQ produits : 300 questions/réponses
- Documentation technique : 150 fiches produits
- Conditions générales de vente : 1 document (20 pages)

**Préparation des données :**
- Nettoyage : 3 semaines (anonymisation clients, suppression doublons)
- Annotation : 500 emails classifiés manuellement (types de demandes)
- Vectorisation : 2 jours (indexation documents pour RAG)

**Coût préparation :** 12 000€ (prestataire externe)

### Équipe Projet

**Composition :**
- 1 Chef de projet métier (Responsable SAV) - 50% temps - 6 mois
- 1 Data scientist (prestataire externe) - 100% temps - 3 mois
- 1 Développeur backend (interne) - 50% temps - 4 mois
- 5 conseillers SAV (beta testeurs) - 10% temps - 2 mois

**Budget RH :**
- Interne : 30k€ (temps passé valorisé)
- Externe : 35k€ (prestataire data science)

---

## Timeline

### Mois 1-2 : Cadrage + Préparation Données

**Activités :**
- Ateliers définition besoins (3 jours)
- Extraction et nettoyage données (3 semaines)
- Sélection des 100 questions prioritaires (POC)
- Choix technologique (OpenAI API + Pinecone pour vecteurs)

**Livrables :**
- Fiche projet validée
- Données nettoyées et vectorisées
- Architecture technique documentée

### Mois 3-4 : POC (Proof of Concept)

**Périmètre POC :**
- 100 questions les plus fréquentes (couvrent 60% du volume)
- 1 canal : Email uniquement
- 1 catégorie produits : Réfrigérateurs (20% du catalogue)
- Test avec 20% du trafic réel (1000 emails/mois)

**Critères de succès POC :**
- ✅ 70% réponses automatisées (sans intervention humaine)
- ✅ 80% satisfaction (thumbs up/down)
- ✅ Temps < 5 min
- ✅ 0 erreur grave (info fausse sur garantie)

**Résultats POC :**
- ✅ 68% automatisation (proche objectif)
- ✅ 82% satisfaction (objectif dépassé)
- ✅ Temps réponse : 2 min (largement sous objectif)
- ✅ 0 erreur grave (guardrails efficaces)

**Décision :** GO Production

### Mois 5-6 : Beta Test (20% → 50% Trafic)

**Objectifs :**
- Étendre à toutes catégories produits
- Passer de 100 à 300 questions couvertes
- Tester scalabilité technique

**Résultats :**
- Automatisation stable : 65-70%
- Satisfaction : 79% (léger recul lié aux nouvelles catégories)
- Coûts API : 450€/mois (dans budget prévu)

**Ajustements :**
- Ajout 50 Q/R sur catégories moins bien couvertes (électroménager cuisson)
- Amélioration guardrails (détection questions hors périmètre)

### Mois 7 : Déploiement Production (100% Trafic)

**Formation équipe SAV :**
- 2 sessions 2h (utilisation outil, escalade cas complexes)
- Documentation procédures

**Monitoring :**
- Dashboard temps réel (métriques techniques + business)
- Alertes automatiques (baisse satisfaction, hausse coûts)

---

## Budget

### POC (Mois 1-4)

| Poste | Montant |
|-------|---------|
| Conseil/Stratégie | 10 000€ |
| Développement (prestataire) | 25 000€ |
| Préparation données | 12 000€ |
| Infra/API (4 mois tests) | 2 000€ |
| Formation équipe | 3 000€ |
| **TOTAL POC** | **52 000€** |

### Production Année 1 (Mois 5-12)

| Poste | Montant |
|-------|---------|
| API LLM (OpenAI) | 30 000€ |
| Infra cloud (Pinecone + hébergement) | 8 000€ |
| Maintenance corrective | 15 000€ |
| Amélioration continue (nouveaux produits) | 7 000€ |
| **TOTAL Production An 1** | **60 000€** |

### Récurrent Année 2+

| Poste | Montant/an |
|-------|---------|
| API LLM | 30 000€ |
| Infra cloud | 8 000€ |
| Maintenance | 20 000€ |
| **TOTAL Année 2+** | **58 000€/an** |

---

## Résultats (6 Mois Post-Déploiement)

### Métriques Techniques

| Métrique | Objectif | Résultat | Status |
|----------|----------|----------|--------|
| Taux automatisation | 70% | 68% | ✅ |
| Temps de réponse | < 5 min | 2.3 min | ✅ |
| Disponibilité | 99% | 99.7% | ✅ |
| Coût par requête | < 0.10€ | 0.06€ | ✅ |

### Métriques Business

| Métrique | Avant IA | Après IA | Évolution |
|----------|----------|----------|-----------|
| Temps réponse moyen | 48h | 4h | **-91%** |
| Satisfaction client | 62% | 79% | **+17pts** |
| Emails traités/conseiller/jour | 25 | 40 | **+60%** |
| ETP conseillers SAV | 8 | 5.5 | **-2.5 ETP** |

### Impact Business

**Gains mesurés :**
- **Économies RH :** 2.5 ETP × 72 000€ = 180 000€/an
- **Amélioration satisfaction :** +17 points NPS → estimé +2% fidélisation = 400k€ CA préservé
- **Productivité conseillers :** Temps libéré sur cas complexes → +15% résolution premier contact

**Gains qualitatifs :**
- Disponibilité 24/7 (vs 9h-18h avant)
- Traçabilité complète des échanges
- Détection automatique sujets récurrents (alerte qualité produit)

---

## ROI Détaillé

### Année 1

**Investissement :**
- POC : 52 000€
- Production (8 mois) : 40 000€
- **Total investi An 1 :** 92 000€

**Gains :**
- Économies RH (8 mois) : 120 000€
- **Total gains An 1 :** 120 000€

**ROI Année 1 :** (120k - 92k) / 92k = **+30%**
**Payback :** 7 mois

### Année 2

**Investissement :**
- Récurrent : 58 000€

**Gains :**
- Économies RH : 180 000€

**ROI Année 2 :** (180k - 58k) / 58k = **+210%**

### Année 3 (Projection)

**ROI cumulé sur 3 ans :** **+250%**
**NPV (Net Present Value) :** 280 000€

---

## Leçons Apprises

### ✅ Ce qui a marché

**1. Impliquer conseillers SAV dès le début**
- Résultat : Ownership, adoption naturelle
- Comment : 5 conseillers dans équipe beta test (phase POC)
- Impact : 0 résistance au changement (vs 30-40% habituellement)

**2. Commencer petit puis scaler**
- Résultat : Validation rapide, ajustements faciles
- Comment : 100 questions POC → 300 production
- Impact : Économie 20k€ vs développement "big bang"

**3. Mesurer satisfaction en continu**
- Résultat : Amélioration itérative ciblée
- Comment : Thumbs up/down après chaque réponse + sondage mensuel
- Impact : Identification rapide questions problématiques

**4. Guardrails stricts sur informations critiques**
- Résultat : 0 erreur sur garanties/prix
- Comment : Vérifications automatiques + template réponse forcé pour sujets sensibles
- Impact : Confiance clients préservée

### ⚠️ Difficultés Rencontrées

**1. Qualité données variable**
- Problème : 30% emails historiques mal classifiés ou incomplets
- Impact : +3 semaines nettoyage (non prévu)
- Solution : Prestataire externe spécialisé data cleaning
- Coût : +12k€ vs budget initial

**2. Résistance initiale équipe SAV**
- Problème : Peur de perdre emploi, "IA va nous remplacer"
- Impact : Frein adoption premiers tests
- Solution : Communication transparente (IA = assistant, pas remplacement) + garantie non-licenciement
- Résultat : Conseillers redéployés sur cas complexes (montée en compétence)

**3. Hallucinations IA sur produits nouveaux**
- Problème : Nouveaux produits (non dans base documentaire) → IA inventait specs
- Impact : 5 réponses fausses en beta test
- Solution : Guardrail "Je n'ai pas l'info, je transfère à un conseiller"
- Résultat : Taux transfert +10% mais 0 erreur grave

**4. Coûts API supérieurs à estimation**
- Problème : Requêtes plus longues que prévu (contexte RAG volumineux)
- Impact : +50% coût API vs prévision (450€/mois vs 300€)
- Solution : Optimisation prompts + cache réponses fréquentes
- Résultat : Retour à 380€/mois (vs 450€ initial)

---

## Questions Manager

### Q : Pourquoi pas un chatbot à règles (moins cher) ?

**R :** Testé en POC parallèle.

**Chatbot à règles :**
- Couverture : 40% requêtes (trop rigide)
- Satisfaction : 55% (frustration utilisateurs)
- Coût : 15k€ développement

**Chatbot IA (RAG) :**
- Couverture : 68% requêtes
- Satisfaction : 79%
- Coût : 35k€ développement

**Conclusion :** +20k€ investissement → +28 points couverture → ROI largement positif

---

### Q : Comment vous avez mesuré la satisfaction ?

**R :** 3 méthodes complémentaires :

1. **Thumbs up/down après chaque réponse**
   - Taux réponse : 30% utilisateurs
   - Résultat : 79% thumbs up

2. **Sondage mensuel clients**
   - Question : "Satisfait du SAV ?" (1-5)
   - Évolution : 3.1/5 → 4.0/5

3. **Taux d'escalade**
   - Métrique : % clients qui demandent "parler à un humain"
   - Résultat : 15% (objectif < 20%)

**Alerte qualité :** Si satisfaction < 70% → revue manuelle 100 derniers échanges

---

### Q : Et si le prestataire IA (OpenAI) augmente ses prix ?

**R :** Risque identifié, 3 mitigations :

1. **Contractualisation budget**
   - Plafond mensuel API : 600€ (alarme à 500€)
   - Si dépassement : throttling automatique

2. **Multi-provider**
   - Architecture compatible Claude/OpenAI/Mistral
   - Test migration : 2 jours (si besoin)

3. **Plan B in-house**
   - Si coûts API x3 → switch Mistral on-premise
   - ROI reste positif jusqu'à 1500€/mois API

---

### Q : Quid de la conformité RGPD ?

**R :** Validé avec DPO en amont :

**Mesures :**
- Anonymisation emails historiques (noms/adresses supprimés)
- Contrat DPA (Data Processing Agreement) avec OpenAI
- Données européennes → serveurs UE
- Conservation limitée : 30 jours conversations

**Coût conformité :** 5k€ (audit DPO externe)

**Risque résiduel :** Faible (pas de données ultra-sensibles)

---

### Q : Combien de temps pour voir le ROI ?

**R :** Payback en **7 mois** :

| Mois | Investissement cumulé | Gains cumulés | Net |
|------|----------------------|---------------|-----|
| M1-4 (POC) | 52k€ | 0€ | -52k€ |
| M5 | 59k€ | 15k€ | -44k€ |
| M6 | 66k€ | 30k€ | -36k€ |
| M7 | 73k€ | 45k€ | -28k€ |
| **M8** | **80k€** | **60k€** | **-20k€** |
| **M9** | **87k€** | **75k€** | **-12k€** |
| **M10** | **92k€** | **90k€** | **-2k€** |
| **M11** | **92k€** | **105k€** | **+13k€** ✅ |

**Note :** Gains progressifs car déploiement 20% → 50% → 100% trafic

---

## Prochaines Étapes (Roadmap An 2)

**Trimestre 1 :**
- [ ] Étendre à canal téléphone (voice bot)
- [ ] Budget : 30k€
- [ ] ROI attendu : +15% automatisation

**Trimestre 2 :**
- [ ] Proactivité (détection insatisfaction client → contact proactif)
- [ ] Budget : 20k€
- [ ] Impact : -5% taux churn

**Trimestre 3-4 :**
- [ ] Multi-langue (anglais, espagnol pour expansion EU)
- [ ] Budget : 25k€

---

## Contact

**Vous avez des questions sur ce cas d'usage ?**

- Email : contact@lafabriq.ai
- Issue GitHub : [ia-managers-toolkit/issues](https://github.com/FR-Digital/ia-managers-toolkit/issues)

**Vous voulez partager votre propre retour d'expérience ?**

Consultez [CONTRIBUTING.md](../../CONTRIBUTING.md)

---

## Ressources Complémentaires

- 📖 [Guide "Lancer un projet IA"](../../docs/guides/01-lancer-projet-ia.md)
- 📊 [Calculateur ROI](../../templates/excel/roi-calculator.xlsx)
- ✓ [Checklist pré-projet](../../docs/checklists/pre-projet.md)

---

*Dernière mise à jour : Novembre 2025*

**Note de confidentialité :** Cas réel anonymisé. Chiffres arrondis pour préserver confidentialité.
