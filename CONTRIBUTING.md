# Guide de Contribution

Merci de votre intérêt pour contribuer à **IA Managers Toolkit** !

Ce repo est une ressource communautaire pour aider les managers à piloter des projets IA. Vos contributions aident des centaines de managers chaque mois.

---

## Comment Contribuer

### 1. Partager un Retour d'Expérience (Cas d'Usage)

Vous avez lancé un projet IA ? Votre retour d'expérience est **extrêmement précieux** !

**Ce qu'on cherche :**
- Projets IA terminés (succès OU échecs instructifs)
- ROI mesuré (ou au moins estimé)
- Budget et timeline réels
- Leçons apprises concrètes

**Comment contribuer :**

1. **Fork** ce repo
2. Créez un fichier dans `examples/use-cases/` en suivant le template :
   - [Template cas d'usage](examples/use-cases/retail-chatbot.md) (utilisez comme modèle)
3. **Anonymisez** :
   - Nom entreprise (sauf si autorisation explicite)
   - Chiffres arrondis (ex: 47k€ → "environ 50k€")
   - Personnes (pas de noms)
4. Soumettez une **Pull Request**

**Sections obligatoires dans un cas d'usage :**
- Contexte (secteur, taille entreprise, problématique)
- Solution mise en place (type d'IA, données, équipe)
- Budget détaillé (POC + Production)
- Résultats mesurés (métriques + ROI)
- Leçons apprises (succès + difficultés)

**Bonus :** Si vous pouvez partager templates internes (anonymisés), c'est encore mieux !

---

### 2. Améliorer Guides & Checklists

**Types d'améliorations bienvenues :**

- ✅ **Corrections** : Fautes, liens cassés, informations obsolètes
- ✅ **Clarifications** : Rendre plus accessible, ajouter exemples
- ✅ **Mise à jour réglementaire** : RGPD, AI Act, normes ISO
- ✅ **Compléments** : Ajouter sections manquantes

**Comment faire :**

1. Identifiez le fichier à améliorer (dans `docs/guides/` ou `docs/checklists/`)
2. Fork + modifiez
3. Pull Request avec description claire de l'amélioration

**Règle d'or :** Gardez le ton **business-friendly** (pas de jargon technique non expliqué)

---

### 3. Créer de Nouveaux Templates

**Templates prioritaires (liste des besoins) :**

- [ ] Template PowerPoint "Pitch COMEX" (présentation projet IA)
- [ ] Excel "Calculateur ROI" (formules automatiques)
- [ ] Word "Cahier des charges IA" (pour appel d'offres prestataires)
- [ ] Excel "Budget POC vs Production" (prévisionnel)
- [ ] PowerPoint "Formation managers" (sensibilisation IA)

**Format attendu :**

- Fichiers natifs (Excel, PowerPoint, Word) + PDF
- Instructions d'utilisation (README dans dossier template)
- Exemple pré-rempli (avec données fictives)
- Compatible Office 2016+ ET LibreOffice

**Où les placer :**
- `templates/excel/` pour fichiers Excel
- `templates/powerpoint/` pour présentations
- `templates/markdown/` pour documents texte

---

### 4. Proposer de Nouveaux Guides

**Guides manquants (idées bienvenues) :**

- Guide "Sélectionner le bon use case IA"
- Guide "Constituer l'équipe projet IA"
- Guide "Communiquer aux stakeholders"
- Guide "Gérer les risques IA (biais, hallucinations)"
- Guide "Choisir entre API et développement interne"

**Structure recommandée pour un guide :**

```markdown
# Titre du Guide

## TL;DR (3 phrases)

## Pourquoi ce guide (impact business)

## Étapes détaillées (3-5 étapes)
- Avec exemples concrets
- Avec pièges à éviter
- Avec conseils pratiques

## FAQ

## Pour aller plus loin (liens)
```

**Longueur cible :** 1500-3000 mots (10-20 min lecture)

---

### 5. Signaler des Erreurs ou Problèmes

**Vous avez trouvé :**
- Une information fausse ou obsolète ?
- Un lien cassé ?
- Un template qui ne fonctionne pas ?
- Une incohérence ?

→ [Ouvrez une issue](https://github.com/FR-Digital/ia-managers-toolkit/issues)

**Format d'issue apprécié :**

```
**Type :** Erreur / Suggestion / Question

**Localisation :** [Fichier concerné] - Ligne X

**Description :** [Ce qui ne va pas]

**Suggestion de correction :** [Si vous en avez une]
```

---

## Standards de Qualité

Tout contenu contribué doit respecter ces principes :

### 1. Business-Oriented (pas technique)

**❌ Mauvais :**
> "Pour implémenter le RAG, vectorisez vos documents avec BERT embeddings puis utilisez une base Pinecone avec top-k=5."

**✅ Bon :**
> "Le RAG permet à l'IA de chercher dans vos documents avant de répondre, évitant ainsi les réponses inventées. Coût : 5-20k€ setup, 200-500€/mois maintenance."

**Règle :** Si vous utilisez un terme technique, expliquez-le en une phrase simple.

### 2. Actionnable (utilisable immédiatement)

**❌ Mauvais :**
> "Il faut bien définir le scope du projet IA."

**✅ Bon :**
> "Remplissez cette checklist (30 min) pour vérifier que votre projet IA est prêt à être lancé : [lien checklist]"

**Règle :** Chaque conseil doit être accompagné d'un outil/template/exemple concret.

### 3. Concret (avec chiffres & exemples)

**❌ Mauvais :**
> "Un projet IA coûte cher."

**✅ Bon :**
> "Budget POC : 20-50k€. Budget production : 100-300k€. Exemple retail : 45k€ POC + 60k€/an production → ROI 71% année 1."

**Règle :** Toujours donner des ordres de grandeur chiffrés (budget, délais, ROI).

### 4. Honnête (échecs acceptés)

**On veut aussi des cas d'échec !**

Les projets qui n'ont pas marché sont **tout aussi instructifs** que les succès.

**Ce qu'on cherche dans un cas d'échec :**
- Pourquoi ça a échoué (données insuffisantes ? mauvais use case ? budget sous-estimé ?)
- Combien ça a coûté (pour éviter à d'autres de faire la même erreur)
- Qu'est-ce qui aurait pu être fait différemment

**Exemple de titre acceptable :**
> "Cas d'usage : Prédiction de churn clients - Échec (ROI négatif) - Leçons apprises"

---

## Style Rédactionnel

**Ton :** Professionnel mais accessible
- Tutoyez ("vous") pas vouvoiement distant
- Évitez jargon inutile
- Expliquez acronymes première occurrence

**Formatage :**
- Titres courts (< 60 caractères)
- Paragraphes courts (3-5 lignes max)
- Listes à puces (plus lisible que longs paragraphes)
- Emojis OK pour structure (✅ ❌ 📊 💡) mais sans excès
- Tableaux pour données chiffrées

**Exemples :**
- Toujours donner exemple concret après une règle générale
- Préférer "Exemple : Enseigne retail, 50 magasins..." à "Une entreprise..."

---

## Code de Conduite

### Valeurs

- **Respect mutuel** : Critiques constructives uniquement
- **Bienveillance** : Tout le monde apprend (y compris nous)
- **Pragmatisme** : Focus sur l'utilité pratique
- **Transparence** : Honnêteté sur limites & difficultés

### Inacceptable

- ❌ Condescendance ("c'est évident", "tout le monde sait que")
- ❌ Jargon non expliqué (volontairement complexe)
- ❌ Promotion déguisée (liens vers produits commerciaux sans disclaimer)
- ❌ Données non anonymisées (violation confidentialité)

---

## Licence & Droits

En contribuant, vous acceptez que :

- Votre contribution soit sous licence **MIT** (libre utilisation)
- Votre nom soit crédité (sauf demande contraire)
- Le contenu puisse être modifié par les mainteneurs (pour cohérence)

**Si vous partagez un template/document :**
- Confirmez que vous en détenez les droits
- Pas de contenu protégé par copyright tiers
- Anonymisation complète (pas de logos/infos confidentielles)

---

## Processus de Review

**Timeline :**
1. Vous soumettez une Pull Request
2. Review par mainteneur (72h max)
3. Échanges/ajustements si nécessaire
4. Merge + Remerciements publics !

**Critères de validation :**
- ✅ Respect standards qualité (ci-dessus)
- ✅ Informations vérifiables (ou clairement marquées "estimation")
- ✅ Anonymisation correcte (si applicable)
- ✅ Formatage cohérent avec repo

---

## Questions Fréquentes

**Q : Je peux contribuer même si mon projet IA a échoué ?**
R : **OUI !** Les échecs sont aussi instructifs que les succès. Partagez les leçons apprises.

**Q : Faut-il donner les vrais chiffres budgets ?**
R : Vous pouvez arrondir (ex: 47k€ → "environ 50k€") mais gardez ordre de grandeur réaliste.

**Q : Mon entreprise peut être citée ?**
R : Seulement si autorisation écrite. Sinon, anonymisez ("ETI retail, 200M€ CA").

**Q : Je peux contribuer un template que j'utilise en interne ?**
R : Oui, mais supprimez toute info confidentielle (logos, noms clients, données internes).

**Q : Combien de temps pour review ?**
R : 48-72h pour première review. On essaie d'être réactifs !

**Q : Je ne suis pas manager, je peux quand même contribuer ?**
R : Absolument ! Consultants, data scientists, chefs de projet... toute perspective est utile.

---

## Reconnaissance des Contributeurs

Les contributeurs majeurs seront :
- ✅ Crédités dans la section "Contributeurs" du README
- ✅ Mentionnés dans les release notes
- ✅ Invités à co-signer articles/publications (si applicable)

---

## Contact Mainteneurs

**Questions sur comment contribuer ?**

- 📧 Email : contact@lafabriq.ai
- 💬 Issue GitHub : [Ouvrir une discussion](https://github.com/FR-Digital/ia-managers-toolkit/issues)
- 🐦 Twitter/X : [@lafabriqlai](https://twitter.com/lafabriqai)

**Délai de réponse :** 48-72h max

---

## Contributeurs Actuels

Merci à tous ceux qui ont contribué à améliorer ce repo !

*(Liste automatiquement générée depuis git history)*

---

**Merci de contribuer à démocratiser l'IA pour les managers ! 🚀**

---

*Dernière mise à jour : Novembre 2025*
