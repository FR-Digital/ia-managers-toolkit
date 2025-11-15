# 30 Questions à Poser à Votre Équipe Technique

> **Évaluer la qualité de votre IA sans comprendre le code**

## Comment Utiliser ce Guide

Ces questions sont formulées en **langage business**. Votre équipe technique doit pouvoir y répondre clairement. Si les réponses sont vagues ou évasives, c'est un signal d'alerte.

**Format :**
- La question en langage simple
- Ce que la réponse devrait contenir
- Signal d'alerte si réponse insuffisante

---

## Questions sur la Performance (6 questions)

### 1. Quel pourcentage de réponses correctes obtient l'IA ?

**Bonne réponse :** "Sur nos 500 cas de test, l'IA répond correctement dans 87% des cas."

**Signal d'alerte :** "C'est difficile à dire" ou "Ça dépend des cas"

**Pourquoi c'est important :** C'est LA métrique de base. Sans ce chiffre, vous volez à l'aveugle.

---

### 2. Combien de temps met l'IA pour répondre ?

**Bonne réponse :** "En moyenne 2.3 secondes, avec 95% des réponses en moins de 5 secondes."

**Signal d'alerte :** "Ça varie beaucoup" sans chiffres précis

**Pourquoi c'est important :** Les utilisateurs abandonnent si c'est trop lent (> 10 sec).

---

### 3. À quelle fréquence l'IA plante ou est indisponible ?

**Bonne réponse :** "Disponibilité de 99.2% le mois dernier. 2 incidents de 30 min chacun."

**Signal d'alerte :** "Je ne sais pas" ou "On n'a pas mesuré"

**Pourquoi c'est important :** Une IA inaccessible = utilisateurs frustrés = abandon.

---

### 4. Sur quoi l'IA se trompe le plus souvent ?

**Bonne réponse :** "Les questions ambiguës (15% d'erreur) et les cas multi-langues (12% d'erreur)."

**Signal d'alerte :** "Elle se trompe rarement" sans analyse des erreurs

**Pourquoi c'est important :** Connaître les faiblesses permet de les corriger ou de prévenir les utilisateurs.

---

### 5. Comment savez-vous si la performance se dégrade ?

**Bonne réponse :** "On monitore quotidiennement la précision et le temps de réponse. Alerte si < 80%."

**Signal d'alerte :** "On verra bien si les utilisateurs se plaignent"

**Pourquoi c'est important :** La performance peut se dégrader silencieusement (drift).

---

### 6. L'IA a-t-elle été testée sur des cas extrêmes ?

**Bonne réponse :** "Oui, 50 cas limites testés : questions très longues, langues mixtes, fautes d'orthographe..."

**Signal d'alerte :** "On a testé les cas normaux"

**Pourquoi c'est important :** Les utilisateurs réels ne suivent pas les scripts parfaits.

---

## Questions sur les Données (6 questions)

### 7. Sur quelles données l'IA a-t-elle été entraînée ?

**Bonne réponse :** "2 ans d'historique de tickets SAV (45k conversations), nettoyées et validées."

**Signal d'alerte :** "Des données du web" ou réponse vague sur la source

**Pourquoi c'est important :** Données de mauvaise qualité = IA de mauvaise qualité.

---

### 8. Les données d'entraînement sont-elles représentatives de notre usage réel ?

**Bonne réponse :** "Oui, même distribution de sujets. 40% livraison, 30% retours, 30% produits."

**Signal d'alerte :** "On pense que oui" sans vérification

**Pourquoi c'est important :** Si l'IA apprend sur des données différentes de l'usage réel, elle sera mauvaise.

---

### 9. Comment protégez-vous les données personnelles ?

**Bonne réponse :** "Anonymisation avant entraînement, chiffrement au repos, accès loggé, conformité RGPD validée."

**Signal d'alerte :** "On fait attention" sans mesures concrètes

**Pourquoi c'est important :** Risque légal et réputationnel majeur.

---

### 10. L'IA peut-elle divulguer des informations confidentielles ?

**Bonne réponse :** "Non, filtres en place. Testé avec 100 tentatives d'extraction, 0 fuite."

**Signal d'alerte :** "En principe non" ou "On n'a pas testé"

**Pourquoi c'est important :** Une fuite de données = crise majeure.

---

### 11. Comment mettez-vous à jour les connaissances de l'IA ?

**Bonne réponse :** "Mise à jour mensuelle avec les nouveaux produits/procédures. Validation avant déploiement."

**Signal d'alerte :** "C'est figé" ou "On verra plus tard"

**Pourquoi c'est important :** Une IA avec des infos obsolètes perd en crédibilité.

---

### 12. Y a-t-il des biais dans les données ?

**Bonne réponse :** "Analysé : sur-représentation clients premium. Compensé par rééchantillonnage."

**Signal d'alerte :** "Quels biais ?" ou "On n'a pas vérifié"

**Pourquoi c'est important :** Biais = discrimination = risque éthique et légal.

---

## Questions sur la Fiabilité (6 questions)

### 13. Que se passe-t-il si l'IA plante ?

**Bonne réponse :** "Basculement automatique vers support humain en 30 sec. Utilisateur prévenu."

**Signal d'alerte :** "L'utilisateur verra une erreur"

**Pourquoi c'est important :** Les pannes arrivent. Votre plan de secours doit être prêt.

---

### 14. Pouvez-vous revenir à la version précédente rapidement ?

**Bonne réponse :** "Oui, rollback en 5 minutes. Testé le mois dernier."

**Signal d'alerte :** "En théorie oui" ou "C'est compliqué"

**Pourquoi c'est important :** Si nouvelle version = catastrophe, vous devez pouvoir revenir en arrière.

---

### 15. Comment détectez-vous les hallucinations ?

**Bonne réponse :** "Vérification automatique contre base de connaissances. Alerte si confiance < 70%."

**Signal d'alerte :** "Les utilisateurs nous le signalent"

**Pourquoi c'est important :** L'IA qui invente des infos fausses détruit la confiance.

---

### 16. L'IA sait-elle dire "je ne sais pas" ?

**Bonne réponse :** "Oui, si confiance < 60%, elle répond 'Je préfère vous transférer à un conseiller'."

**Signal d'alerte :** "Elle essaie toujours de répondre"

**Pourquoi c'est important :** Mieux vaut ne pas répondre que répondre faux.

---

### 17. Combien de conversations par jour peut-elle gérer ?

**Bonne réponse :** "Testé jusqu'à 10k requêtes/heure sans dégradation. Notre pic est 2k/heure."

**Signal d'alerte :** "On n'a pas testé la charge"

**Pourquoi c'est important :** Si succès = saturation = panne au pire moment.

---

### 18. Les logs sont-ils conservés pour analyse ?

**Bonne réponse :** "Oui, 6 mois de logs. Dashboard de suivi. Revue hebdomadaire des erreurs."

**Signal d'alerte :** "On ne logge pas tout"

**Pourquoi c'est important :** Sans logs, impossible de diagnostiquer les problèmes.

---

## Questions sur les Coûts (6 questions)

### 19. Combien coûte chaque requête à l'IA ?

**Bonne réponse :** "0.02€ par requête en moyenne. À 10k requêtes/jour = 200€/jour."

**Signal d'alerte :** "C'est inclus dans la licence" sans détail

**Pourquoi c'est important :** Les coûts peuvent exploser avec le volume.

---

### 20. Quels sont les coûts cachés ?

**Bonne réponse :** "Infrastructure : 500€/mois. Maintenance : 0.5 ETP. Réentraînement : 2k€/trimestre."

**Signal d'alerte :** "Juste la licence IA"

**Pourquoi c'est important :** Le vrai coût est souvent 3x la licence.

---

### 21. Comment le coût évolue-t-il avec le volume ?

**Bonne réponse :** "Linéaire jusqu'à 50k req/jour, puis palier. Économies d'échelle au-delà."

**Signal d'alerte :** "Ça devrait être pareil"

**Pourquoi c'est important :** Votre succès peut tuer votre budget.

---

### 22. Quel est le coût si on doit tout arrêter ?

**Bonne réponse :** "Préavis 3 mois sur licence. Données exportables. Transition estimée à 20k€."

**Signal d'alerte :** "On n'y a pas pensé"

**Pourquoi c'est important :** Le lock-in vendor peut coûter très cher.

---

### 23. Combien pour corriger un bug critique ?

**Bonne réponse :** "Équipe dédiée. Correction < 4h. Inclus dans support. Historique : 2 bugs critiques en 6 mois."

**Signal d'alerte :** "Ça dépend de notre disponibilité"

**Pourquoi c'est important :** Un bug critique non corrigé = business arrêté.

---

### 24. Combien d'heures par mois pour maintenir l'IA ?

**Bonne réponse :** "20h/mois : monitoring (10h), corrections (5h), mises à jour (5h)."

**Signal d'alerte :** "Presque rien, c'est automatique"

**Pourquoi c'est important :** Sous-estimer la maintenance = dette technique.

---

## Questions sur les Risques (6 questions)

### 25. Quels sont les 3 risques majeurs identifiés ?

**Bonne réponse :** "1) Dégradation performance sans MAJ, 2) Pic de charge non anticipé, 3) Changement API fournisseur."

**Signal d'alerte :** "Il n'y a pas vraiment de risque"

**Pourquoi c'est important :** Pas de risque identifié = risque non géré.

---

### 26. Que se passe-t-il si le fournisseur d'IA ferme ?

**Bonne réponse :** "Plan B : migration vers alternative en 2 mois. Code portable. Données exportables."

**Signal d'alerte :** "On verra le moment venu"

**Pourquoi c'est important :** Dépendance fournisseur = vulnérabilité.

---

### 27. L'IA peut-elle être manipulée par des utilisateurs malveillants ?

**Bonne réponse :** "Tests de sécurité réalisés. Injection de prompts bloquée. Rate limiting en place."

**Signal d'alerte :** "Nos utilisateurs sont internes"

**Pourquoi c'est important :** Même les utilisateurs internes peuvent faire des erreurs ou être malveillants.

---

### 28. Comment gérez-vous une crise (IA dit quelque chose d'inapproprié) ?

**Bonne réponse :** "Procédure : alerte immédiate, suspension temporaire, analyse, communication. Testé en simulation."

**Signal d'alerte :** "On réagira"

**Pourquoi c'est important :** Une crise mal gérée = réputation détruite.

---

### 29. L'IA respecte-t-elle les réglementations de notre secteur ?

**Bonne réponse :** "Validé avec juridique. Conforme [réglementation spécifique]. Audit externe prévu Q2."

**Signal d'alerte :** "C'est juste un outil interne"

**Pourquoi c'est important :** Non-conformité = amendes et sanctions.

---

### 30. Quand prévoyez-vous une obsolescence de cette IA ?

**Bonne réponse :** "Durée de vie estimée : 2-3 ans. Technologies alternatives surveillées. Budget évolution prévu."

**Signal d'alerte :** "C'est la dernière technologie"

**Pourquoi c'est important :** L'IA évolue vite. Prévoir l'obsolescence évite les surprises.

---

## Comment Interpréter les Réponses

### Comptez les Signaux d'Alerte

| Nombre | Interprétation | Action |
|--------|----------------|--------|
| **0-3** | ✅ Équipe mature | Confiance élevée |
| **4-8** | ⚠️ Points à clarifier | Demandez des précisions |
| **9-15** | 🟡 Lacunes significatives | Renforcez avant déploiement |
| **16+** | 🔴 Risque majeur | Reconsidérez le projet |

### Questions les Plus Critiques

Si vous n'avez le temps que pour 5 questions, posez :
- #1 (Précision)
- #10 (Fuites données)
- #14 (Rollback)
- #19 (Coût par requête)
- #25 (Risques identifiés)

---

## Template de Questionnaire

**Projet :** [Nom]
**Date :** [Date]
**Équipe interrogée :** [Noms]

| # | Question | Réponse | Alerte ? |
|---|----------|---------|----------|
| 1 | Précision ? | | ☐ |
| 2 | Temps réponse ? | | ☐ |
| ... | ... | | ☐ |

**Score final :** [ ] / 30 réponses satisfaisantes

**Recommandation :**

---

*Ces questions ne font pas de vous un expert technique. Elles font de vous un manager informé qui pose les bonnes questions.*
