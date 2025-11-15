# Risques et Éthique de l'IA

> Identifier, évaluer et mitiger les risques d'un projet IA.

## Pourquoi C'est Critique

Un projet IA mal géré peut causer :
- **Pertes financières** (erreurs coûteuses, échec projet)
- **Dommages réputationnels** (biais discriminatoires, incidents publics)
- **Problèmes légaux** (non-conformité RGPD, décisions illégales)
- **Impact humain** (décisions injustes, perte d'emplois mal gérée)

**En tant que manager, vous êtes responsable** de ces risques.

---

## Catégories de Risques

### 1. Risques Techniques

#### Hallucinations (IA Générative)
**Définition :** L'IA invente des informations fausses avec confiance.

**Impact :**
- Conseils erronés aux clients
- Citations de lois inexistantes
- Chiffres inventés

**Mitigation :**
- Vérification humaine obligatoire pour décisions critiques
- Limiter aux tâches non-critiques
- Avertissement clair aux utilisateurs
- Utiliser RAG avec sources vérifiées

#### Biais Algorithmiques
**Définition :** L'IA reproduit/amplifie les biais présents dans les données.

**Exemples réels :**
- Recrutement discriminant les femmes (Amazon)
- Reconnaissance faciale moins précise sur peaux foncées
- Scoring crédit défavorisant certaines zones

**Mitigation :**
- Audit des données d'entraînement
- Tests d'équité sur différents groupes
- Monitoring continu des décisions
- Diversité dans l'équipe de développement

#### Data Drift
**Définition :** Les données changent, le modèle devient obsolète.

**Impact :**
- Performance qui se dégrade
- Prédictions de moins en moins fiables
- Décisions basées sur des patterns anciens

**Mitigation :**
- Monitoring automatique de la distribution des données
- Alertes si drift détecté
- Processus de ré-entraînement planifié
- Comparaison régulière avec la réalité terrain

#### Sécurité et Attaques
**Types d'attaques :**
- **Prompt injection :** Manipuler l'IA avec des instructions malveillantes
- **Data poisoning :** Corrompre les données d'entraînement
- **Model inversion :** Extraire des données sensibles du modèle
- **Adversarial attacks :** Tromper l'IA avec des inputs malicieux

**Mitigation :**
- Validation des inputs
- Sandboxing des requêtes
- Monitoring des comportements anormaux
- Tests de pénétration réguliers

---

### 2. Risques Business

#### Adoption Échec
**Causes :**
- Résistance au changement
- UX inadaptée
- Confiance insuffisante
- Formation insuffisante

**Impact :**
- ROI négatif
- Budget gaspillé
- Moral équipe affecté

**Mitigation :**
- Change management dès le début
- Impliquer les utilisateurs dans le design
- Formation et support robustes
- Quick wins pour démontrer la valeur

#### Dépendance Fournisseur (Vendor Lock-in)
**Problème :**
- API propriétaire indisponible = votre service down
- Prix qui augmentent sans alternative
- Politique d'utilisation qui change

**Mitigation :**
- Architecture abstraite (pas de dépendance directe)
- Plan B avec fournisseur alternatif
- Considérer l'open source
- Clauses contractuelles de sortie

#### Coûts Incontrôlés
**Scénarios :**
- Usage API qui explose
- Besoins en infra sous-estimés
- Maintenance plus lourde que prévu

**Mitigation :**
- Limites de budget avec alertes
- Quotas d'utilisation
- Revue mensuelle des coûts
- Optimisation continue

---

### 3. Risques Légaux et Conformité

#### RGPD et Protection des Données
**Obligations :**
- Base légale pour le traitement
- Information des personnes concernées
- Droit d'accès et de suppression
- Privacy by design

**Questions clés :**
- "Quelles données personnelles l'IA utilise-t-elle ?"
- "Les personnes sont-elles informées ?"
- "Peut-on exercer le droit à l'oubli ?"
- "Les données sont-elles pseudonymisées/anonymisées ?"

**Mitigation :**
- Data Protection Impact Assessment (DPIA)
- Consultation DPO dès le cadrage
- Minimisation des données
- Documentation complète

#### Droit à l'Explication (AI Act EU)
**Exigence :**
Pour certaines décisions (crédit, recrutement, etc.), l'IA doit être explicable.

**Impact :**
- "Boîte noire" peut être illégale
- Obligation de justifier les décisions
- Responsabilité en cas d'erreur

**Mitigation :**
- Utiliser des modèles explicables (quand possible)
- Documenter la logique de décision
- Prévoir supervision humaine
- Tenir registre des décisions

#### Responsabilité en Cas d'Erreur
**Question :**
Si l'IA fait une erreur qui cause un préjudice, qui est responsable ?

**Réponse :**
- L'entreprise reste responsable
- L'IA n'a pas de personnalité juridique
- Le manager doit avoir mis les garde-fous

**Mitigation :**
- Assurance cyber/erreur pro
- Limitation du scope décisionnel de l'IA
- Supervision humaine documentée
- Procédures de recours claires

---

### 4. Risques Éthiques

#### Remplacement d'Emplois
**Considérations :**
- Impact social sur les équipes
- Responsabilité employeur
- Communication transparente

**Approche responsable :**
- Anticiper et communiquer
- Plan de reconversion/formation
- L'IA augmente plutôt que remplace
- Accompagnement humain du changement

#### Transparence et Confiance
**Problème :**
Les utilisateurs ne savent pas qu'ils interagissent avec une IA.

**Bonnes pratiques :**
- Indiquer clairement que c'est une IA
- Expliquer les limites
- Permettre l'escalade vers un humain
- Ne pas tromper (ex: faux profil humain)

#### Équité et Justice
**Questions à se poser :**
- "Notre IA traite-t-elle tout le monde équitablement ?"
- "Y a-t-il des groupes désavantagés ?"
- "Les décisions sont-elles justes ?"

**Actions :**
- Tests d'équité par groupe démographique
- Audit externe si décisions sensibles
- Feedback loop pour détecter les injustices
- Processus de contestation disponible

---

## Matrice des Risques

### Comment Évaluer

**Probabilité :**
- Très probable (>70%)
- Probable (40-70%)
- Possible (10-40%)
- Rare (<10%)

**Impact :**
- Critique (arrêt activité, dommage légal majeur)
- Sévère (perte financière importante, réputation)
- Modéré (inefficacité, coût supplémentaire)
- Mineur (inconvénient, facilement corrigé)

### Exemple Projet Chatbot

| Risque | Probabilité | Impact | Score | Mitigation |
|--------|-------------|--------|-------|------------|
| Hallucination sur conseil juridique | Probable | Critique | ROUGE | Interdire les conseils juridiques |
| Biais dans les réponses | Possible | Sévère | ORANGE | Tests d'équité + monitoring |
| Données client mal protégées | Possible | Critique | ROUGE | Audit sécurité + chiffrement |
| Adoption faible | Probable | Modéré | JAUNE | Formation + quick wins |
| Coûts API explosent | Possible | Modéré | JAUNE | Quotas + monitoring |
| Indisponibilité service | Rare | Sévère | JAUNE | Fallback + SLA fournisseur |

**Code couleur :**
- ROUGE : Action immédiate requise
- ORANGE : Plan de mitigation à définir
- JAUNE : Surveillance et mesures préventives
- VERT : Acceptable, monitoring basique

---

## Check-List Éthique

### Avant le Projet
- [ ] DPIA (Data Protection Impact Assessment) réalisé
- [ ] DPO consulté
- [ ] Risques identifiés et documentés
- [ ] Parties prenantes informées
- [ ] Budget mitigation prévu

### Pendant le Développement
- [ ] Données d'entraînement auditées pour biais
- [ ] Tests d'équité sur différents groupes
- [ ] Sécurité du système validée
- [ ] Documentation des décisions techniques
- [ ] Privacy by design appliqué

### Avant la Production
- [ ] Supervision humaine en place
- [ ] Processus d'escalade défini
- [ ] Communication utilisateurs prête
- [ ] Monitoring biais/drift configuré
- [ ] Plan de rollback testé

### En Production
- [ ] Monitoring continu des métriques d'équité
- [ ] Feedback utilisateurs analysé
- [ ] Incidents documentés
- [ ] Revue trimestrielle des risques
- [ ] Audit externe annuel (si sensible)

---

## Gouvernance IA Responsable

### Comité Éthique IA
**Composition suggérée :**
- Sponsor exécutif
- Responsable projet
- DPO / Juridique
- RH
- Représentant utilisateurs
- Expert externe (optionnel)

**Rôle :**
- Valider les projets sensibles
- Arbitrer les dilemmes éthiques
- Auditer les systèmes en production
- Recommander les meilleures pratiques

### Processus de Validation

```
Nouveau Projet IA
       │
       ▼
Classification du Risque
       │
       ├─ Faible Risque ────> Validation Manager
       │
       ├─ Risque Modéré ────> Validation Manager + DPO
       │
       └─ Risque Élevé ─────> Comité Éthique IA
```

**Critères Risque Élevé :**
- Décisions affectant des personnes (recrutement, crédit)
- Données sensibles (santé, finance, RH)
- Impact juridique potentiel
- Large audience (>1000 utilisateurs)
- Pas de supervision humaine prévue

---

## Conformité AI Act (Union Européenne)

### Classification des Systèmes IA

**Risque Inacceptable (Interdit) :**
- Scoring social
- Manipulation comportementale
- Exploitation des vulnérabilités
- Identification biométrique en temps réel (sauf exceptions)

**Risque Élevé (Régulation forte) :**
- Recrutement et gestion RH
- Accès aux services essentiels (crédit, assurance)
- Justice et immigration
- Infrastructures critiques

**Risque Limité (Transparence) :**
- Chatbots
- Systèmes de recommandation
- Génération de contenu

**Risque Minimal (Pas de contrainte) :**
- Filtres spam
- Jeux vidéo
- Assistants personnels basiques

### Obligations Risque Élevé
- Système de gestion des risques
- Gouvernance des données
- Documentation technique complète
- Transparence et information
- Supervision humaine
- Robustesse et cybersécurité
- Enregistrement et traçabilité

---

## Ressources

- [Framework évaluation](../evaluation/framework-3-niveaux.md) - Évaluer objectivement
- [Budget et ROI](budget-et-roi.md) - Coûts de mitigation
- [Quand arrêter](../evaluation/quand-arreter-projet.md) - Savoir dire stop

**Ressources externes :**
- [AI Act EU](https://artificialintelligenceact.eu/)
- [Guidelines CNIL](https://www.cnil.fr/fr/intelligence-artificielle)
- [Responsible AI Practices (Google)](https://ai.google/responsibility/responsible-ai-practices/)

---

*Risques et éthique IA | Dernière MAJ : Nov 2025*
