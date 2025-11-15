# Types d'IA Expliqués pour Managers

> Comprendre les différentes catégories d'IA et leurs applications business.

## Vue d'Ensemble

Il n'existe pas "une" IA mais **plusieurs types**, chacun adapté à des problèmes différents. Choisir le bon type est crucial pour le succès de votre projet.

```
                    Intelligence Artificielle
                            │
            ┌───────────────┼───────────────┐
            │               │               │
        IA Prédictive   IA de Perception  IA Générative
            │               │               │
       Machine Learning  Computer Vision    LLM
       Deep Learning     Speech Recognition GenAI
```

---

## 1. IA Prédictive (Machine Learning)

### Ce que c'est
Analyse des données historiques pour **prédire des outcomes futurs** ou **classifier des données**.

### Sous-catégories

#### Apprentissage Supervisé
- **Principe :** On montre des exemples avec les bonnes réponses
- **Exemple :** 10 000 emails étiquetés spam/pas spam
- **Usage :** Classification, régression, prédiction

#### Apprentissage Non Supervisé
- **Principe :** L'IA trouve les patterns sans étiquettes
- **Exemple :** Segmenter les clients par comportement
- **Usage :** Clustering, détection d'anomalies

#### Apprentissage par Renforcement
- **Principe :** L'IA apprend par essai-erreur avec récompenses
- **Exemple :** Optimisation de prix dynamique
- **Usage :** Optimisation, jeux, robotique

### Applications Business Concrètes

| Cas d'Usage | Description | Données Nécessaires |
|-------------|-------------|---------------------|
| **Prédiction de churn** | Identifier les clients qui vont partir | Historique client, transactions, interactions |
| **Scoring crédit** | Évaluer le risque d'un emprunteur | Données financières, historique paiements |
| **Prévision de ventes** | Estimer les ventes futures | Historique ventes, saisonnalité, promotions |
| **Détection fraude** | Repérer les transactions suspectes | Patterns de transactions normales/frauduleuses |
| **Maintenance prédictive** | Prévoir les pannes équipement | Données capteurs, historique pannes |

### Prérequis
- **Données :** Minimum 1 000-10 000 exemples de qualité
- **Équipe :** Data scientist + data engineer
- **Infrastructure :** Serveur avec GPU pour l'entraînement
- **Timeline :** 3-6 mois pour un POC

### Avantages / Inconvénients

**Avantages :**
- Très précis sur les patterns répétitifs
- Explicable (on peut comprendre les décisions)
- Coût raisonnable en production

**Inconvénients :**
- Nécessite beaucoup de données historiques
- Ne gère pas bien les cas jamais vus
- Ré-entraînement nécessaire quand les données changent

---

## 2. IA de Perception (Computer Vision / NLP)

### Ce que c'est
L'IA "voit", "entend" ou "lit" comme un humain. Analyse d'images, de sons ou de textes.

### Sous-catégories

#### Computer Vision (Vision par Ordinateur)
- **Principe :** Analyser et comprendre les images/vidéos
- **Exemples :** Reconnaissance d'objets, OCR, détection de défauts

#### Speech Recognition (Reconnaissance Vocale)
- **Principe :** Convertir la parole en texte
- **Exemples :** Assistants vocaux, transcription automatique

#### NLP Classique (Natural Language Processing)
- **Principe :** Analyser et comprendre le texte
- **Exemples :** Analyse de sentiment, extraction d'entités, classification de documents

### Applications Business Concrètes

| Cas d'Usage | Type | Description |
|-------------|------|-------------|
| **Contrôle qualité** | Vision | Détecter les défauts sur ligne de production |
| **OCR Documents** | Vision | Extraire les infos des factures automatiquement |
| **Analyse sentiment** | NLP | Classifier les avis clients positifs/négatifs |
| **Transcription réunions** | Speech | Compte-rendu automatique des meetings |
| **Modération contenu** | Vision/NLP | Filtrer les contenus inappropriés |

### Prérequis
- **Données :** 5 000+ images annotées (vision) ou textes étiquetés (NLP)
- **Équipe :** Spécialiste CV ou NLP
- **Infrastructure :** GPU puissants (surtout pour vision)
- **Timeline :** 4-8 mois pour un POC

### Avantages / Inconvénients

**Avantages :**
- Automatise des tâches visuelles/linguistiques répétitives
- Précision souvent supérieure à l'humain pour tâches simples
- Scalable (peut traiter des millions d'images/documents)

**Inconvénients :**
- Annotation coûteuse et longue
- Sensible aux conditions (éclairage, qualité image/audio)
- Modèles lourds (GPU nécessaires)

---

## 3. IA Générative (GenAI / LLM)

### Ce que c'est
L'IA **crée du nouveau contenu** : texte, images, code, musique. C'est la révolution actuelle avec ChatGPT, Midjourney, etc.

### Sous-catégories

#### Large Language Models (LLM)
- **Principe :** Modèles entraînés sur des milliards de textes
- **Exemples :** GPT-4, Claude, Llama, Mistral
- **Usage :** Génération de texte, chatbots, résumés

#### Text-to-Image
- **Principe :** Générer des images à partir de descriptions
- **Exemples :** DALL-E, Midjourney, Stable Diffusion
- **Usage :** Création visuelle, prototypage

#### Code Generation
- **Principe :** Générer du code à partir de descriptions
- **Exemples :** GitHub Copilot, Claude Code
- **Usage :** Assistance développement, automatisation

### Applications Business Concrètes

| Cas d'Usage | Description | Exemple |
|-------------|-------------|---------|
| **Chatbot intelligent** | Support client conversationnel | Répondre aux questions FAQ avec contexte |
| **Génération contenu** | Créer des textes marketing | Rédiger des descriptions produits |
| **Résumé automatique** | Synthétiser des documents longs | Résumer des rapports de 100 pages |
| **Assistance rédaction** | Aider à écrire des emails/rapports | Reformuler, corriger, structurer |
| **Analyse de documents** | Extraire des insights de textes | Analyser des contrats juridiques |

### Modes d'Utilisation

#### 1. API Cloud (OpenAI, Anthropic, Google)
- **Avantage :** Simple, rapide à démarrer
- **Inconvénient :** Données envoyées au fournisseur, coût variable
- **Coût :** ~0.01-0.03€ par 1000 tokens

#### 2. Fine-tuning
- **Avantage :** Modèle adapté à votre domaine
- **Inconvénient :** Nécessite expertise et données
- **Coût :** 10k-50k€ + temps d'entraînement

#### 3. RAG (Retrieval Augmented Generation)
- **Avantage :** Utilise vos documents sans ré-entraînement
- **Inconvénient :** Setup complexe
- **Coût :** 20k-100k€ de développement

### Prérequis
- **Données :** Vos documents métier (pour RAG/fine-tuning)
- **Équipe :** ML Engineer ou dev backend + prompt engineer
- **Infrastructure :** Cloud suffisant pour héberger (on-premise) ou budget API
- **Timeline :** 1-3 mois pour POC avec API, 3-6 mois pour fine-tuning

### Avantages / Inconvénients

**Avantages :**
- Très polyvalent (texte, code, analyse)
- Rapide à prototyper (API)
- Interface naturelle (conversation)

**Inconvénients :**
- Hallucinations (invente des faits)
- Coût API peut exploser
- Confidentialité des données (si cloud)
- Besoin de supervision humaine

---

## 4. IA Hybride

### Ce que c'est
Combine plusieurs types d'IA pour un système complet.

### Exemples

**Système de Support Client Intelligent :**
1. Speech Recognition → Transcrire l'appel
2. NLP → Comprendre l'intention
3. LLM → Générer la réponse
4. ML Prédictif → Scorer la satisfaction

**Analyse Automatique de Contrats :**
1. OCR → Lire le PDF scanné
2. NLP → Extraire les clauses clés
3. ML Classification → Identifier les risques
4. LLM → Résumer en langage simple

---

## Comment Choisir le Bon Type ?

### Arbre de Décision

```
Quel est votre objectif ?
│
├─ Prédire/Classifier → IA Prédictive (ML)
│   ├─ Ai-je des données historiques étiquetées ?
│   │   ├─ OUI → Supervised Learning
│   │   └─ NON → Unsupervised Learning
│   └─ Le problème est-il d'optimisation ?
│       └─ OUI → Reinforcement Learning
│
├─ Analyser images/audio/texte → IA de Perception
│   ├─ Images/Vidéos → Computer Vision
│   ├─ Audio → Speech Recognition
│   └─ Texte (analyse) → NLP Classique
│
└─ Générer du contenu → IA Générative
    ├─ Texte/Chat → LLM (GPT, Claude)
    ├─ Images → Text-to-Image (DALL-E, Midjourney)
    └─ Code → Code Generation (Copilot)
```

### Matrice de Décision

| Besoin | Type Recommandé | Effort | Coût |
|--------|----------------|--------|------|
| Prédire qui va churner | ML Supervisé | Moyen | €€ |
| Segmenter les clients | ML Non Supervisé | Moyen | €€ |
| Contrôle qualité visuel | Computer Vision | Élevé | €€€ |
| Chatbot FAQ | LLM + RAG | Faible-Moyen | €-€€ |
| Générer des rapports | LLM | Faible | € |
| Analyser des sentiments | NLP Classique | Moyen | €€ |

---

## Red Flags par Type d'IA

### IA Prédictive
- "On n'a que 100 exemples" → Pas assez
- "Les données ont 5 ans" → Trop vieilles
- "On ne sait pas ce qu'on veut prédire" → Objectif flou

### IA de Perception
- "On a des images de qualité variable" → Risque de mauvaise performance
- "Les annotations sont faites vite fait" → Garbage in, garbage out
- "On veut détecter des choses jamais vues" → Impossible

### IA Générative
- "L'IA doit être 100% fiable" → Impossible (hallucinations)
- "Pas de budget pour les APIs" → Coûtera cher en volume
- "On ne veut pas superviser les réponses" → Risque élevé

---

## Pour Aller Plus Loin

- [Comprendre l'IA en 10 min](comprendre-ia-en-10min.md) - Les bases
- [Questions à poser](../evaluation/questions-equipe-tech.md) - Valider le choix technique
- [Lancer un projet IA](../pilotage/lancer-projet-ia.md) - Guide de démarrage

---

*4 types d'IA expliqués | Dernière MAJ : Nov 2025*
