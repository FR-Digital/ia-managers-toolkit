# Checklist Pré-Projet IA

## À quoi sert cette checklist ?

Cette checklist vous permet de vérifier que vous avez tous les éléments nécessaires **avant** de lancer un projet IA.

**Utilisation :** 30 minutes, avant toute décision d'investissement.

**Score minimal requis :** 70% pour lancer un POC.

---

## ✓ Phase 1 : Clarté Business

### Objectif

- [ ] **L'objectif est formulé en termes business (€, temps, qualité)**
  - 📝 *Pourquoi :* Un objectif technique ne permet pas de mesurer le ROI
  - 👤 *Responsable :* Sponsor projet
  - ⏱️ *Temps :* 1h

- [ ] **Le KPI de succès est défini et mesurable**
  - 📝 *Exemple :* "Réduire temps de traitement de 48h à 4h"
  - 👤 *Responsable :* Manager métier

- [ ] **Le seuil minimum acceptable est fixé**
  - 📝 *Exemple :* "En dessous de 60% de précision, on arrête"
  - 👤 *Responsable :* Sponsor + Manager

### Cas d'usage

- [ ] **Le cas d'usage est spécifique (pas "faire de l'IA dans le SAV")**
  - 📝 *Bon exemple :* "Automatiser les 100 questions les plus fréquentes du SAV email"
  - ⚠️ *Piège :* Les cas d'usage vagues ne se concrétisent jamais

- [ ] **Le problème existe vraiment (validé avec utilisateurs finaux)**
  - 📝 *Comment :* 5 interviews utilisateurs minimum
  - 👤 *Responsable :* Chef de projet

- [ ] **Il existe une solution manuelle aujourd'hui (à améliorer)**
  - 📝 *Pourquoi :* Si ça n'existe pas manuellement, l'IA ne le fera pas mieux
  - ⚠️ *Piège :* Vouloir créer quelque chose de totalement nouveau avec l'IA

- [ ] **Le volume justifie l'automatisation (>100 cas/mois)**
  - 📝 *Seuil rentabilité :* < 100 cas/mois = trop faible pour ROI positif
  - 💰 *Impact :* Volume x10 = ROI x5 généralement

---

## ✓ Phase 2 : Données

### Disponibilité

- [ ] **Les données existent et sont accessibles**
  - ⚠️ *Piège :* Les données "dans un vieux système" = souvent inexploitables
  - 📝 *Vérification :* Extraire un échantillon de 100 lignes et vérifier qualité

- [ ] **Volume suffisant (minimum 1000 exemples pour IA supervisée)**
  - 📝 *Détail par type :*
    - Classification : 1000+ exemples (100+ par catégorie)
    - Génération de texte (RAG) : 100+ documents de référence
    - Détection d'anomalies : 10 000+ exemples normaux + 100+ anomalies

- [ ] **Qualité correcte (< 20% d'erreurs)**
  - 📝 *Comment mesurer :* Vérifier manuellement 100 exemples aléatoires
  - ⚠️ *Seuil critique :* > 30% d'erreurs = nettoyage obligatoire (coût x2-3)

- [ ] **Données représentatives (couvrent tous les cas d'usage)**
  - 📝 *Exemple :* Si chatbot SAV, avoir des exemples de TOUTES les catégories de produits
  - ⚠️ *Piège :* Données biaisées = IA qui ne marche que sur 50% des cas

### Conformité

- [ ] **Conformité RGPD vérifiée**
  - 👤 *Responsable :* DPO (Data Protection Officer)
  - 📝 *Action :* Créer fiche registre de traitement
  - 💰 *Coût non-conformité :* Amendes jusqu'à 20M€ ou 4% CA

- [ ] **Données sensibles identifiées**
  - 📝 *Types :* Données santé, données bancaires, données RH, données enfants
  - ⚠️ *Impact :* Si données sensibles → contraintes AI Act (audit obligatoire)

- [ ] **Plan d'anonymisation si nécessaire**
  - 📝 *Techniques :* Pseudonymisation, suppression identifiants, agrégation
  - 💰 *Coût :* 5-20k€ pour anonymisation professionnelle

- [ ] **Droits d'utilisation clarifiés (données tierces)**
  - 📝 *Question :* Avons-nous le droit contractuel d'utiliser ces données pour entraîner une IA ?
  - ⚠️ *Piège :* Données clients/partenaires peuvent avoir restrictions contractuelles

---

## ✓ Phase 3 : Équipe & Compétences

- [ ] **Sponsor projet identifié (niveau COMEX/CODIR)**
  - 📝 *Pourquoi :* Nécessaire pour débloquer budget et arbitrer
  - ⏱️ *Engagement :* Min 2h/mois de disponibilité

- [ ] **Manager métier dédié (min 20% de son temps)**
  - 📝 *Rôle :* Définir les besoins, valider les résultats, former les utilisateurs
  - ⚠️ *Piège :* Projet 100% tech sans pilotage métier = échec garanti

- [ ] **Accès à compétence IA (interne ou externe)**
  - 📝 *Options :*
    - Interne : Data scientist (100k€/an)
    - Externe : Prestataire (400-800€/jour)
    - Hybride : Freelance + Formation interne
  - 💰 *Budget POC :* 20-50k€ (prestataire externe)

- [ ] **Utilisateurs finaux disponibles pour tests (min 5 personnes)**
  - 📝 *Engagement :* 2-4h/mois pendant phase POC
  - 📝 *Profils :* Utilisateurs "normaux" (pas que des experts)

---

## ✓ Phase 4 : Budget & Timeline

- [ ] **Budget POC validé (20-50k€)**
  - 📝 *Détail :*
    - Développement : 15-35k€
    - API/Infrastructure : 2-5k€
    - Données (nettoyage) : 3-10k€
  - 👤 *Validation :* DAF + Sponsor

- [ ] **Budget production estimé (100-300k€)**
  - 📝 *Détail :*
    - Développement/Industrialisation : 50-150k€
    - Infrastructure : 20-80k€
    - Formation & Change management : 10-30k€
    - Audit conformité (RGPD/AI Act) : 5-20k€
    - Contingence (20%) : 20-60k€

- [ ] **Timeline réaliste définie (min 6 mois idée→prod)**
  - 📝 *Phases :*
    - Cadrage : 1 mois
    - POC : 2-3 mois
    - Évaluation & go/no-go : 2 semaines
    - Production : 3-6 mois
  - ⚠️ *Piège :* Timeline < 4 mois = risque fort d'échec

- [ ] **Plan de financement (opex vs capex) clarifié**
  - 📝 *Options :*
    - CAPEX : Développement interne, serveurs on-premise
    - OPEX : API externes (OpenAI, Claude), cloud
  - 👤 *Décision :* DAF

---

## ✓ Phase 5 : Risques

- [ ] **Risque technique évalué (complexité IA)**
  - 📝 *Niveaux :*
    - 🟢 Faible : RAG simple, classification basique (succès 80%)
    - 🟡 Moyen : NLP complexe, détection anomalies (succès 60%)
    - 🔴 Élevé : IA générative sur mesure, vision par ordinateur (succès 40%)
  - 💡 *Conseil :* Commencez par risque faible pour apprendre

- [ ] **Risque métier évalué (impact si échec)**
  - 📝 *Questions :*
    - Que se passe-t-il si l'IA se trompe ?
    - Impact financier d'une erreur ?
    - Impact réputation ?
  - ⚠️ *Exemple à risque :* Diagnostic médical, décision de crédit, contrôle qualité sécurité

- [ ] **Risque réputationnel évalué (erreurs IA visibles?)**
  - 📝 *Scénarios :*
    - Client : Chatbot donne info fausse → insatisfaction
    - Public : IA discriminatoire → bad buzz médiatique
  - 💡 *Mitigation :* Toujours garder humain dans la boucle pour décisions importantes

- [ ] **Plan B défini (que fait-on si ça ne marche pas?)**
  - 📝 *Options :*
    - Pivot vers use case plus simple
    - Solution non-IA (automatisation classique)
    - Abandon projet
  - 💰 *Budget Plan B :* Prévoir 10-20% du budget POC

---

## 📊 Score de Maturité

**Calculez votre score :**

**Total items cochés :** _____ / 25

**Interprétation :**

- **0-30% cochés (0-7 items) :** 🔴 **STOP** - Ne lancez pas le projet maintenant
  - Action : Identifier les gaps les plus critiques
  - Timeline : Revenir dans 2-3 mois après avoir comblé les lacunes

- **30-70% cochés (8-17 items) :** 🟡 **ATTENTION** - Travail préparatoire nécessaire (2-4 semaines)
  - Action : Compléter les items manquants en priorité
  - Focus : Données + Budget (items bloquants)

- **70-100% cochés (18-25 items) :** 🟢 **GO** - Vous pouvez lancer un POC
  - Action : Créer la fiche projet formelle
  - Timeline : Démarrage POC dans 2-4 semaines

---

## 💡 Tips

**Conseil 1 :** Faites cette checklist avec TOUTES les parties prenantes (IT + métier + data + finance)
- Pourquoi : Éviter les mauvaises surprises ("ah on n'a pas les données !")
- Comment : Atelier 2h avec 5-8 personnes clés

**Conseil 2 :** Si < 50% cochés, revenez dans 1 mois après avoir travaillé les gaps
- Ne forcez pas le lancement d'un projet non mature
- Coût échec > coût attente

**Conseil 3 :** Les items "Données" et "Budget" sont bloquants - priorisez-les
- Pas de données = pas d'IA possible
- Pas de budget = projet mort-né

**Conseil 4 :** Impliquez votre DPO dès le début (RGPD/AI Act)
- Coût conformité post-développement = x3-5 vs anticipé
- Délai audit externe : 4-8 semaines (prévoir dans planning)

---

## 📥 Versions téléchargeables

- 📄 **PDF imprimable** : [checklist-pre-projet.pdf](../../templates/pdf/checklist-pre-projet.pdf)
- 📊 **Excel avec scoring auto** : [checklist-pre-projet.xlsx](../../templates/excel/checklist-pre-projet.xlsx)
- 🔗 **Google Sheets** : *(à venir)*

---

## 📖 Pour Aller Plus Loin

Après avoir complété cette checklist :

**Si score > 70% :**
- 👉 Lisez le [Guide complet "Lancer un projet IA"](../guides/01-lancer-projet-ia.md)
- 👉 Utilisez le [Template fiche projet](../../templates/markdown/project-charter.md)
- 👉 Calculez votre ROI avec le [Calculateur Excel](../../templates/excel/roi-calculator.xlsx)

**Si score 30-70% :**
- 👉 Identifiez les 3-5 items les plus critiques manquants
- 👉 Créez un plan d'action 2-4 semaines pour les combler
- 👉 Refaites la checklist dans 1 mois

**Si score < 30% :**
- 👉 Le projet n'est pas mature - focalisez sur autre chose
- 👉 Ou formez-vous d'abord : [ia-glossaire-business-fr](https://github.com/FR-Digital/ia-glossaire-business-fr)

---

## Exemples de Projets Selon Score

### Exemple 1 : Score 85% → GO ✅

**Contexte :** PME retail, chatbot SAV
- ✅ Objectif clair : -40% temps réponse SAV
- ✅ 50k emails historiques (données ok)
- ✅ Budget 45k€ POC validé
- ✅ Manager SAV dédié 30% temps
- ✅ Prestataire IA identifié
- ⚠️ Pas encore RGPD validé (à faire semaine 1)

**Décision :** Lancement POC dans 2 semaines

---

### Exemple 2 : Score 45% → ATTENTION ⚠️

**Contexte :** Industrie, maintenance prédictive
- ✅ Objectif clair : -30% pannes machines
- ❌ Données dispersées dans 3 systèmes (extraction 6 semaines)
- ❌ Budget non validé (en attente COMEX)
- ✅ Sponsor identifié
- ❌ Pas de compétence IA (ni interne ni externe)

**Décision :** Travail prépa 2 mois (extraction données + validation budget)

---

### Exemple 3 : Score 20% → STOP 🔴

**Contexte :** Startup, "on veut faire de l'IA"
- ❌ Objectif vague ("améliorer l'expérience client")
- ❌ Pas de données
- ❌ Pas de budget défini
- ❌ Pas de sponsor
- ❌ Pas de compétence IA

**Décision :** Formation équipe + définition use case précis (retour dans 3 mois)

---

## Questions Fréquentes

**Q : Peut-on lancer avec un score de 60% ?**
R : Techniquement oui, mais risque d'échec élevé (60%). Mieux vaut attendre 1 mois et monter à 75%.

**Q : Quel est l'item le plus bloquant ?**
R : Les données. Sans données de qualité, aucune IA ne marchera. Si cet item n'est pas coché, STOP immédiatement.

**Q : Faut-il 100% pour lancer ?**
R : Non. 75-80% suffit. Certains items se règlent pendant le POC (ex: utilisateurs beta testeurs).

**Q : Combien de temps pour compléter la checklist ?**
R : 30 min si vous avez toutes les infos. 1-2 semaines si vous devez investiguer (données, budget, etc.).

---

**Besoin d'aide pour compléter cette checklist ?**

Ouvrez une [issue](https://github.com/FR-Digital/ia-managers-toolkit/issues) ou contactez-nous : contact@lafabriq.ai

---

*Dernière MAJ : Novembre 2025 | [Contribuer](../../CONTRIBUTING.md)*
