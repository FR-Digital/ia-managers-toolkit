# Vocabulaire IA Essentiel pour Managers

> 30 termes clés expliqués simplement, avec analogies et exemples business.

## Termes Fondamentaux

### 1. Intelligence Artificielle (IA)
**Définition :** Programme qui apprend à partir de données pour effectuer des tâches.
**Analogie :** Un stagiaire très rapide qu'on forme avec des milliers d'exemples.
**Exemple :** Un système qui apprend à reconnaître les emails spam.

### 2. Machine Learning (ML)
**Définition :** Sous-ensemble de l'IA où le programme apprend sans être explicitement programmé.
**Analogie :** Au lieu de lui dire "si email contient GRATUIT alors spam", on lui montre des exemples et il trouve les règles tout seul.
**Exemple :** Netflix qui apprend vos goûts en analysant ce que vous regardez.

### 3. Deep Learning
**Définition :** ML avancé utilisant des réseaux de neurones à plusieurs couches.
**Analogie :** Un stagiaire avec un cerveau plus complexe, capable de reconnaître des patterns très subtils.
**Exemple :** Reconnaissance faciale sur votre téléphone.

### 4. Modèle
**Définition :** Le "cerveau" de l'IA après entraînement, qui contient les patterns appris.
**Analogie :** L'expertise accumulée par votre employé après sa formation.
**Exemple :** GPT-4 est un modèle de langage entraîné sur internet.

### 5. Dataset (Jeu de données)
**Définition :** Ensemble de données utilisées pour entraîner l'IA.
**Analogie :** Les manuels de formation de votre stagiaire.
**Exemple :** 100 000 tickets SAV avec leurs résolutions pour entraîner un chatbot.

---

## Termes d'Entraînement

### 6. Entraînement (Training)
**Définition :** Phase où l'IA apprend à partir des données.
**Analogie :** La période d'essai où le stagiaire apprend le métier.
**Exemple :** Montrer 50 000 images de chats à l'IA pour qu'elle apprenne à les reconnaître.

### 7. Inférence
**Définition :** Quand l'IA utilise ce qu'elle a appris pour faire des prédictions sur de nouvelles données.
**Analogie :** Le stagiaire formé qui travaille maintenant sur de vrais dossiers.
**Exemple :** Le modèle entraîné qui classe un nouvel email comme spam ou non.

### 8. Overfitting (Sur-apprentissage)
**Définition :** L'IA a trop mémorisé les exemples d'entraînement et ne généralise pas bien.
**Analogie :** Un étudiant qui apprend par cœur les réponses sans comprendre.
**Exemple :** 99% de précision sur les tests, 60% en production.

### 9. Underfitting (Sous-apprentissage)
**Définition :** L'IA n'a pas assez appris, elle est trop simpliste.
**Analogie :** Un stagiaire qui n'a pas assez de formation.
**Exemple :** L'IA classe tout comme "non-spam" par défaut.

### 10. Fine-tuning
**Définition :** Adapter un modèle pré-entraîné à une tâche spécifique avec moins de données.
**Analogie :** Former un expert général à votre industrie spécifique.
**Exemple :** Prendre GPT et l'adapter à votre jargon métier.

---

## Métriques de Performance

### 11. Précision (Accuracy)
**Définition :** Pourcentage de bonnes réponses sur l'ensemble des prédictions.
**Exemple :** Sur 100 emails classés, 92 sont correctement identifiés = 92% de précision.
**Attention :** Peut être trompeuse si les classes sont déséquilibrées.

### 12. Recall (Rappel)
**Définition :** Parmi tous les vrais positifs, combien l'IA en a trouvé.
**Exemple :** Sur 50 vrais spams, l'IA en a détecté 45 = 90% de recall.
**Quand c'est important :** Quand manquer un cas est grave (fraude, maladie).

### 13. Precision (Précision du positif)
**Définition :** Parmi ce que l'IA prédit comme positif, combien le sont vraiment.
**Exemple :** Sur 60 emails marqués spam, 54 sont vraiment spam = 90% precision.
**Quand c'est important :** Quand les faux positifs coûtent cher.

### 14. F1-Score
**Définition :** Moyenne harmonique entre Precision et Recall.
**Quand l'utiliser :** Pour avoir une vision équilibrée de la performance.
**Bon score :** > 0.8 généralement.

### 15. Latence
**Définition :** Temps de réponse de l'IA.
**Exemple :** Le chatbot répond en 2 secondes = 2s de latence.
**Seuil typique :** < 3 secondes pour une bonne UX.

---

## Termes IA Générative

### 16. LLM (Large Language Model)
**Définition :** Gros modèle de langage entraîné sur des milliards de textes.
**Exemples :** GPT-4, Claude, Llama, Mistral.
**Usage :** Chatbots, génération de texte, résumés.

### 17. Prompt
**Définition :** L'instruction ou question que vous donnez à l'IA générative.
**Analogie :** La consigne que vous donnez à un assistant.
**Exemple :** "Résume ce document en 3 points clés".

### 18. Prompt Engineering
**Définition :** L'art de formuler des prompts efficaces.
**Pourquoi important :** Un bon prompt = meilleure réponse.
**Conseil :** Soyez précis, donnez du contexte, des exemples.

### 19. Hallucination
**Définition :** Quand l'IA invente des informations fausses avec confiance.
**Analogie :** Quelqu'un qui ment sans le savoir.
**Exemple :** ChatGPT qui cite un livre qui n'existe pas.
**Risque :** Critique dans les contextes juridiques, médicaux, financiers.

### 20. Temperature
**Définition :** Paramètre qui contrôle la créativité vs précision de l'IA.
**Temperature basse (0.1) :** Réponses prévisibles, précises.
**Temperature haute (0.9) :** Réponses créatives, variées.
**Usage :** Basse pour FAQ, haute pour brainstorming.

### 21. Tokens
**Définition :** Unités de texte (mots ou morceaux de mots) traitées par l'IA.
**Pourquoi ça compte :** Le coût API est souvent calculé en tokens.
**Exemple :** "Bonjour, comment allez-vous ?" = environ 6 tokens.

---

## Termes Techniques Importants

### 22. API (Application Programming Interface)
**Définition :** Interface permettant à vos systèmes de communiquer avec l'IA.
**Analogie :** Le guichet par lequel vous passez vos commandes.
**Exemple :** Appeler l'API OpenAI pour obtenir une réponse de GPT.

### 23. Cloud vs On-Premise
**Cloud :** L'IA tourne sur les serveurs du fournisseur (OpenAI, Google, etc.).
**On-Premise :** L'IA tourne sur vos propres serveurs.
**Trade-off :** Cloud = plus simple mais moins de contrôle sur les données.

### 24. GPU (Graphics Processing Unit)
**Définition :** Processeur spécialisé nécessaire pour entraîner et faire tourner les IA.
**Pourquoi ça coûte cher :** Les GPU IA coûtent 10 000€ à 30 000€ pièce.
**Alternative :** Louer du GPU cloud (AWS, Google Cloud, Azure).

### 25. Biais (Bias)
**Définition :** Préjugés présents dans les données qui se retrouvent dans l'IA.
**Exemple :** IA de recrutement qui favorise les hommes car entraînée sur des historiques biaisés.
**Solution :** Auditer les données et tester l'équité du modèle.

---

## Termes Business

### 26. POC (Proof of Concept)
**Définition :** Petit projet pilote pour valider la faisabilité technique.
**Durée typique :** 1-3 mois.
**Budget typique :** 20k-50k€.
**Objectif :** Prouver que ça marche, pas que c'est scalable.

### 27. MLOps
**Définition :** Pratiques pour déployer et maintenir des modèles IA en production.
**Analogie :** Le DevOps mais pour les modèles ML.
**Pourquoi important :** Sans MLOps, votre IA se dégrade avec le temps.

### 28. Data Drift
**Définition :** Quand les nouvelles données diffèrent de celles d'entraînement.
**Exemple :** Modèle entraîné pré-COVID qui ne marche plus après.
**Solution :** Monitoring continu et ré-entraînement régulier.

### 29. ROI (Return on Investment)
**Définition :** (Gains - Coûts) / Coûts × 100
**Calcul IA typique :**
- Gains : temps économisé × coût horaire + revenus additionnels
- Coûts : développement + API + maintenance + infrastructure
**Bon ROI :** > 100% à 12-18 mois.

### 30. Time to Value
**Définition :** Temps entre le début du projet et les premiers bénéfices mesurables.
**POC :** 1-3 mois pour premiers résultats.
**Production :** 6-12 mois pour ROI positif.
**Attention :** Les projets IA prennent plus de temps qu'on ne pense.

---

## Anti-Glossaire : Ce que ça ne veut PAS dire

| Terme | Ce que ça ne veut PAS dire |
|-------|----------------------------|
| "L'IA comprend" | Elle reconnaît des patterns, elle ne comprend pas vraiment |
| "L'IA apprend" | Elle optimise des paramètres mathématiques |
| "L'IA est intelligente" | Elle est très bonne à une tâche spécifique, pas intelligente au sens humain |
| "95% de précision" | Pas que ça marche 95% du temps en production |

---

## Prochaines étapes

- [Mythes vs Réalité](mythes-vs-realite.md) - Démystifier les idées reçues
- [Types d'IA expliqués](types-ia-expliques.md) - Approfondir les catégories
- [Questions à poser](../evaluation/questions-equipe-tech.md) - Utiliser ce vocabulaire en réunion

---

*30 termes essentiels | Dernière MAJ : Nov 2025*
