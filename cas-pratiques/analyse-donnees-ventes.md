# Cas Pratique : Analyse Prédictive des Ventes

> Retour d'expérience sur un projet de prédiction de ventes avec Machine Learning - **un échec instructif**.

---

## Contexte

**Entreprise :** Distributeur B2B (matériel industriel, 80 employés)
**Département :** Commercial / Direction
**Durée projet :** 6 mois (Février - Juillet 2024) - **Arrêté prématurément**
**Budget consommé :** 78k€ sur 120k€ prévus

---

## Le Problème Initial

### Situation Avant Projet

**Équipe commerciale :**
- 15 commerciaux terrain
- 3000 clients actifs
- CA : 25M€/an
- Prévisions de ventes : Fait manuellement par les commerciaux

**Douleurs identifiées :**
1. **Prévisions peu fiables** : Écart de 25% entre prévision et réalité
2. **Stocks mal gérés** : Sur-stock ou ruptures fréquentes
3. **Opportunités manquées** : Pas de visibilité sur les clients à potentiel
4. **Décisions au feeling** : Peu de data-driven

**Impact business estimé :**
- Coût des stocks excédentaires : 180k€/an
- Ruptures de stock : 120k€/an de ventes perdues
- Total impact : 300k€/an

---

## La Solution Proposée

### Objectif Initial

Développer un modèle de prédiction des ventes à 3 mois pour :
1. Anticiper les commandes par client
2. Optimiser les stocks
3. Identifier les clients à fort potentiel
4. Améliorer les prévisions globales

### Type d'IA Choisi

**Architecture :** Machine Learning supervisé (régression + classification)

**Stack technique :**
- Algorithmes : XGBoost, Random Forest
- Features : Historique ventes, saisonnalité, données marché
- Infrastructure : Cloud Azure
- Intégration : Dashboard Power BI

**ROI projeté :** 250% sur 3 ans (optimiste, on le verra)

---

## Déroulement du Projet

### Phase 1 : Cadrage (4 semaines) - 12k€

**Activités :**
- Audit des données disponibles
- Définition des KPIs
- Identification des sources de données
- Business case

**Découvertes :**
- Historique de ventes : 5 ans dans l'ERP ✅
- Données clients : Secteur, taille, localisation ✅
- Données produits : Catégories, prix, marge ✅
- Données externes : Tendances marché, concurrence ❌ Non disponibles

**Red flags ignorés (avec le recul) :**
- Données historiques pas si propres
- 30% des clients avec historique < 1 an
- Saisonnalité complexe et mal documentée
- Équipe data inexistante en interne

**Décision :** GO POC malgré les signaux

---

### Phase 2 : POC (10 semaines) - 45k€

**Objectif POC :** Prédire les ventes à 3 mois avec < 15% d'erreur.

**Équipe :**
- 1 Data Scientist senior (externe, 100%)
- 1 Data Engineer (externe, 50%)
- 1 Chef de projet (interne, 30%)
- 1 Directeur commercial (interne, 10%)

**Activités :**
- Extraction et nettoyage des données (6 semaines !)
- Feature engineering
- Entraînement de modèles
- Évaluation sur données historiques

**Problèmes rencontrés :**

1. **Données sales**
   - Duplicates dans l'ERP
   - Clients avec multiples codes
   - Produits renommés sans traçabilité
   - 6 semaines au lieu de 2 pour nettoyer

2. **Manque de features explicatives**
   - Pas de données sur les actions commerciales
   - Pas d'historique des promotions
   - Pas de données concurrence
   - Contexte business non capturé

3. **Comportement client imprévisible**
   - 40% des gros clients = contrats annuels (pas de pattern)
   - Projets ponctuels importants (non prévisibles)
   - Influence forte du commercial (relation humaine)

**Résultats POC :**

| Métrique | Objectif | Obtenu | Verdict |
|----------|----------|--------|---------|
| Erreur moyenne (MAPE) | < 15% | 32% | ❌ |
| R² (corrélation) | > 0.7 | 0.45 | ❌ |
| Prédiction top clients | > 80% | 61% | ❌ |
| Prédiction produits | > 75% | 58% | ❌ |

**Analyse des erreurs :**
- Le modèle était bon pour la tendance générale
- Mais incapable de prédire les variations individuelles
- Les "gros coups" (projets majeurs) impossibles à anticiper
- La saisonnalité était mal capturée

**Hypothèses invalidées :**
- "On a assez de données" → Non, pas les bonnes données
- "Les patterns sont dans l'historique" → Trop de bruit
- "ML va trouver les corrélations" → Garbage in, garbage out

**Décision :** CONTINUER avec pivot (erreur)

---

### Phase 3 : Pivot (8 semaines) - 21k€

**Nouveau scope :** Se concentrer sur la segmentation clients plutôt que prédiction précise.

**Nouvel objectif :** Classifier les clients par potentiel (A/B/C) pour prioriser les efforts commerciaux.

**Activités :**
- Clustering des clients par comportement
- Scoring du potentiel
- Dashboard de visualisation

**Résultats :**

| Métrique | Objectif | Obtenu | Verdict |
|----------|----------|--------|---------|
| Précision classification | > 80% | 72% | ⚠️ |
| Accord avec commerciaux | > 75% | 55% | ❌ |
| Valeur ajoutée perçue | Haute | Faible | ❌ |

**Feedback commerciaux :**
- "Je connais déjà mes clients mieux que votre algo"
- "Les critères de l'IA ne correspondent pas à mon terrain"
- "Ça m'apprend rien que je ne sache déjà"

**Problème fondamental :**
L'expertise humaine des commerciaux (20 ans de relation) était supérieure au modèle basé sur des données incomplètes.

---

### Phase 4 : Arrêt du Projet

**Raisons de l'arrêt :**

1. **Performance insuffisante** : 32% d'erreur inacceptable pour piloter les stocks
2. **Pas d'adoption** : Les commerciaux n'utilisent pas l'outil
3. **ROI négatif** : Gains non prouvés, coûts réels
4. **Confiance perdue** : Direction sceptique sur la suite
5. **Coût d'opportunité** : Ressources mieux utilisées ailleurs

**Budget final :**
- Consommé : 78k€
- Restant non utilisé : 42k€
- Gains réalisés : ~0€
- **Perte sèche : 78k€**

---

## Analyse Post-Mortem

### Pourquoi Ça a Échoué

1. **Problème mal posé**
   - La prédiction de ventes B2B avec peu de transactions est fondamentalement difficile
   - Le ML excelle sur les patterns récurrents, pas sur les événements uniques
   - Les ventes B2B sont relationnelles, pas transactionnelles

2. **Données insuffisantes**
   - Pas les bonnes features (actions commerciales, contexte)
   - Qualité médiocre (nettoyage sous-estimé)
   - Volume insuffisant pour ML robuste

3. **Expertise métier sous-utilisée**
   - Les commerciaux pas assez impliqués au départ
   - Leur connaissance terrain ignorée
   - L'IA vue comme remplacement plutôt qu'augmentation

4. **Signaux d'alarme ignorés**
   - POC aurait dû être stop/pivot plus tôt
   - Espoir que "ça va s'améliorer" non justifié
   - Pression du management pour résultats

5. **Mauvaise estimation de la complexité**
   - Vendre de l'IA comme solution miracle
   - Sous-estimation du travail sur les données
   - Comparaison avec des cas B2C (Netflix, Amazon) non pertinente

---

## Leçons Apprises

### Ce qu'il fallait faire différemment

1. **Valider les données AVANT le business case**
   - Faire un audit data sérieux (2-3 semaines)
   - S'assurer qu'on a les bonnes features
   - Évaluer la qualité réelle, pas supposée

2. **Commencer par une baseline simple**
   - Comparer avec la moyenne mobile
   - Comparer avec le jugement humain
   - Si la baseline est bonne, ML n'apportera pas grand-chose

3. **Impliquer les experts métier plus tôt**
   - Quels facteurs influencent vraiment les ventes ?
   - L'IA peut-elle capturer ces facteurs ?
   - Le modèle a-t-il du sens métier ?

4. **Critères de stop clairs et respectés**
   - POC avec < 70% de l'objectif = STOP
   - Pas de continuation "au cas où"
   - Mieux vaut arrêter tôt que gaspiller plus

5. **Alternative à considérer : BI classique**
   - Dashboard de suivi des ventes
   - Alertes sur clients dormants
   - Rapports automatisés
   - ROI immédiat et certain

---

## Ce Qui Aurait Pu Marcher

### Approches Alternatives

1. **Recommandation produits (pas prédiction)**
   - "Ce client achète X, proposez-lui Y"
   - Basé sur les achats similaires
   - Aide au commercial, pas remplacement

2. **Détection d'anomalies**
   - Client qui achète moins qu'avant = alerte
   - Plus simple à implémenter
   - Valeur ajoutée claire

3. **Analyse RFM (Recency, Frequency, Monetary)**
   - Segmentation sans ML complexe
   - Règles métier simples
   - Compréhensible par tous

4. **BI avancée avant ML**
   - Dashboards interactifs
   - Tendances et comparaisons
   - Base solide pour ensuite faire du ML

---

## Impact Organisationnel

### Conséquences du Projet

**Négatif :**
- 78k€ de budget perdu
- 6 mois de temps management
- Confiance réduite dans l'IA
- Frustration équipe projet

**Positif (apprentissages) :**
- Meilleure compréhension des données
- Nettoyage ERP réalisé (utile pour autre chose)
- Maturité sur les projets IA
- Critères de succès plus réalistes

### Prochains Projets

**Nouvelles règles internes :**
1. Audit data obligatoire avant validation budget
2. Baseline simple à battre
3. Critères GO/NO-GO stricts et respectés
4. Budget contingence de 30%
5. Quick win avant gros projet

---

## Conseils pour Éviter Cet Échec

### Questions à Se Poser

1. **"Avons-nous les bonnes données ?"**
   - Pas juste beaucoup de données, les BONNES données
   - Les features qui expliquent vraiment le phénomène

2. **"Le ML est-il vraiment nécessaire ?"**
   - Une règle simple fait-elle l'affaire ?
   - L'expertise humaine est-elle déjà bonne ?

3. **"Le problème est-il prévisible ?"**
   - Patterns récurrents ou événements uniques ?
   - B2B relationnel ≠ B2C transactionnel

4. **"Quel est le plan B ?"**
   - Si le ML ne marche pas ?
   - Critères d'arrêt définis ?

5. **"Les utilisateurs en veulent-ils vraiment ?"**
   - Vont-ils l'utiliser ?
   - Apporte-t-il vraiment de la valeur ?

---

## Conclusion

Ce projet est un **échec financier** mais un **succès d'apprentissage**.

**Messages clés :**
- L'IA n'est pas magique
- Les données sont la fondation (sans elles, rien ne marche)
- L'expertise humaine reste précieuse
- Savoir arrêter un projet est une compétence
- Les échecs bien analysés évitent de reproduire les erreurs

**Morale :**
Un projet IA qui échoue rapidement avec des apprentissages capitalisés est meilleur qu'un projet qui traîne indéfiniment en gaspillant des ressources.

---

## Ressources

- [Quand arrêter un projet](../evaluation/quand-arreter-projet.md)
- [Mythes vs Réalité](../fondamentaux/mythes-vs-realite.md)
- [Questions équipe tech](../evaluation/questions-equipe-tech.md)

---

*Cas pratique prédiction ventes (échec) | Nov 2025*
