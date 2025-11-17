# Critères Go/No-Go Production

> **Décider objectivement si votre IA est prête pour la production**

## Le Problème

Votre équipe dit "C'est prêt !" Mais comment en être sûr ? Cette matrice vous donne des critères objectifs pour prendre la décision.

---

## Matrice de Décision

### Les 3 Questions Fondamentales

Avant d'aller en production, répondez par OUI à ces 3 questions :

1. **Est-ce que ça marche ?** (Niveau 1 validé)
2. **Est-ce que c'est utilisé ?** (Niveau 2 validé)
3. **Est-ce que ça rapporte ?** (Niveau 3 positif ou prometteur)

---

## Critères Par Catégorie

### 🔴 Bloquants (NO-GO absolu)

Si UN SEUL de ces critères n'est pas rempli = **NO-GO**

| Critère | Seuil | Vérifié |
|---------|-------|---------|
| Précision Niveau 1 | > 80% | [ ] |
| Pas d'hallucinations critiques | 0 en test | [ ] |
| Sécurité des données | Audit passé | [ ] |
| Plan de rollback | Testé et documenté | [ ] |
| Responsable identifié | Nom + backup | [ ] |
| Budget maintenance | Approuvé | [ ] |

**Si un critère bloquant manque :** STOP. Réglez-le d'abord.

---

### 🟡 Importants (Risque accru si manquant)

Ces critères devraient être remplis. Si non, documentez le risque accepté.

| Critère | Seuil | Vérifié | Si non, risque |
|---------|-------|---------|----------------|
| Adoption beta | > 50% | [ ] | Rejet utilisateurs |
| Satisfaction | > 3.5/5 | [ ] | Frustration, abandon |
| Monitoring actif | Dashboard en place | [ ] | Problèmes non détectés |
| Documentation | Complète | [ ] | Maintenance difficile |
| Formation équipe | Réalisée | [ ] | Mauvaise utilisation |
| Tests de charge | Validés | [ ] | Pannes sous charge |

**Si critères importants manquent :** GO possible avec plan de mitigation documenté.

---

### 🟢 Souhaitables (Amélioration continue)

Idéalement remplis, mais pas bloquants.

| Critère | Seuil | Vérifié |
|---------|-------|---------|
| ROI calculé | Positif | [ ] |
| Précision | > 90% | [ ] |
| Satisfaction | > 4/5 | [ ] |
| Adoption | > 80% | [ ] |
| Cas limites | Documentés | [ ] |
| Amélioration continue | Processus défini | [ ] |

**Si critères souhaitables manquent :** GO OK, à améliorer post-lancement.

---

## Scénarios de Décision

### Scénario 1 : Feu Vert Total 🟢

**Situation :**
- Tous les bloquants ✅
- Tous les importants ✅
- La plupart des souhaitables ✅

**Décision : GO**

**Actions :**
- Déploiement confiant
- Communication positive
- Suivi standard (mensuel)

---

### Scénario 2 : Go Conditionnel 🟡

**Situation :**
- Tous les bloquants ✅
- 1-2 importants manquants
- Souhaitables partiels

**Décision : GO avec conditions**

**Conditions typiques :**
- Revue hebdomadaire (pas mensuelle)
- Monitoring renforcé
- Plan d'amélioration daté
- Périmètre limité (pilote élargi)

**Exemple :**
- "Satisfaction à 3.2/5 (sous le seuil de 3.5)"
- Décision : GO conditionnel avec objectif 3.5/5 en 6 semaines

---

### Scénario 3 : Attente Active 🟠

**Situation :**
- Tous les bloquants ✅
- Plusieurs importants manquants
- Doutes sur l'adoption

**Décision : ATTENDRE**

**Actions :**
- Identifier les manquants prioritaires
- Fixer deadline (2-4 semaines)
- Ressources dédiées pour corriger
- Re-évaluation planifiée

**Exemple :**
- "Monitoring pas encore en place"
- "Formation utilisateurs non faite"
- Décision : Attendre 2 semaines, refaire le go/no-go

---

### Scénario 4 : No-Go 🔴

**Situation :**
- Un ou plusieurs bloquants manquants
- OU risques majeurs non mitigés
- OU sponsor métier oppose son veto

**Décision : NO-GO**

**Actions :**
- Communiquer clairement les raisons
- Plan d'action corrective
- Nouvelle date de go/no-go
- Potentiel pivot ou arrêt du projet

**Exemple :**
- "Précision à 72% (sous 80%)"
- Décision : Retour en développement, minimum 1 mois

---

## Qui Décide ?

### RACI de la Décision

| Rôle | Responsabilité |
|------|----------------|
| **Product Owner** | **Décideur final** (Accountable) |
| **Tech Lead** | Valide critères techniques (Consulted) |
| **Responsable Sécurité** | Valide critères sécurité (Consulted) |
| **Sponsor Métier** | Valide l'intérêt business (Consulted) |
| **Utilisateurs Pilotes** | Donnent leur feedback (Informed) |
| **Direction** | Informée de la décision (Informed) |

### Règle d'Or

**Le Product Owner décide, MAIS :**
- Si le Tech Lead dit "risque technique majeur" → écouter attentivement
- Si la Sécurité dit "faille critique" → NO-GO obligatoire
- Si le Sponsor Métier retire son soutien → réévaluer le projet

---

## Template de Réunion Go/No-Go

### Participants Requis

- [ ] Product Owner (décideur)
- [ ] Tech Lead
- [ ] Représentant Métier
- [ ] Responsable Sécurité (si sensible)

### Ordre du Jour (1h)

1. **Rappel objectifs** (5 min)
   - Pourquoi ce projet ?
   - Critères de succès définis

2. **Revue des critères bloquants** (15 min)
   - Passer chaque critère
   - Evidence/preuve pour chacun

3. **Revue des critères importants** (15 min)
   - Status de chacun
   - Plan de mitigation si manquant

4. **Risques et préoccupations** (10 min)
   - Tour de table
   - Chacun exprime ses doutes

5. **Discussion** (10 min)
   - Débat ouvert
   - Arguments pour/contre

6. **Décision** (5 min)
   - Vote ou consensus
   - Conditions si GO conditionnel
   - Actions si NO-GO

### Documentation Obligatoire

À la fin de la réunion, documenter :
- Décision prise (GO/NO-GO/CONDITIONNEL)
- Raisons de la décision
- Conditions (si applicable)
- Prochaines étapes
- Date de réévaluation (si NO-GO)
- Signatures des présents

---

## Erreurs Courantes à Éviter

### ❌ "On verra bien en production"

**Problème :** Reporter les problèmes sur les utilisateurs réels.
**Solution :** Si vous n'êtes pas sûr, ce n'est pas prêt.

### ❌ "La direction veut que ce soit live"

**Problème :** Pression business sans considération technique.
**Solution :** Communiquer les risques clairement. Si la direction accepte le risque en connaissance de cause, documentez.

### ❌ "L'équipe a travaillé dur, il faut déployer"

**Problème :** Facteur émotionnel dans une décision technique.
**Solution :** Respectez les critères objectifs. Le travail n'est pas perdu, il sera déployé quand c'est prêt.

### ❌ "C'est juste pour un petit groupe"

**Problème :** Sous-estimer l'impact d'un bug en production.
**Solution :** Les critères s'appliquent même pour un pilote. Adaptez le niveau d'exigence mais gardez les bloquants.

### ❌ "On corrigera après"

**Problème :** Dette technique et perte de confiance.
**Solution :** Si c'est connu comme problème, corrigez AVANT. Les surprises post-lancement coûtent plus cher.

---

## Checklist de Sortie de Réunion

### Si GO

- [ ] Date de déploiement fixée
- [ ] Plan de communication validé
- [ ] Support prêt et informé
- [ ] Monitoring actif vérifié
- [ ] Première revue post-lancement planifiée (J+7)
- [ ] Success criteria rappelés

### Si NO-GO

- [ ] Raisons documentées clairement
- [ ] Plan d'action corrective défini
- [ ] Responsables assignés
- [ ] Deadline pour corrections
- [ ] Date de prochain go/no-go fixée
- [ ] Communication aux stakeholders préparée

### Si CONDITIONNEL

- [ ] Conditions listées précisément
- [ ] Métriques de suivi définies
- [ ] Revue rapprochée planifiée (hebdo)
- [ ] Critères de rollback définis
- [ ] Communication adaptée (pilote limité)
- [ ] Plan d'amélioration avec deadlines

---

## Questions Ultimes

Avant de donner le GO final, posez-vous :

1. "Dormirais-je tranquille si ça plante cette nuit ?"
2. "Suis-je à l'aise de défendre cette décision devant la direction ?"
3. "Les utilisateurs seront-ils satisfaits ou frustrés ?"
4. "Si un problème survient, savons-nous comment réagir ?"
5. "Cette IA améliore-t-elle vraiment la situation actuelle ?"

Si vous répondez NON à l'une de ces questions, reconsidérez.

---

*La meilleure décision est celle prise avec des données, pas sous pression.*
