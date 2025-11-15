# Checklist Pré-Production IA

> 50 points de vérification avant de déployer une IA en production.

---

## Instructions

- Cochez chaque item une fois validé ✅
- Documentez les exceptions avec justification
- Cette checklist doit être signée par le responsable projet et le sponsor
- Conserver comme preuve de due diligence

**Projet :** [Nom]
**Date :** [JJ/MM/AAAA]
**Responsable :** [Nom]

---

## 1. Performance Technique (10 items)

### Qualité du Modèle

- [ ] **1.1** Précision globale > [X]% sur jeu de test indépendant
- [ ] **1.2** Métriques spécifiques validées (recall, precision, F1) selon le cas d'usage
- [ ] **1.3** Pas de dégradation significative entre dev et staging
- [ ] **1.4** Tests sur cas limites (edge cases) effectués et documentés
- [ ] **1.5** Taux d'erreur critique < [X]% (hallucinations graves, etc.)

### Performance Système

- [ ] **1.6** Temps de réponse moyen < [X] secondes (p50)
- [ ] **1.7** Temps de réponse p95 < [X] secondes
- [ ] **1.8** Test de charge réalisé (X requêtes/seconde supportées)
- [ ] **1.9** Disponibilité > 99% sur période de test (1 semaine minimum)
- [ ] **1.10** Consommation ressources (CPU, RAM, GPU) dans les limites

---

## 2. Données et Modèle (8 items)

### Gestion des Données

- [ ] **2.1** Pipeline de données documenté et automatisé
- [ ] **2.2** Qualité des données en production validée (pas de données corrompues)
- [ ] **2.3** Processus de refresh des données défini si applicable
- [ ] **2.4** Backup des données en place

### Gestion du Modèle

- [ ] **2.5** Modèle versionné et reproductible
- [ ] **2.6** Procédure de rollback testée (retour version précédente en < 15 min)
- [ ] **2.7** Processus de ré-entraînement documenté
- [ ] **2.8** Modèle stocké de manière sécurisée (accès restreint)

---

## 3. Intégration et Infrastructure (8 items)

### Intégration Systèmes

- [ ] **3.1** APIs documentées (Swagger/OpenAPI ou équivalent)
- [ ] **3.2** Tests d'intégration avec systèmes existants passés
- [ ] **3.3** Authentification et autorisation configurées
- [ ] **3.4** Gestion des erreurs API définie (codes retour, messages)

### Infrastructure

- [ ] **3.5** Environnement de production séparé du dev/staging
- [ ] **3.6** Auto-scaling configuré si nécessaire
- [ ] **3.7** Redondance en place (pas de single point of failure)
- [ ] **3.8** Plan de disaster recovery documenté

---

## 4. Sécurité (8 items)

### Protection des Données

- [ ] **4.1** Données chiffrées at-rest et in-transit (TLS 1.2+)
- [ ] **4.2** Accès aux données restreint (principe du moindre privilège)
- [ ] **4.3** Logs d'accès activés et monitorés
- [ ] **4.4** Pas de données sensibles dans les logs (PII, mots de passe)

### Sécurité Applicative

- [ ] **4.5** Validation des inputs (protection prompt injection si LLM)
- [ ] **4.6** Rate limiting configuré (protection DDoS)
- [ ] **4.7** Audit de sécurité réalisé (ou planifié post-prod)
- [ ] **4.8** Secrets gérés via vault (pas de credentials en dur)

---

## 5. Monitoring et Observabilité (6 items)

### Monitoring Technique

- [ ] **5.1** Dashboard de monitoring en place (latence, erreurs, volume)
- [ ] **5.2** Alertes configurées (seuils définis pour incidents critiques)
- [ ] **5.3** Logs centralisés et consultables
- [ ] **5.4** Métriques business trackées (pas seulement techniques)

### Monitoring ML Spécifique

- [ ] **5.5** Détection de data drift configurée
- [ ] **5.6** Suivi de la distribution des prédictions (détecter les anomalies)

---

## 6. Conformité et Légal (6 items)

### RGPD et Protection Données

- [ ] **6.1** DPIA (Data Protection Impact Assessment) réalisé si requis
- [ ] **6.2** Base légale du traitement documentée
- [ ] **6.3** Information des personnes concernées faite (privacy notice)
- [ ] **6.4** Processus de droit d'accès/suppression en place

### Éthique et Biais

- [ ] **6.5** Tests d'équité réalisés (biais par groupe démographique)
- [ ] **6.6** Documentation sur les limitations de l'IA accessible

---

## 7. Support et Maintenance (6 items)

### Documentation

- [ ] **7.1** Documentation technique complète et à jour
- [ ] **7.2** Guide utilisateur rédigé
- [ ] **7.3** Runbook opérationnel (procédures incidents) documenté
- [ ] **7.4** FAQ support préparée

### Organisation Support

- [ ] **7.5** Équipe de support identifiée (qui répond si problème ?)
- [ ] **7.6** Procédure d'escalade définie (L1 → L2 → L3)

---

## 8. Communication et Change Management (4 items)

### Communication

- [ ] **8.1** Utilisateurs informés du lancement et formés
- [ ] **8.2** Communication claire que c'est une IA (pas de tromperie)
- [ ] **8.3** Canal de feedback utilisateurs en place
- [ ] **8.4** Plan de communication en cas d'incident préparé

---

## 9. Business Readiness (4 items)

### Validation Business

- [ ] **9.1** Sponsor a validé le GO production
- [ ] **9.2** KPIs business définis et baseline mesurée
- [ ] **9.3** Critères de succès à 1 mois / 3 mois documentés
- [ ] **9.4** Budget maintenance Y1 approuvé

---

## Synthèse

### Résumé Validation

| Section | Items Validés | Total | % |
|---------|---------------|-------|---|
| Performance Technique | [ ]/10 | 10 | [ ]% |
| Données et Modèle | [ ]/8 | 8 | [ ]% |
| Intégration et Infra | [ ]/8 | 8 | [ ]% |
| Sécurité | [ ]/8 | 8 | [ ]% |
| Monitoring | [ ]/6 | 6 | [ ]% |
| Conformité | [ ]/6 | 6 | [ ]% |
| Support | [ ]/6 | 6 | [ ]% |
| Communication | [ ]/4 | 4 | [ ]% |
| Business | [ ]/4 | 4 | [ ]% |
| **TOTAL** | **[ ]/50** | **50** | **[ ]%** |

### Décision

**Score minimum pour GO :** 90% (45/50 items validés)
**Aucun item critique non validé** (items 1.5, 4.1-4.4, 6.1-6.4)

**Score obtenu : [ ]/50 ([ ]%)**

### Exceptions Acceptées

*Lister ici les items non validés avec justification et plan de remédiation*

| Item | Raison Exception | Plan de Remédiation | Date Cible | Responsable |
|------|------------------|---------------------|------------|-------------|
| [X.X] | [Justification] | [Action] | [Date] | [Nom] |

---

## Signatures

**GO PRODUCTION : ☐ APPROUVÉ / ☐ REFUSÉ**

| Rôle | Nom | Signature | Date |
|------|-----|-----------|------|
| Responsable Projet | [Nom] | _________ | [Date] |
| Sponsor | [Nom] | _________ | [Date] |
| Responsable Technique | [Nom] | _________ | [Date] |
| DPO (si applicable) | [Nom] | _________ | [Date] |
| Sécurité (si applicable) | [Nom] | _________ | [Date] |

---

## Post-Déploiement

### Actions J+1 à J+7

- [ ] Monitoring renforcé des métriques
- [ ] Revue quotidienne des alertes
- [ ] Collecte feedback utilisateurs
- [ ] Standby équipe technique

### Revue J+30

- [ ] Analyse KPIs vs objectifs
- [ ] Rapport performance première période
- [ ] Décision sur ajustements nécessaires

---

*Template Checklist Pré-Production | v1.0 | Nov 2025*
