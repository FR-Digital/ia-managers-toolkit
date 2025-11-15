# Guide d'Harmonisation LaFabriq
## Standards pour les Repositories Open Source

> Ce document définit les standards communs pour tous les repositories LaFabriq afin d'assurer une cohérence de marque et une expérience utilisateur unifiée.

---

## 1. Identité LaFabriq

### Positionnement

**LaFabriq = L'IA accessible aux décideurs**

- **Mission** : Démystifier l'IA pour les managers et décideurs non-techniques
- **Valeur** : Pragmatisme avant théorie, action avant buzzwords
- **Ton** : Expert mais accessible, honnête (y compris sur les limites)
- **Promesse** : "Vous n'avez pas besoin d'être data scientist pour piloter l'IA"

### Les 3 Pilliers

1. **Comprendre** → ia-glossaire-business-fr
2. **Évaluer** → ia-evaluation-pratique
3. **Piloter** → ia-managers-toolkit

Ces repos forment un **écosystème cohérent** : le glossaire pour le vocabulaire, l'évaluation pour mesurer, le toolkit pour agir.

---

## 2. Standards README.md

### Structure Obligatoire

```markdown
# [Nom du Repo] 🎯

> **[Tagline courte et percutante - max 10 mots]**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![French](https://img.shields.io/badge/Langue-Français-blue)]()
[![LaFabriq](https://img.shields.io/badge/LaFabriq-Open%20Source-orange)](https://lafabriq.ai)

## 🚀 Le Problème

[1-2 paragraphes décrivant le problème que ce repo résout]
- Point de douleur 1
- Point de douleur 2
- Point de douleur 3

## 💡 La Solution

[Explication claire de ce que ce repo offre]

## 📦 Ce que vous trouverez

[Liste structurée du contenu]

## ⚡ Quick Start

[3-4 étapes pour démarrer immédiatement]

1. **Besoin X ?** → [Lien](chemin)
2. **Besoin Y ?** → [Lien](chemin)
3. **Besoin Z ?** → [Lien](chemin)

## 🗂️ Structure du Repo

\`\`\`
repo-name/
├── dossier1/
├── dossier2/
└── ...
\`\`\`

## 🌐 Écosystème LaFabriq

Ce repo fait partie de la **suite LaFabriq** pour managers :

- 📖 **[ia-glossaire-business-fr](https://github.com/FR-Digital/ia-glossaire-business-fr)** - Vocabulaire IA sans jargon
- 📊 **[ia-evaluation-pratique](https://github.com/FR-Digital/ia-evaluation-pratique)** - Évaluer si votre IA fonctionne
- 🛠️ **[ia-managers-toolkit](https://github.com/FR-Digital/ia-managers-toolkit)** - Boîte à outils complète pour piloter l'IA

## 🤝 Contribuer

Vos retours d'expérience sont précieux !
Voir [CONTRIBUTING.md](CONTRIBUTING.md)

## 📜 Licence

[MIT License](LICENSE) - Utilisez, modifiez, partagez librement.

---

**Créé par [LaFabriq](https://lafabriq.ai)** - L'IA accessible aux décideurs | [Date]
```

### Éléments Obligatoires

- [ ] Badges standards (MIT, Français, LaFabriq)
- [ ] Section "Le Problème" claire
- [ ] Quick Start actionnable
- [ ] Liens vers les autres repos LaFabriq
- [ ] Référence LaFabriq en footer
- [ ] Emojis modérés (navigation visuelle)

---

## 3. Taglines des Repos

### Taglines Officielles

| Repo | Tagline | Emoji |
|------|---------|-------|
| **ia-glossaire-business-fr** | "Le vocabulaire IA traduit pour les décideurs" | 📖 |
| **ia-evaluation-pratique** | "Savoir si votre IA fonctionne bien, sans être data scientist" | 📊 |
| **ia-managers-toolkit** | "Tout ce qu'un manager doit savoir sur l'IA, sans le jargon technique" | 🛠️ |

### Sous-titres Complémentaires

Pour chaque repo, utiliser ces formulations cohérentes :

- **Glossaire** : "50+ termes essentiels expliqués simplement"
- **Évaluation** : "Framework en 3 niveaux : ça marche ? c'est utilisé ? ça rapporte ?"
- **Toolkit** : "Comprendre, évaluer, piloter - tout en un"

---

## 4. Structure des Dossiers

### Convention de Nommage

**Dossiers :** minuscules, tirets pour séparer
```
bon: guides-pratiques/
mauvais: GuidesPratiques/ ou guides_pratiques/
```

**Fichiers :** minuscules, tirets, .md
```
bon: comprendre-ia-en-10min.md
mauvais: ComprendreIA.md ou comprendre_ia.md
```

### Structure Standard par Repo

#### ia-glossaire-business-fr
```
ia-glossaire-business-fr/
├── README.md
├── CONTRIBUTING.md
├── LICENSE
├── SOURCES.md
├── glossaire/
│   ├── par-lettre/          # A.md, B.md, C.md...
│   ├── par-theme/           # ml.md, genai.md, data.md...
│   └── top-30-essentiels.md
├── fiches-concepts/
│   ├── machine-learning.md
│   ├── deep-learning.md
│   ├── llm-explique.md
│   └── ...
├── anti-glossaire/           # Ce que les termes NE veulent PAS dire
│   └── mythes-vocabulaire.md
└── ressources/
    └── comment-utiliser-glossaire.md
```

#### ia-evaluation-pratique
```
ia-evaluation-pratique/
├── README.md
├── CONTRIBUTING.md
├── LICENSE
├── SOURCES.md
├── frameworks/
│   ├── 3-niveaux-evaluation.md
│   ├── metriques-business-vs-tech.md
│   └── quand-arreter-projet.md
├── guides/
│   ├── organiser-tests-utilisateurs.md
│   ├── questions-equipe-technique.md
│   └── criteres-go-production.md
├── templates/
│   ├── grille-evaluation.md
│   ├── rapport-qualite.md
│   └── feedback-utilisateur.md
├── checklists/
│   ├── qualite-minimum.md
│   └── pre-production.md
└── examples/
    ├── evaluation-chatbot.md
    └── evaluation-analyse-sentiment.md
```

#### ia-managers-toolkit
```
ia-managers-toolkit/
├── README.md
├── CONTRIBUTING.md
├── LICENSE
├── SOURCES.md
├── fondamentaux/
│   ├── comprendre-ia-en-10min.md
│   ├── vocabulaire-essentiel.md
│   ├── mythes-vs-realite.md
│   └── types-ia-expliques.md
├── evaluation/
│   ├── framework-3-niveaux.md
│   ├── questions-equipe-tech.md
│   ├── metriques-business.md
│   └── quand-arreter-projet.md
├── pilotage/
│   ├── lancer-projet-ia.md
│   ├── budget-et-roi.md
│   ├── gerer-equipe-data.md
│   └── risques-et-ethique.md
├── templates/
│   ├── business-case-ia.md
│   ├── grille-evaluation.md
│   ├── rapport-avancement.md
│   └── checklist-pre-prod.md
├── cas-pratiques/
│   ├── chatbot-service-client.md
│   ├── automatisation-documents.md
│   └── analyse-donnees-ventes.md
└── ressources/
    ├── glossaire-complet.md
    ├── liens-utiles.md
    └── formations-recommandees.md
```

---

## 5. Style de Rédaction

### Ton LaFabriq

**À FAIRE :**
- ✅ Direct et concis
- ✅ Exemples concrets avant théorie
- ✅ Analogies accessibles
- ✅ Honnête sur les limites ("l'IA ne fait pas X")
- ✅ Pragmatique ("ce qui marche en vrai")
- ✅ Questions rhétoriques pour engager

**À ÉVITER :**
- ❌ Jargon technique non expliqué
- ❌ Phrases de plus de 3 lignes
- ❌ Ton académique ou pompeux
- ❌ Promesses irréalistes sur l'IA
- ❌ Condescendance ("c'est simple, voyons...")
- ❌ Anglicismes inutiles

### Exemples

**Mauvais :**
> "L'implémentation d'un système de Machine Learning nécessite une approche méthodologique rigoureuse incluant la collecte de datasets de qualité, le preprocessing, le feature engineering, et l'optimisation des hyperparamètres."

**Bon (LaFabriq) :**
> "Lancer un projet IA, c'est comme former un stagiaire très rapide. Vous lui montrez 10 000 exemples, il apprend les patterns, puis il peut travailler seul. Mais attention : s'il apprend sur de mauvais exemples, il fera de mauvaises prédictions. **La qualité des données = la qualité de l'IA.**"

### Formulations Récurrentes

Phrases à utiliser pour créer la cohérence :

- "Sans être data scientist..."
- "Ce que ça veut dire concrètement..."
- "En vrai, dans les entreprises..."
- "La question à poser : ..."
- "Red flag : ..."
- "Ce qui marche / Ce qui ne marche pas"
- "Avant de continuer, vérifiez que..."

---

## 6. Éléments Visuels

### Emojis Standards

| Usage | Emoji | Exemple |
|-------|-------|---------|
| Attention/Warning | ⚠️ | ⚠️ **Red flag** |
| Check/Validé | ✅ | ✅ Niveau 1 validé |
| Erreur/Échec | ❌ | ❌ Score insuffisant |
| Question | ❓ | ❓ À se poser |
| Important | 🚨 | 🚨 Critique |
| Conseil | 💡 | 💡 Astuce |
| Argent/Budget | 💰 | 💰 Coûts |
| Temps | ⏱️ | ⏱️ Timeline |
| Objectif | 🎯 | 🎯 But |
| Lancement | 🚀 | 🚀 Quick Start |

**Règle :** Max 1-2 emojis par section titre. Pas d'emojis dans le corps de texte sauf listes.

### Tableaux

Structure standard pour comparaisons :

```markdown
| Métrique | Seuil Minimum | Idéal | Votre Score |
|----------|---------------|-------|-------------|
| Précision | > 70% | > 90% | [ ] |
| Recall | > 60% | > 80% | [ ] |
```

### Code Blocks

Pour les formules ou exemples :

```markdown
ROI = (Gains - Coûts) / Coûts × 100

Exemple :
Gains = 180k€
Coûts = 105k€
ROI = (180 - 105) / 105 × 100 = 71%
```

### Schémas ASCII

Pour les workflows simples :

```
Question 1 : ÇA MARCHE ?
    │
    ├─ OUI ─────────────> Question 2
    │
    └─ NON ─────────────> STOP
```

---

## 7. Fichiers Standards

### CONTRIBUTING.md

Chaque repo doit avoir un CONTRIBUTING.md qui :
- Explique comment contribuer (cas pratiques, corrections, templates)
- Définit les standards de qualité
- Décrit le process de review
- Mentionne le code de conduite

**Template standard fourni dans ia-managers-toolkit/CONTRIBUTING.md**

### SOURCES.md

Chaque repo doit avoir un SOURCES.md qui :
- Liste les sources principales
- Explique la méthodologie de vulgarisation
- Reconnaît les limites du contenu
- Remercie les contributeurs

**Template standard fourni dans ia-managers-toolkit/SOURCES.md**

### LICENSE

**MIT License** pour tous les repos LaFabriq.

Texte standard :
```
MIT License

Copyright (c) 2025 LaFabriq

Permission is hereby granted, free of charge, to any person obtaining a copy...
```

---

## 8. Références Croisées

### Liens Entre Repos

Chaque repo doit référencer les autres quand pertinent :

**Dans ia-glossaire-business-fr :**
> "Vous maîtrisez le vocabulaire ? Passez à l'action avec le [ia-managers-toolkit](lien)"

**Dans ia-evaluation-pratique :**
> "Besoin de comprendre un terme ? Consultez le [glossaire](lien)"

**Dans ia-managers-toolkit :**
> "Pour évaluer en détail, utilisez [ia-evaluation-pratique](lien)"

### Section "Écosystème LaFabriq"

Obligatoire dans chaque README :

```markdown
## 🌐 Écosystème LaFabriq

Ce repo fait partie de la **suite LaFabriq** pour managers :

- 📖 **[ia-glossaire-business-fr](lien)** - Vocabulaire IA sans jargon
- 📊 **[ia-evaluation-pratique](lien)** - Évaluer si votre IA fonctionne
- 🛠️ **[ia-managers-toolkit](lien)** - Boîte à outils complète

**Parcours recommandé :** Glossaire → Évaluation → Toolkit
```

---

## 9. Cohérence des Contenus

### Termes à Utiliser de Manière Cohérente

| Terme Standard | Variantes Acceptées | À Éviter |
|----------------|---------------------|----------|
| Manager | Décideur, Dirigeant | Chef |
| Data Scientist | DS | Scientifique des données |
| Machine Learning | ML, Apprentissage automatique | Machine learning (sans majuscule) |
| Deep Learning | DL | Apprentissage profond |
| IA Générative | GenAI, LLM | IA générative (minuscule) |
| ROI | Retour sur investissement | RSI |
| POC | Proof of Concept | Preuve de concept |
| Dataset | Jeu de données | Set de données |

### Chiffres et Métriques Cohérents

Utiliser les mêmes ordres de grandeur dans tous les repos :

**Coûts typiques :**
- POC : 30-80k€
- Pilote : 50-150k€
- Production Y1 : 100-300k€
- Maintenance : 20-30% du coût initial/an

**Timelines typiques :**
- POC : 2-3 mois
- Pilote : 3-6 mois
- Mise en prod : 1-3 mois
- Total : 9-15 mois

**Métriques de succès :**
- Précision minimum : > 70-80%
- Adoption utilisateurs : > 50%
- Satisfaction : > 3.5/5
- ROI : > 0% minimum, idéal > 100%

---

## 10. Checklist de Publication

Avant de publier/merger un repo LaFabriq :

### Contenu
- [ ] README.md complet avec tous les éléments obligatoires
- [ ] Badges LaFabriq présents
- [ ] Section Écosystème avec liens vers autres repos
- [ ] Quick Start actionnable
- [ ] CONTRIBUTING.md présent
- [ ] SOURCES.md présent
- [ ] LICENSE MIT

### Qualité
- [ ] Pas de jargon non expliqué
- [ ] Exemples concrets présents
- [ ] Ton LaFabriq respecté (pragmatique, honnête)
- [ ] Structure de dossiers conforme
- [ ] Nommage des fichiers en minuscules avec tirets
- [ ] Liens internes fonctionnels
- [ ] Orthographe/grammaire vérifiée

### Branding
- [ ] Référence LaFabriq en footer
- [ ] Emojis modérés et cohérents
- [ ] Tagline officielle utilisée
- [ ] Termes standards utilisés
- [ ] Cohérence des chiffres/métriques

---

## 11. Roadmap Harmonisation

### Phase 1 : Corrections Urgentes

**ia-glossaire-business-fr :**
- [ ] Créer README.md complet
- [ ] Structurer les dossiers (glossaire/, fiches-concepts/, etc.)
- [ ] Ajouter CONTRIBUTING.md et SOURCES.md
- [ ] Créer contenu principal (50+ termes)

**ia-evaluation-pratique :**
- [ ] Vérifier conformité README (badges, écosystème)
- [ ] Ajouter liens vers autres repos
- [ ] Vérifier CONTRIBUTING.md et SOURCES.md

**ia-managers-toolkit :**
- [ ] Mettre à jour README avec badges LaFabriq
- [ ] Ajouter section Écosystème
- [ ] Vérifier cohérence avec les 2 autres repos

### Phase 2 : Enrichissement

- [ ] Vérifier références croisées (termes du glossaire dans toolkit, etc.)
- [ ] Harmoniser les exemples (même chatbot SAV dans les 3 repos)
- [ ] Créer un repo "méta" ou landing page commune
- [ ] Ajouter des liens GitHub Topics cohérents

### Phase 3 : Communication

- [ ] Landing page sur lafabriq.ai avec les 3 repos
- [ ] Posts LinkedIn de lancement
- [ ] Contribution guidelines communes

---

## 12. Templates Prêts à Copier

### Badge LaFabriq

```markdown
[![LaFabriq](https://img.shields.io/badge/LaFabriq-Open%20Source-orange)](https://lafabriq.ai)
```

### Section Écosystème (copier-coller)

```markdown
## 🌐 Écosystème LaFabriq

Ce repo fait partie de la **suite LaFabriq** pour managers :

- 📖 **[ia-glossaire-business-fr](https://github.com/FR-Digital/ia-glossaire-business-fr)** - Vocabulaire IA sans jargon
- 📊 **[ia-evaluation-pratique](https://github.com/FR-Digital/ia-evaluation-pratique)** - Évaluer si votre IA fonctionne
- 🛠️ **[ia-managers-toolkit](https://github.com/FR-Digital/ia-managers-toolkit)** - Boîte à outils complète

**Parcours recommandé :** Glossaire → Évaluation → Toolkit
```

### Footer Standard

```markdown
---

**Créé par [LaFabriq](https://lafabriq.ai)** - L'IA accessible aux décideurs | Nov 2025
```

---

## Conclusion

Ce guide assure que les 3 repos LaFabriq ont une **identité visuelle et éditoriale cohérente**. Le lecteur qui passe d'un repo à l'autre doit immédiatement reconnaître "la patte LaFabriq" :

- **Même ton** : pragmatique et honnête
- **Même structure** : claire et navigable
- **Même promesse** : l'IA accessible sans être expert
- **Même qualité** : concret et actionnable

La force de LaFabriq est dans la **complémentarité** des 3 repos, pas dans leur isolation. Un manager qui découvre le glossaire doit naturellement être guidé vers l'évaluation, puis vers le toolkit complet.

---

*Guide d'Harmonisation LaFabriq | v1.0 | Nov 2025*
