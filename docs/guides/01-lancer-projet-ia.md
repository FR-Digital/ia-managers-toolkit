# Comment lancer un projet IA : Le guide complet pour managers

## TL;DR

En 3 phrases : **Définir un objectif business mesurable, vérifier la faisabilité (données + budget), lancer un POC limité puis scaler si succès.** Ce guide vous évite les pièges classiques qui font échouer 70% des projets IA. Résultat : ROI mesurable en 3-6 mois.

---

## Pourquoi ce guide

- **Impact business :** Réduire les risques d'échec de 70% à 30%
- **Coût de l'inaction :** Retard concurrentiel, opportunités perdues (coût moyen : 200k€/an pour une ETI)
- **Opportunité :** ROI moyen 300% sur projets bien lancés (source : McKinsey 2024)

---

## Les 5 étapes essentielles

### Étape 1 : Définir l'objectif business (pas technique)

**Ce qu'il faut faire :**
- Formuler le problème en termes business (€, temps, qualité)
- Identifier le KPI de succès (mesurable)
- Définir le "minimum acceptable" (seuil go/no-go)

**Qui le fait :** Sponsor projet + Manager métier
**Temps :** 2-4h
**Livrable :** Fiche objectif (🚧 template à venir)

**💡 Conseil :** Commencez par "Nous voulons réduire/augmenter [QUOI] de [COMBIEN]"

⚠️ **Piège à éviter :** Partir d'une technologie ("on veut du ChatGPT") plutôt qu'un besoin

**Exemple concret :**
- ❌ **Mauvais :** "On veut faire de l'IA dans le SAV"
- ✅ **Bon :** "On veut réduire le temps de réponse SAV de 48h à 4h pour augmenter la satisfaction client de 60% à 85%"

**Framework de formulation :**

```
Notre objectif : [VERBE ACTION] + [MÉTRIQUE] de [VALEUR ACTUELLE] à [VALEUR CIBLE]

Impact attendu :
- Gain financier : [X]€/an
- Gain temps : [Y] heures/mois
- Gain qualité : [Z]% d'amélioration

Seuil minimum acceptable : [VALEUR PLANCHER]
```

**Exemple rempli :**

```
Notre objectif : Réduire le temps de traitement des demandes SAV de 48h à 4h

Impact attendu :
- Gain financier : 180k€/an (2.5 ETP redéployés)
- Gain temps : 500 heures/mois
- Gain qualité : +20 points de satisfaction client

Seuil minimum acceptable : Temps < 8h ET satisfaction > 75%
```

---

### Étape 2 : Vérifier la faisabilité (checklist)

**Ce qu'il faut faire :**
- ✓ Vérifier que les **données existent** et sont accessibles
- ✓ Vérifier que le **budget** est réaliste (POC : 20-50k€, Production : 100-300k€)
- ✓ Vérifier que vous avez accès à la **compétence IA** (interne ou externe)
- ✓ Vérifier que le **ROI** est atteignable (payback < 18 mois)

**Qui le fait :** Chef de projet + DSI + DAF
**Temps :** 1 semaine
**Livrable :** [Checklist pré-projet](../checklists/pre-projet.md) complétée

**💡 Conseil :** Si moins de 70% des items sont cochés, reportez le projet de 2-3 mois

⚠️ **Piège à éviter :** Sous-estimer les besoins en données (qualité > quantité)

**Checklist rapide (version courte) :**

**Données :**
- [ ] Les données existent (pas "on va les créer")
- [ ] Volume suffisant (min 1000 exemples pour IA supervisée)
- [ ] Qualité correcte (< 20% d'erreurs)
- [ ] Accessibles légalement (RGPD ok)

**Budget :**
- [ ] Budget POC validé (20-50k€)
- [ ] Budget production estimé (100-300k€)
- [ ] ROI calculé (🚧 calculateur à venir)
- [ ] Payback < 18 mois

**Équipe :**
- [ ] Sponsor projet identifié (niveau COMEX/CODIR)
- [ ] Manager métier dédié (min 20% temps)
- [ ] Accès compétence IA (interne ou externe)
- [ ] Utilisateurs finaux disponibles pour tests

**Risques :**
- [ ] Risque technique évalué (complexité)
- [ ] Risque métier évalué (impact échec)
- [ ] Plan B défini (que fait-on si ça échoue ?)

**Score de maturité :**
- **< 50% :** 🔴 STOP - Ne lancez pas
- **50-80% :** 🟡 ATTENTION - Travail préparatoire nécessaire
- **> 80% :** 🟢 GO - Vous pouvez lancer un POC

---

### Étape 3 : Lancer un POC limité (Proof of Concept)

**Ce qu'il faut faire :**
- Définir un **périmètre réduit** (10-20% du cas d'usage complet)
- Fixer une **durée limitée** (2-3 mois max)
- Définir des **critères de succès clairs** (métriques mesurables)
- Tester avec de **vrais utilisateurs** (pas juste l'équipe projet)

**Qui le fait :** Équipe projet complète (métier + tech)
**Temps :** 2-3 mois
**Budget :** 20-50k€
**Livrable :** POC fonctionnel + rapport d'évaluation

**💡 Conseil :** Commencez par le cas d'usage le plus simple ET le plus fréquent

⚠️ **Piège à éviter :** Vouloir couvrir 100% des cas dès le POC (vous n'y arriverez jamais)

**Exemple de périmètre POC :**

**Cas complet :** Chatbot SAV pour 5000 requêtes/mois
**POC limité :**
- 100 questions les plus fréquentes (20% du volume)
- 1 canal (email uniquement, pas téléphone)
- 1 catégorie de produits
- Test avec 20% du trafic réel

**Critères de succès POC :**
- ✓ 70% de réponses automatisées (sans intervention humaine)
- ✓ 80% de satisfaction utilisateur (thumbs up/down)
- ✓ Temps de réponse < 5 minutes
- ✓ 0 erreur grave (informations fausses dangereuses)

**Décision go/no-go après POC :**
- **> 80% critères atteints :** 🟢 GO Production (scaling)
- **60-80% critères atteints :** 🟡 AMÉLIORER (itération POC)
- **< 60% critères atteints :** 🔴 STOP (revoir approche ou abandonner)

---

### Étape 4 : Évaluer et décider (go/no-go production)

**Ce qu'il faut faire :**
- Mesurer les **métriques de succès** définies au POC
- Calculer le **ROI réel** (vs ROI estimé)
- Recueillir le **feedback utilisateurs** (qualitatif)
- Identifier les **risques production** (scalabilité, coûts, maintenance)

**Qui le fait :** Sponsor + Chef de projet + DAF
**Temps :** 1 semaine
**Livrable :** Grille go/no-go (🚧 à venir) + Décision formelle

**💡 Conseil :** Impliquez les utilisateurs finaux dans la décision (pas que le COMEX)

⚠️ **Piège à éviter :** Continuer un projet qui ne marche pas par "peur d'avoir perdu l'investissement POC"

**Grille de décision :**

| Critère | Poids | Score /10 | Note pondérée |
|---------|-------|-----------|---------------|
| **Métriques techniques atteintes** | 25% | 8 | 2.0 |
| **Satisfaction utilisateurs** | 25% | 9 | 2.25 |
| **ROI projeté > 200%** | 30% | 7 | 2.1 |
| **Risques maîtrisés** | 20% | 6 | 1.2 |
| **TOTAL** | 100% | - | **7.55/10** |

**Décision selon score :**
- **> 8/10 :** 🟢 GO Production immédiat
- **6-8/10 :** 🟡 GO Production avec ajustements
- **4-6/10 :** 🟠 Nouvelle itération POC nécessaire
- **< 4/10 :** 🔴 STOP - Abandon ou pivot majeur

---

### Étape 5 : Déployer en production (scaling)

**Ce qu'il faut faire :**
- **Scaler progressivement** (20% → 50% → 100% du trafic)
- **Monitorer en continu** (dashboard métriques temps réel)
- **Former les équipes** (utilisateurs + support)
- **Prévoir la maintenance** (budget récurrent, équipe dédiée)

**Qui le fait :** Équipe projet + DSI + Métier
**Temps :** 3-6 mois
**Budget :** 100-300k€ (selon complexité)
**Livrable :** Solution en production + Documentation + Plan de maintenance

**💡 Conseil :** Gardez toujours un "circuit de secours" manuel pendant les 3 premiers mois

⚠️ **Piège à éviter :** Passer de 0 à 100% du trafic d'un coup (risque d'incident majeur)

**Plan de déploiement progressif :**

**Mois 1-2 : 20% du trafic**
- Objectif : Valider stabilité technique
- Monitoring : Toutes les heures
- Rollback possible : Oui (immédiat)
- Support : Équipe projet en alerte 24/7

**Mois 3-4 : 50% du trafic**
- Objectif : Valider scalabilité
- Monitoring : Toutes les 4 heures
- Rollback possible : Oui (en 1 heure)
- Support : Équipe support formée

**Mois 5-6 : 100% du trafic**
- Objectif : Production complète
- Monitoring : Quotidien + alertes automatiques
- Rollback possible : Oui (procédure documentée)
- Support : Run courant (équipe métier)

**Métriques à monitorer en production :**

**Techniques :**
- Temps de réponse (p50, p95, p99)
- Taux d'erreur (< 1%)
- Disponibilité (> 99.5%)
- Coût par requête

**Business :**
- Taux d'utilisation (% utilisateurs actifs)
- Satisfaction utilisateurs (NPS)
- ROI réel vs projeté
- Gain temps/coût mesuré

**Exemple de dashboard (métriques clés) :**

```
┌─────────────────────────────────────────┐
│ DASHBOARD PRODUCTION - Chatbot SAV     │
├─────────────────────────────────────────┤
│ Technique                               │
│  • Temps réponse : 2.3s (cible < 5s) ✓ │
│  • Taux erreur : 0.4% (cible < 1%) ✓   │
│  • Disponibilité : 99.8% (cible 99.5%) ✓│
│  • Coût/requête : 0.02€ (budget 0.05€) ✓│
├─────────────────────────────────────────┤
│ Business                                │
│  • Utilisation : 68% requêtes auto ✓   │
│  • Satisfaction : 79% (cible 75%) ✓    │
│  • Gain temps : 520h/mois (cible 500h) ✓│
│  • ROI : 71% (cible 50%) ✓             │
└─────────────────────────────────────────┘
```

---

## Checklist complète

Pour ne rien oublier, utilisez la [checklist pré-projet complète](../checklists/pre-projet.md).

---

## Templates prêts à l'emploi

- 🚧 Fiche objectif projet - Document de cadrage *(à venir)*
- 🚧 Calculateur ROI - Excel avec formules automatiques *(à venir)*
- 🚧 Pitch COMEX - Présentation pour convaincre *(à venir)*

---

## Exemples réels

Consultez nos cas d'usage documentés avec ROI réel :
- [Chatbot SAV Retail](../../examples/use-cases/retail-chatbot.md) - ROI 71%, payback 7 mois
- 🚧 Maintenance prédictive Industrie - ROI 240% *(à venir)*
- 🚧 Détection fraude Finance - ROI 450% *(à venir)*

---

## FAQ

**Q : Combien de temps pour lancer un projet IA ?**
R : De l'idée au POC : 2-3 mois. Du POC à la production : 3-6 mois. Total : 6-9 mois en moyenne.

**Q : Quel budget prévoir ?**
R : POC : 20-50k€. Production : 100-300k€ selon complexité. Maintenance : 20-50k€/an.

**Q : Peut-on faire sans équipe data science ?**
R : Oui, en utilisant des APIs (OpenAI, Claude, etc.) et en faisant appel à un prestataire externe pour le POC. Mais vous aurez besoin d'un chef de projet qui comprend l'IA.

**Q : Comment convaincre le COMEX ?**
R : Parlez ROI, pas technologie. Montrez des cas d'usage similaires dans votre secteur. Proposez un POC limité (risque contrôlé). Un template pitch COMEX sera bientôt disponible.

**Q : Que faire si le POC échoue ?**
R : Analysez pourquoi (données ? complexité ? mauvais use case ?). Si c'est réparable, itérez. Sinon, arrêtez et pivotez sur un autre use case. Un POC qui échoue n'est PAS un échec si vous en tirez des leçons.

**Q : Faut-il développer in-house ou utiliser des APIs ?**
R : Pour démarrer : API (plus simple, moins cher). Pour scaler : dépend du volume et de la sensibilité des données. Un guide détaillé API vs In-House sera bientôt disponible.

**Q : Comment gérer la conformité RGPD et AI Act ?**
R : Impliquez votre DPO dès l'étape 1. Documentez l'usage des données. Prévoyez un registre de traitement. Pour l'AI Act : si votre IA est "à haut risque" (RH, santé, finance), prévoyez un audit externe. Budget : 5-20k€.

---

## Sources & Références

Ce guide s'appuie sur :
- [GitHub AI Playbook](https://resources.github.com/enterprise/ai-powered-workforce-playbook/)
- [Hands-on ML Checklist](https://github.com/ageron/handson-ml/blob/master/ml-project-checklist.md)
- Retours d'expérience de 50+ projets IA en ETI françaises (2023-2024)

---

## Pour Aller Plus Loin

- 🚧 Sélectionner le bon use case - Éviter les fausses bonnes idées *(à venir)*
- 🚧 Constituer l'équipe - Qui recruter et comment *(à venir)*
- 🚧 Mesurer le ROI - Framework complet avec exemples *(à venir)*

---

**Besoin d'aide ?** Ouvrez une [issue](https://github.com/FR-Digital/ia-managers-toolkit/issues) ou contactez-nous : contact@lafabriq.ai

---

*Dernière mise à jour : Novembre 2025 | [Contribuer](../../CONTRIBUTING.md)*
