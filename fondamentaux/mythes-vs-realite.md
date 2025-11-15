# Mythes vs Réalité sur l'IA

> 10 idées reçues sur l'IA démystifiées pour les décideurs.

## Mythe 1 : "L'IA va remplacer tous les emplois"

### Ce qu'on entend
"Dans 5 ans, il n'y aura plus besoin d'humains, l'IA fera tout."

### La réalité
L'IA **automatise des tâches**, pas des emplois entiers. Elle est bonne pour les tâches répétitives et à pattern, mauvaise pour le jugement, la créativité et les relations humaines.

**Ce qui se passe vraiment :**
- Les emplois évoluent plus qu'ils ne disparaissent
- L'IA augmente la productivité humaine
- De nouveaux rôles émergent (prompt engineer, AI trainer)
- Les emplois nécessitant empathie et jugement restent humains

**Exemple concret :**
Un chatbot SAV traite 70% des questions simples. Les agents humains se concentrent sur les cas complexes et la relation client. Résultat : plus de satisfaction client, pas moins d'emplois.

---

## Mythe 2 : "L'IA est toujours objective"

### Ce qu'on entend
"L'IA décide sans biais, contrairement aux humains."

### La réalité
L'IA **reproduit les biais présents dans ses données d'entraînement**. Si les données historiques sont biaisées, l'IA l'est aussi.

**Exemples de biais documentés :**
- IA de recrutement d'Amazon pénalisant les CV de femmes
- Reconnaissance faciale moins précise sur peaux foncées
- Systèmes de crédit défavorisant certaines zones géographiques

**Comment se protéger :**
- Auditer les données d'entraînement
- Tester l'équité sur différents groupes
- Garder une supervision humaine sur les décisions importantes
- Documenter et monitorer les décisions de l'IA

---

## Mythe 3 : "Plus de données = meilleure IA"

### Ce qu'on entend
"On a 10 millions de lignes, notre IA sera forcément meilleure."

### La réalité
La **qualité prime sur la quantité**. Des données mal étiquetées, incomplètes ou non représentatives donneront une mauvaise IA, quelle que soit la quantité.

**Ce qui compte vraiment :**
- **Qualité :** Données propres, bien étiquetées, vérifiées
- **Représentativité :** Couvre tous les cas d'usage réels
- **Fraîcheur :** Données récentes, pas obsolètes
- **Pertinence :** Données liées au problème à résoudre

**Règle d'or :**
1 000 exemples de qualité > 100 000 exemples bruités

**Exemple :**
Un chatbot entraîné sur 5 000 conversations SAV bien annotées performera mieux qu'un chatbot avec 50 000 conversations non vérifiées contenant des erreurs.

---

## Mythe 4 : "L'IA comprend ce qu'elle dit"

### Ce qu'on entend
"ChatGPT comprend vraiment ma question et y répond intelligemment."

### La réalité
L'IA générative est un **très bon système de prédiction statistique**. Elle prédit le mot suivant le plus probable, sans "comprendre" au sens humain.

**Conséquences :**
- **Hallucinations :** L'IA peut inventer des faits avec confiance
- **Pas de bon sens :** Elle peut écrire des absurdités logiques
- **Pas de vérification :** Elle ne sait pas si ce qu'elle dit est vrai
- **Manipulation facile :** On peut lui faire dire n'importe quoi

**Conseil pratique :**
- Toujours vérifier les informations factuelles
- Ne pas utiliser l'IA pour des décisions critiques sans validation humaine
- Être particulièrement vigilant pour les chiffres, dates, citations

---

## Mythe 5 : "Implémenter l'IA est rapide et facile"

### Ce qu'on entend
"On va intégrer ChatGPT en 2 semaines et c'est réglé."

### La réalité
Un projet IA sérieux prend **6 à 18 mois** et nécessite des compétences spécifiques.

**Timeline réaliste :**
- POC : 1-3 mois
- Pilote : 3-6 mois
- Production : 3-6 mois supplémentaires
- Stabilisation : 3-6 mois encore

**Les obstacles ignorés :**
- Nettoyage des données (40% du temps projet)
- Intégration avec systèmes existants
- Formation des utilisateurs
- Mise en place du monitoring
- Gestion du changement

**Coûts cachés :**
- Infrastructure (GPU, stockage, réseau)
- Licences API (ça chiffre vite)
- Maintenance continue (ré-entraînement, mise à jour)
- Support et formation

---

## Mythe 6 : "Une fois déployée, l'IA fonctionne seule"

### Ce qu'on entend
"On déploie et on n'y touche plus pendant 3 ans."

### La réalité
L'IA nécessite une **maintenance continue** sinon elle se dégrade.

**Pourquoi l'IA se dégrade :**
- **Data drift :** Les données réelles changent (ex: post-COVID)
- **Concept drift :** Le problème évolue (nouveaux produits, nouvelles fraudes)
- **Dépendances :** Les APIs et librairies changent
- **Usage :** Les utilisateurs trouvent des cas non prévus

**Maintenance nécessaire :**
- Monitoring des performances (quotidien)
- Ré-entraînement (mensuel à trimestriel)
- Mise à jour des modèles (annuel)
- Correction des bugs (continu)

**Budget maintenance :**
Prévoir 20-30% du coût initial par an en maintenance.

---

## Mythe 7 : "L'IA générative peut tout faire"

### Ce qu'on entend
"Avec GPT-4, on peut automatiser n'importe quoi."

### La réalité
L'IA générative excelle dans certains domaines et est **médiocre voire dangereuse** dans d'autres.

**Où l'IA générative excelle :**
- Rédaction de contenus marketing
- Résumés et reformulation
- Brainstorming et idéation
- Assistance au code
- FAQ et support basique

**Où elle est risquée :**
- Conseils juridiques ou médicaux
- Calculs mathématiques complexes
- Faits historiques précis
- Décisions financières critiques
- Tout ce qui nécessite une garantie de véracité

**Règle d'or :**
Plus les conséquences d'une erreur sont graves, plus la supervision humaine doit être forte.

---

## Mythe 8 : "Notre cas est trop spécifique pour l'IA"

### Ce qu'on entend
"Notre industrie est tellement particulière que l'IA ne marchera pas."

### La réalité
L'IA s'adapte bien aux cas spécifiques grâce au **fine-tuning** et au **prompt engineering**.

**Ce qui est vrai :**
- Les modèles génériques ne marcheront pas out-of-the-box
- Vous aurez besoin de données spécifiques à votre domaine
- Le jargon métier doit être appris

**Ce qui est faisable :**
- Fine-tuner un modèle sur vos données
- Utiliser RAG (Retrieval Augmented Generation) avec vos documents
- Créer des prompts spécialisés pour votre contexte

**Exemple :**
Un cabinet d'avocats peut fine-tuner un LLM sur la jurisprudence française pour avoir un assistant juridique pertinent.

---

## Mythe 9 : "L'IA va résoudre tous nos problèmes de données"

### Ce qu'on entend
"On a des données en vrac, l'IA va les organiser."

### La réalité
**Garbage in, garbage out.** L'IA ne corrige pas les mauvaises données, elle les amplifie.

**Problèmes que l'IA ne résout pas :**
- Données manquantes
- Données mal étiquetées
- Données contradictoires
- Données non structurées sans contexte
- Silos de données non connectés

**Ce qu'il faut avant l'IA :**
1. Stratégie data claire
2. Gouvernance des données
3. Pipelines de nettoyage
4. Standards de qualité
5. Infrastructure de stockage

**Conseil :**
Investissez d'abord dans votre data platform avant de lancer des projets IA.

---

## Mythe 10 : "Notre concurrent a de l'IA, on doit en avoir aussi"

### Ce qu'on entend
"Tout le monde fait de l'IA, on va être en retard."

### La réalité
L'IA n'est pas une fin en soi. C'est un **outil pour résoudre des problèmes business spécifiques**.

**Mauvaises raisons de faire de l'IA :**
- "C'est tendance"
- "Le concurrent en a"
- "Pour impressionner les investisseurs"
- "Parce qu'on a des données"

**Bonnes raisons de faire de l'IA :**
- Problème business clair et mesurable
- ROI calculable et positif
- Données disponibles et de qualité
- Équipe capable de maintenir
- Cas d'usage où l'IA apporte une vraie valeur

**Question clé :**
"Quel problème business précis cette IA résout-elle, et pourquoi l'IA est-elle la meilleure solution ?"

---

## Résumé : Les Vraies Questions à Se Poser

| Au lieu de... | Demandez-vous... |
|---------------|------------------|
| "On a besoin d'IA" | "Quel problème business précis voulons-nous résoudre ?" |
| "L'IA va tout automatiser" | "Quelles tâches spécifiques peuvent être automatisées ?" |
| "On a plein de données" | "Nos données sont-elles propres, pertinentes et représentatives ?" |
| "L'IA sera objective" | "Quels biais pourraient exister dans nos données ?" |
| "On déploie et c'est fini" | "Qui va maintenir et monitorer cette IA ?" |

---

## Pour aller plus loin

- [Framework d'évaluation](../evaluation/framework-3-niveaux.md) - Évaluer objectivement un projet IA
- [Risques et éthique](../pilotage/risques-et-ethique.md) - Gérer les risques IA
- [Budget et ROI](../pilotage/budget-et-roi.md) - Calculer le vrai coût

---

*10 mythes démystifiés | Dernière MAJ : Nov 2025*
