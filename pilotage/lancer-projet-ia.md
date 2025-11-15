# Lancer un Projet IA : Guide Complet

> De l'idée à la production en évitant les pièges classiques.

## Les 4 Phases d'un Projet IA

```
PHASE 1: CADRAGE (1-2 mois)
    │
    ▼
PHASE 2: POC - Proof of Concept (2-3 mois)
    │
    ▼
PHASE 3: PILOTE (3-6 mois)
    │
    ▼
PHASE 4: PRODUCTION (ongoing)
```

---

## Phase 1 : Cadrage (1-2 mois)

### Objectif
Valider que le projet IA est **pertinent, faisable et rentable**.

### Étape 1.1 : Identifier le Problème Business

**Questions essentielles :**
- Quel problème précis résolvons-nous ?
- Qui souffre de ce problème aujourd'hui ?
- Quel est l'impact financier actuel ?
- Comment le problème est-il géré actuellement ?

**Red flags :**
- "On veut faire de l'IA" sans problème précis
- Problème mal défini ou trop vaste
- Pas d'impact mesurable

**Template Problème :**
```
En tant que [rôle],
je dois [action actuelle],
ce qui prend [temps/coût],
et cause [douleur].
Si on automatisait [partie],
on gagnerait [bénéfice mesurable].
```

**Exemple :**
```
En tant qu'agent SAV,
je dois répondre à 200 emails/jour,
ce qui prend 8h de travail,
et cause des délais de réponse de 48h.
Si on automatisait les réponses aux FAQ (70% du volume),
on réduirait le temps de traitement de 5h et les délais de réponse à 12h.
```

### Étape 1.2 : Valider la Faisabilité Technique

**Checklist données :**
- [ ] Données disponibles en volume suffisant (>1000 exemples)
- [ ] Données accessibles (pas bloquées par IT/légal)
- [ ] Données représentatives du problème
- [ ] Qualité acceptable (pas trop de bruit)
- [ ] Conformité RGPD vérifiée

**Checklist compétences :**
- [ ] Équipe data disponible ou recrutement prévu
- [ ] Compétences en ML/IA suffisantes
- [ ] Infra cloud ou on-premise disponible
- [ ] Budget alloué

**Questions à l'équipe tech :**
- "Ce problème est-il solvable par l'IA ?"
- "Quelles données avons-nous ?"
- "Quel type d'IA serait adapté ?"
- "Estimation grossière de la difficulté ?"

### Étape 1.3 : Calculer le ROI Potentiel

**Formule simple :**
```
ROI = (Bénéfices annuels - Coûts annuels) / Coûts annuels × 100
```

**Estimation des coûts :**
- POC : 30-80k€ (3 mois, 2 ETP)
- Pilote : 50-150k€ (6 mois)
- Production année 1 : 100-300k€
- Maintenance annuelle : 20-30% du coût initial

**Estimation des bénéfices :**
- Temps économisé × coût horaire
- Revenue additionnel
- Erreurs évitées
- Satisfaction client améliorée

**Seuil minimum :**
ROI projeté > 100% à 18 mois, sinon reconsidérer.

### Livrables Phase 1
- [ ] Business case validé
- [ ] Sponsor exécutif identifié
- [ ] Budget alloué (POC minimum)
- [ ] Équipe constituée
- [ ] Timeline défini
- [ ] Critères de succès mesurables

---

## Phase 2 : POC - Proof of Concept (2-3 mois)

### Objectif
Prouver que **techniquement, ça peut marcher**.

### Scope du POC

**Ce qu'il doit prouver :**
- L'IA peut résoudre le problème technique
- La précision est dans la cible (>70-80%)
- Les données sont exploitables
- L'approche choisie est viable

**Ce qu'il NE DOIT PAS faire :**
- Être production-ready
- Gérer tous les cas edge
- Avoir une belle UI
- Être scalable

**Règle d'or :**
POC = la solution la plus simple qui prouve le concept.

### Métriques du POC

| Métrique | Seuil Minimum | Pour Continuer |
|----------|---------------|----------------|
| Précision | > 70% | > 80% |
| Recall (si critique) | > 60% | > 75% |
| Temps réponse | < 10s | < 5s |
| Couverture cas | > 50% | > 70% |

### Déroulement Type

**Semaine 1-2 : Setup**
- Collecter et nettoyer les données
- Setup environnement de développement
- Baseline simple (règles ou modèle basique)

**Semaine 3-6 : Développement**
- Expérimenter différentes approches
- Itérer sur le modèle
- Tester sur jeu de validation

**Semaine 7-8 : Évaluation**
- Tests sur données réelles (pas vues à l'entraînement)
- Analyse des erreurs
- Documentation résultats

**Semaine 9-10 : Décision**
- Présentation résultats
- Recommandation : GO/NO-GO/PIVOT
- Si GO : planning phase pilote

### Red Flags POC

- "Ça marche sur mon poste" sans tests réels
- Précision mesurée sur données d'entraînement
- Aucune analyse des cas d'erreur
- Dérive de scope (trop de features)
- Retards répétés sans justification

### Livrables Phase 2
- [ ] Modèle fonctionnel (même brouillon)
- [ ] Métriques de performance documentées
- [ ] Analyse des erreurs et limites
- [ ] Estimation coût/effort phase pilote
- [ ] Recommandation GO/NO-GO argumentée

---

## Phase 3 : Pilote (3-6 mois)

### Objectif
Valider que **les utilisateurs l'utilisent et que ça crée de la valeur**.

### Différences POC vs Pilote

| Aspect | POC | Pilote |
|--------|-----|--------|
| Utilisateurs | Équipe projet | 20-50 vrais utilisateurs |
| Données | Échantillon | Données production |
| Qualité code | Prototype | Code propre, testé |
| Monitoring | Basique | Dashboard complet |
| Support | Aucun | Équipe dédiée |
| Durée | 2-3 mois | 3-6 mois |

### Déploiement Progressif

**Stratégie "canary" :**
1. **Semaine 1-2 :** 5 utilisateurs early adopters
2. **Semaine 3-4 :** 20 utilisateurs (après corrections)
3. **Mois 2 :** 50 utilisateurs
4. **Mois 3+ :** Tous les utilisateurs pilotes

**À chaque palier :**
- Collecter feedback
- Corriger bugs critiques
- Améliorer modèle si nécessaire
- Valider métriques

### Métriques à Suivre

**Techniques :**
- Performance modèle en production
- Latence réelle
- Taux d'erreur
- Utilisation ressources

**Adoption :**
- % utilisateurs actifs
- Fréquence d'utilisation
- Taux d'abandon
- Satisfaction (NPS, rating)

**Business :**
- Temps économisé
- Volume traité
- Qualité output
- Indicateurs métier spécifiques

### Accompagnement du Changement

**Formation utilisateurs :**
- Session d'onboarding (1-2h)
- Documentation utilisateur simple
- Vidéos tutoriels
- FAQ des questions courantes

**Support :**
- Canal dédié (Slack, Teams)
- Permanence équipe projet
- Collecte systématique du feedback
- Response time < 4h

**Communication :**
- Kick-off projet avec sponsors
- Update hebdomadaire aux stakeholders
- Célébration des quick wins
- Transparence sur les difficultés

### Critères de Passage en Prod

**GO si :**
- [ ] Adoption > 60% des utilisateurs pilotes
- [ ] Satisfaction > 4/5
- [ ] Performance stable (pas de dégradation)
- [ ] ROI positif mesurable ou très probable
- [ ] Pas d'incident critique non résolu
- [ ] Plan de support production défini
- [ ] Documentation complète

**NO-GO si :**
- [ ] Adoption < 30% malgré accompagnement
- [ ] Satisfaction < 3/5
- [ ] Performance dégradante
- [ ] Risques légaux/éthiques identifiés
- [ ] Coûts > prévisions de > 50%

### Livrables Phase 3
- [ ] Rapport de pilote complet
- [ ] Métriques d'adoption et satisfaction
- [ ] Liste bugs corrigés et restants
- [ ] Estimation ROI révisée
- [ ] Plan de déploiement production
- [ ] Plan de support et maintenance
- [ ] Décision GO/NO-GO formelle

---

## Phase 4 : Production (Ongoing)

### Objectif
**Délivrer de la valeur durablement** à l'ensemble des utilisateurs.

### Déploiement

**Stratégie recommandée : Rolling deployment**
- 10% des utilisateurs semaine 1
- 25% semaine 2
- 50% semaine 3
- 100% semaine 4

**Avec monitoring renforcé** à chaque palier.

### Monitoring en Production

**Dashboard temps réel :**
- Nombre de requêtes
- Taux d'erreur
- Latence (p50, p95, p99)
- Alertes automatiques si seuils dépassés

**Suivi modèle :**
- Data drift detection
- Performance degradation
- Distribution des prédictions

**Business metrics :**
- ROI cumulé
- KPIs métier
- Satisfaction utilisateur

### Maintenance Continue

**Hebdomadaire :**
- Review des alertes
- Analyse tickets support
- Performance check

**Mensuelle :**
- Rapport performance
- Analyse erreurs récurrentes
- Feedback utilisateurs

**Trimestrielle :**
- Évaluation data drift
- Décision ré-entraînement
- Review ROI
- Roadmap améliorations

### Gouvernance

**Rôles clés :**
- **Product Owner IA :** Priorise les améliorations
- **ML Engineer :** Maintient le modèle
- **Data Engineer :** Gère les pipelines data
- **Support :** Accompagne les utilisateurs

**Comités :**
- Hebdomadaire : Opérationnel (équipe technique)
- Mensuel : Tactique (PO + tech + métier)
- Trimestriel : Stratégique (direction + sponsors)

---

## Pièges Classiques à Éviter

### 1. "On va tout faire d'un coup"
**Solution :** Commencer petit, itérer, prouver la valeur, puis étendre.

### 2. "Les données, on verra plus tard"
**Solution :** Valider la disponibilité et qualité des données en phase 1.

### 3. "L'équipe tech gère tout seule"
**Solution :** Impliquer les métiers dès le départ, ils connaissent le problème.

### 4. "Pas besoin de former les utilisateurs"
**Solution :** Budget et temps pour l'accompagnement du changement.

### 5. "Une fois en prod, c'est fini"
**Solution :** Prévoir 20-30% du budget pour la maintenance annuelle.

---

## Timeline Réaliste

**Projet IA typique :**
- Cadrage : 1-2 mois
- POC : 2-3 mois
- Pilote : 3-6 mois
- Production : 1-3 mois
- **Total : 9-15 mois avant impact business**

**ROI positif :** 12-18 mois après le début du projet.

---

## Ressources

- [Business case template](../templates/business-case-ia.md)
- [Budget et ROI](budget-et-roi.md)
- [Framework évaluation](../evaluation/framework-3-niveaux.md)
- [Questions équipe tech](../evaluation/questions-equipe-tech.md)

---

*Guide lancement projet IA | Dernière MAJ : Nov 2025*
