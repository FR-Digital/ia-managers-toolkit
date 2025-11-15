# Gérer une Équipe Data/IA

> Manager des data scientists quand on n'est pas technique.

## Les Défis du Management IA

### Ce qui est différent
- **Incertitude élevée :** "On ne sait pas si ça va marcher"
- **Langage technique :** Vocabulaire hermétique
- **Mesure de performance floue :** Difficile d'évaluer la productivité
- **Timeline imprévisible :** Les expérimentations prennent du temps

### Ce qui reste pareil
- Besoin de vision claire
- Communication régulière
- Objectifs mesurables
- Reconnaissance du travail

---

## Comprendre les Rôles

### Data Scientist
**Ce qu'il fait :**
- Analyse les données
- Crée et entraîne les modèles
- Expérimente différentes approches
- Évalue la performance

**Ce qu'il attend de vous :**
- Comprendre que l'expérimentation prend du temps
- Accès aux données
- Clarté sur l'objectif business
- Feedback sur la pertinence métier

### Data Engineer
**Ce qu'il fait :**
- Construit les pipelines de données
- Assure la qualité des données
- Gère l'infrastructure
- Optimise les performances

**Ce qu'il attend de vous :**
- Budget infra réaliste
- Temps pour faire proprement
- Pas de dette technique forcée
- Reconnaissance du travail invisible

### ML Engineer
**Ce qu'il fait :**
- Déploie les modèles en production
- Optimise pour la scalabilité
- Met en place le monitoring
- Automatise les pipelines ML

**Ce qu'il attend de vous :**
- Standards de qualité clairs
- Temps pour la mise en prod (pas de "ça marche sur mon poste")
- Budget maintenance
- Implication dans les décisions techniques

### Prompt Engineer / AI Product Manager
**Ce qu'il fait :**
- Conçoit les interactions IA-utilisateur
- Optimise les prompts
- Gère la qualité des outputs
- Fait le pont métier-technique

**Ce qu'il attend de vous :**
- Compréhension des cas d'usage métier
- Feedback utilisateurs
- Définition claire des critères de succès
- Équilibre vitesse vs qualité

---

## Structurer les Interactions

### Daily Standup (15 min)
**Adapté IA :**
- Ce que j'ai testé hier
- Ce que je teste aujourd'hui
- Mes blocages

**À éviter :**
- Demander "combien de lignes de code ?"
- Micro-manager les expérimentations
- Exiger des résultats quotidiens

### Weekly Tech Review (1h)
**Format recommandé :**
1. Métriques de performance (10 min)
2. Expérimentations en cours (20 min)
3. Problèmes rencontrés (15 min)
4. Priorités semaine prochaine (15 min)

**Questions utiles :**
- "Qu'avez-vous appris cette semaine ?"
- "Quelles hypothèses avez-vous validées/invalidées ?"
- "De quoi avez-vous besoin de ma part ?"

### Monthly Business Review
**Pour connecter tech et business :**
- KPIs métier vs métriques techniques
- Feedback utilisateurs
- ROI update
- Roadmap ajustement

---

## Communication Efficace

### Traduire le Jargon

**Équipe dit :** "Le recall est trop bas"
**Vous comprenez :** "L'IA rate trop de cas importants"
**Vous demandez :** "Combien de cas sur 100 sont manqués ?"

**Équipe dit :** "On a de l'overfitting"
**Vous comprenez :** "L'IA a trop mémorisé et ne généralise pas"
**Vous demandez :** "Quelle est la différence de performance entre test et production ?"

**Équipe dit :** "Il nous faut plus de données"
**Vous comprenez :** "Les exemples actuels ne suffisent pas"
**Vous demandez :** "De quel type de données précisément ? Combien ?"

### Poser les Bonnes Questions

**Au lieu de :** "C'est fini quand ?"
**Demandez :** "Quelles sont les étapes restantes et leurs risques ?"

**Au lieu de :** "Pourquoi c'est si long ?"
**Demandez :** "Qu'est-ce qui bloque et comment puis-je aider ?"

**Au lieu de :** "Ça marche ou pas ?"
**Demandez :** "Quelles sont les métriques actuelles et comment se comparent-elles à notre objectif ?"

**Au lieu de :** "C'est mieux que la concurrence ?"
**Demandez :** "Comment se compare notre solution à notre baseline ? Et aux solutions du marché ?"

### Feedback Constructif

**Bon feedback :**
"Les utilisateurs trouvent les réponses trop longues. Peut-on les raccourcir tout en gardant l'information clé ?"

**Mauvais feedback :**
"C'est pas bon, refaites."

**Bon feedback :**
"Cette fonctionnalité aide vraiment le métier car [explication]. Excellent travail sur [aspect spécifique]."

**Mauvais feedback :**
"C'est bien." (trop vague)

---

## Gérer l'Incertitude

### Accepter l'Expérimentation

**Mindset nécessaire :**
- 70% des expérimentations échouent
- L'échec = apprentissage précieux
- Pivoter n'est pas un problème
- Le chemin n'est pas linéaire

**Comment réagir à un échec :**
1. "Qu'avons-nous appris ?"
2. "Cette hypothèse est invalidée, quelle est la suivante ?"
3. "Comment capitaliser sur cet apprentissage ?"

### Gérer les Estimations

**Réalité :**
Les estimations IA sont souvent fausses (×2-3 en temps).

**Stratégie :**
- Demander des fourchettes (min-max)
- Identifier les incertitudes explicitement
- Prévoir des points de go/no-go
- Budgéter une marge de 30-50%

**Exemple :**
"Estimation : 2-4 semaines selon la complexité des données. Point de validation après 1 semaine pour réévaluer."

---

## Éviter les Pièges Classiques

### 1. "Je veux voir du code chaque jour"
**Problème :** Les data scientists passent 60% du temps à comprendre les données, pas à coder.

**Solution :** Mesurer les apprentissages et hypothèses testées, pas les lignes de code.

### 2. "On peut accélérer en ajoutant des gens"
**Problème :** La loi de Brooks s'applique doublement à l'IA.

**Solution :** Mieux vaut une petite équipe experte qu'une grosse équipe junior.

### 3. "Le modèle fonctionne, on passe en prod"
**Problème :** 90% du travail est après que "ça marche".

**Solution :** Prévoir autant de temps pour la mise en prod que pour le développement.

### 4. "L'équipe tech décide seule"
**Problème :** L'IA sans input métier résout le mauvais problème.

**Solution :** Impliquer les utilisateurs finaux dès le début.

### 5. "On embauche un génie qui va tout faire"
**Problème :** Aucun profil ne maîtrise toute la chaîne.

**Solution :** Équipe pluridisciplinaire (DS + DE + MLEng minimum).

---

## Recruter et Retenir les Talents

### Compétences à Rechercher

**Hard skills :**
- Solide en statistiques et ML
- Expérience avec les données réelles (pas que Kaggle)
- Capacité à déployer en production
- Familiarité avec le cloud

**Soft skills (critiques) :**
- Communication claire aux non-techniques
- Curiosité et apprentissage continu
- Tolérance à l'ambiguïté
- Pragmatisme vs perfectionnisme

### Questions d'Entretien Utiles

**Pour évaluer la communication :**
"Expliquez-moi [concept technique] comme si j'étais votre grand-mère."

**Pour évaluer le pragmatisme :**
"Racontez-moi un projet où vous avez dû simplifier votre approche pour des contraintes business."

**Pour évaluer la résolution de problèmes :**
"Comment aborderiez-vous un problème où les données sont sales et incomplètes ?"

### Rétention

**Ce qui motive les talents data :**
- Problèmes intéressants à résoudre
- Impact visible de leur travail
- Accès aux bonnes données et outils
- Temps pour apprendre et expérimenter
- Reconnaissance de leur expertise

**Ce qui les fait partir :**
- Bureaucratie excessive
- Pas d'accès aux données
- Management qui ne comprend pas
- Pas de mise en production
- Infrastructure dépassée

---

## KPIs d'Équipe

### Performance Projet
- Nombre de modèles déployés en prod
- Time to production (du POC à la prod)
- ROI des projets délivrés
- Taux de succès des POCs

### Qualité Technique
- Uptime des modèles en production
- Fréquence des incidents
- Technical debt accumulée
- Documentation à jour

### Satisfaction Équipe
- Turnover (critique si > 20%/an)
- Satisfaction (survey anonyme)
- Temps passé en maintenance vs innovation
- Opportunités d'apprentissage prises

---

## Check-List Manager

### Mensuel
- [ ] 1:1 avec chaque membre de l'équipe
- [ ] Review des métriques projet
- [ ] Feedback utilisateurs partagé
- [ ] Blocages identifiés et résolus

### Trimestriel
- [ ] Review des objectifs équipe
- [ ] Plan de formation/montée en compétences
- [ ] Évaluation de la dette technique
- [ ] Roadmap ajustée

### Annuel
- [ ] Évaluation de performance
- [ ] Plan de développement individuel
- [ ] Budget équipe et outils réévalué
- [ ] Stratégie IA alignée avec business

---

## Ressources

- [Vocabulaire essentiel](../fondamentaux/vocabulaire-essentiel.md) - Comprendre le jargon
- [Questions équipe tech](../evaluation/questions-equipe-tech.md) - Poser les bonnes questions
- [Lancer un projet IA](lancer-projet-ia.md) - Structurer le travail

---

*Management équipe data/IA | Dernière MAJ : Nov 2025*
