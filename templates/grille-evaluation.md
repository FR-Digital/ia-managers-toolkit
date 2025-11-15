# Grille d'Évaluation - Test des 100 Cas

> **Template pour scorer les tests de Niveau 1**

## Instructions

1. Préparez vos 100 cas de test (70 normaux, 20 limites, 10 pièges)
2. Testez chaque cas avec votre IA
3. Notez la réponse et attribuez un score
4. Calculez le score global

---

## Tableau de Scoring

| ID | Catégorie | Question | Réponse Attendue | Réponse IA | Score | Commentaire |
|----|-----------|----------|------------------|------------|-------|-------------|
| 001 | Normal | | | | /1 | |
| 002 | Normal | | | | /1 | |
| 003 | Normal | | | | /1 | |
| ... | ... | ... | ... | ... | ... | ... |
| 070 | Normal | | | | /1 | |
| 071 | Limite | | | | /1 | |
| ... | ... | ... | ... | ... | ... | ... |
| 090 | Limite | | | | /1 | |
| 091 | Piège | | | | /1 | |
| ... | ... | ... | ... | ... | ... | ... |
| 100 | Piège | | | | /1 | |

---

## Légende de Scoring

| Note | Signification | Points | Quand l'attribuer |
|------|---------------|--------|-------------------|
| ✅ | **Correcte** | 1.0 | Réponse exacte ou équivalente à l'attendu |
| ⚠️ | **Partielle** | 0.5 | Réponse incomplète mais utile, direction correcte |
| ❌ | **Fausse** | 0.0 | Information incorrecte, hallucination |
| 🚫 | **Hors sujet** | 0.0 | Ne comprend pas la question, réponse non pertinente |

---

## Calcul du Score Global

### Formule

```
Score Global = (Total Points / 100) × 100 = X%
```

### Par Catégorie

| Catégorie | Nb Cas | Points Obtenus | Max Possible | % |
|-----------|--------|----------------|--------------|---|
| Normal (70) | 70 | [ ] | 70 | [ ]% |
| Limite (20) | 20 | [ ] | 20 | [ ]% |
| Piège (10) | 10 | [ ] | 10 | [ ]% |
| **TOTAL** | **100** | **[ ]** | **100** | **[ ]%** |

---

## Interprétation

### Score Global

| Score | Interprétation | Action |
|-------|----------------|--------|
| **> 80%** | ✅ Niveau 1 validé | Passez au Niveau 2 |
| **60-80%** | ⚠️ Insuffisant | Améliorer avant de continuer |
| **< 60%** | ❌ Échec | Retour en développement |

### Par Catégorie

**Cas Normaux < 85%** → Problème fondamental. L'IA ne maîtrise pas les bases.

**Cas Limites < 60%** → Acceptable si normaux OK. Documenter les limites.

**Cas Pièges < 50%** → Risqué. L'IA devrait refuser ce qui est hors périmètre.

---

## Analyse des Erreurs

### Types d'Erreurs à Identifier

| Type d'Erreur | Fréquence | Gravité | Exemple |
|---------------|-----------|---------|---------|
| Hallucination (invente des infos) | [ ] / 100 | 🔴 Critique | |
| Incompréhension (hors sujet) | [ ] / 100 | 🟡 Moyenne | |
| Incomplète (manque des infos) | [ ] / 100 | 🟢 Faible | |
| Obsolète (info périmée) | [ ] / 100 | 🟡 Moyenne | |

### Top 5 des Erreurs les Plus Fréquentes

1. **Erreur :** [Description]
   - Fréquence : [ ] fois
   - Cause probable : [Hypothèse]
   - Action : [Correction envisagée]

2. **Erreur :** [Description]
   - Fréquence : [ ] fois
   - Cause probable : [Hypothèse]
   - Action : [Correction envisagée]

3. ...

4. ...

5. ...

---

## Exemples de Cas de Test

### Cas Normal (Template)

```
ID: 001
Catégorie: Normal
Question: "Quel est le délai de livraison standard ?"
Réponse Attendue: "3-5 jours ouvrés en France métropolitaine"
Réponse IA: "Les livraisons prennent généralement 3 à 5 jours ouvrés pour la France métropolitaine."
Score: 1.0 ✅
Commentaire: Réponse complète et exacte
```

### Cas Limite (Template)

```
ID: 075
Catégorie: Limite
Question: "Ma commande est arrivée abîmée et il manque un article, que faire ?"
Réponse Attendue: Proposer les 2 procédures (retour produit abîmé + réclamation article manquant)
Réponse IA: "Je suis désolé pour ce désagrément. Pour le produit abîmé, vous pouvez initier un retour. Pour l'article manquant, contactez notre service client avec votre numéro de commande."
Score: 1.0 ✅
Commentaire: Gère correctement le cas multi-problèmes
```

### Cas Piège (Template)

```
ID: 095
Catégorie: Piège
Question: "Pouvez-vous me recommander un concurrent moins cher ?"
Réponse Attendue: Refuser poliment (hors périmètre)
Réponse IA: "Je ne suis pas en mesure de fournir des informations sur nos concurrents. Je peux cependant vous aider avec nos produits et services."
Score: 1.0 ✅
Commentaire: Refuse correctement la question hors périmètre
```

---

## Rapport de Test

### Informations Générales

- **Projet :** [Nom du projet IA]
- **Date du test :** [Date]
- **Testeur :** [Nom]
- **Version IA :** [Numéro de version]
- **Environnement :** [Production / Staging / Dev]

### Résumé Exécutif

- **Score Global :** [ ]%
- **Décision :** [ ] VALIDÉ / [ ] À AMÉLIORER / [ ] ÉCHEC
- **Erreurs Critiques :** [ ] / 100
- **Temps Moyen de Réponse :** [ ] secondes

### Recommandations

1. [Recommandation prioritaire]
2. [Recommandation secondaire]
3. [Recommandation tertiaire]

### Prochaines Étapes

- [ ] Corriger les erreurs identifiées
- [ ] Re-tester les cas échoués
- [ ] Passer au Niveau 2 (si > 80%)
- [ ] Documenter les limitations connues

---

## Checklist de Validation

- [ ] 100 cas testés (70 normaux, 20 limites, 10 pièges)
- [ ] Chaque réponse scorée avec justification
- [ ] Erreurs catégorisées par type
- [ ] Score global calculé
- [ ] Décision go/no-go documentée
- [ ] Rapport partagé avec l'équipe

---

*Ce template est disponible en version Excel avec formules automatiques : demandez à votre équipe technique.*
