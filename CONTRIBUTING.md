# Guide de Contribution

> Comment contribuer à l'IA Managers Toolkit

---

## Bienvenue !

Merci de votre intérêt pour contribuer à ce projet. Ce toolkit est un effort collectif pour démystifier l'IA auprès des managers et décideurs.

**Toutes les contributions sont les bienvenues**, que vous soyez :
- Manager ayant vécu un projet IA
- Data scientist voulant vulgariser
- Consultant partageant ses templates
- Lecteur ayant trouvé une erreur

---

## Types de Contributions

### 1. Partager un Cas Pratique

**Vous avez vécu un projet IA ?** Documentez-le !

**Format attendu :**
```markdown
# Cas Pratique : [Titre]

## Contexte
- Entreprise (anonymisée ou non)
- Département
- Durée et budget

## Problème Initial
- Situation avant
- Douleurs identifiées
- Impact business

## Solution
- Type d'IA choisi
- Architecture technique (simplifiée)
- Approche

## Résultats
- Métriques avant/après
- ROI réel
- Leçons apprises

## Conclusion
- Ce qui a marché
- Ce qui aurait pu être mieux
- Conseils pour reproduction
```

**Critères d'acceptation :**
- Anonymisation si nécessaire (nom entreprise, personnes)
- Chiffres réels (pas d'estimations floues)
- Honnêteté (les échecs sont aussi précieux)
- Format respecté

### 2. Améliorer le Contenu Existant

**Corrections bienvenues :**
- Fautes d'orthographe/grammaire
- Informations obsolètes
- Liens cassés
- Erreurs factuelles
- Clarifications nécessaires

### 3. Ajouter des Ressources

**Types acceptés :**
- Nouveaux termes pour le glossaire
- Liens vers formations de qualité
- Articles/études pertinents
- Outils pratiques

**Critères :**
- Ressources gratuites ou clairement indiquées comme payantes
- Qualité vérifiée (pas de spam/promo)
- Pertinence pour le public cible (managers non-techniques)

### 4. Proposer de Nouveaux Templates

**Templates utiles :**
- Nouveaux business cases
- Checklists spécialisées
- Grilles d'évaluation
- Rapports types

**Format :**
- Markdown avec sections claires
- Instructions d'utilisation
- Exemples remplis si possible

### 5. Traductions

**Langues prioritaires :**
- Anglais (principale)
- Espagnol
- Allemand

---

## Comment Contribuer

### Via GitHub (Recommandé)

1. **Fork** le repository
2. **Créez une branche** : `git checkout -b feature/mon-ajout`
3. **Faites vos modifications**
4. **Testez** : Vérifiez les liens, la syntaxe markdown
5. **Commitez** : `git commit -m "Ajout cas pratique chatbot RH"`
6. **Pushez** : `git push origin feature/mon-ajout`
7. **Ouvrez une Pull Request** avec description détaillée

### Via Issues

1. Allez dans l'onglet "Issues"
2. Cliquez "New Issue"
3. Choisissez le template approprié :
   - Bug/Erreur
   - Suggestion d'amélioration
   - Nouveau contenu
   - Question

### Via Email

Si vous n'êtes pas à l'aise avec GitHub :
- Envoyez votre contribution par email
- Format : Document Word/Google Doc ou texte simple
- Indiquez clairement où l'ajouter

---

## Standards de Qualité

### Rédaction

**Style attendu :**
- **Clair** : Pas de jargon non expliqué
- **Concis** : Aller à l'essentiel
- **Actionnable** : Le lecteur peut agir
- **Honnête** : Pas de survente de l'IA
- **Structuré** : Titres, listes, tableaux

**À éviter :**
- Termes techniques sans explication
- Phrases de plus de 3 lignes
- Contenus promotionnels
- Affirmations sans sources
- Ton condescendant

### Formatage Markdown

```markdown
# Titre Principal (H1)

## Section (H2)

### Sous-section (H3)

**Texte en gras** pour les points importants

*Texte en italique* pour les nuances

- Listes à puces pour les énumérations
- Comme ceci

1. Listes numérotées pour les étapes
2. Ordonnées

| Tableau | Pour | Comparaisons |
|---------|------|--------------|
| Données | Ici | Là |

`Code inline` pour les termes techniques

> Citation ou remarque importante

[Lien](url) pour les références

---

Séparateur horizontal pour changer de sujet majeur
```

### Structure des Fichiers

```
nom-du-fichier.md
│
├── Titre Principal
│
├── Introduction / Contexte
│   └── Pourquoi ce contenu
│
├── Corps Principal
│   ├── Section 1
│   ├── Section 2
│   └── Section 3
│
├── Exemples / Cas Pratiques
│
├── Ressources / Liens
│
└── Métadonnées
    └── Date, sources, auteur
```

---

## Processus de Review

### Pour les Petites Corrections
- Review automatique par maintainer
- Merge sous 48-72h si approuvé
- Pas de discussion nécessaire

### Pour les Nouveaux Contenus
1. **Review initiale** : Vérification du format
2. **Review de fond** : Exactitude des informations
3. **Feedback** : Suggestions d'amélioration si nécessaire
4. **Approbation** : Validation par 1-2 maintainers
5. **Merge** : Intégration au projet

**Délai typique :** 1-2 semaines

### Critères de Review

**Nous vérifions :**
- [ ] Format markdown correct
- [ ] Pas de fautes majeures
- [ ] Liens fonctionnels
- [ ] Informations vérifiables
- [ ] Cohérence avec le reste du projet
- [ ] Valeur ajoutée pour le lecteur
- [ ] Pas de contenu promotionnel
- [ ] Respect de la cible (managers non-tech)

---

## Propriété Intellectuelle

### Votre Contribution

- Vous conservez les droits sur votre contenu
- Vous accordez une licence pour l'utilisation dans le projet
- Le projet reste sous licence MIT

### Contenu Tiers

- Citez toujours vos sources
- Respectez les copyrights
- Pas de copier-coller sans attribution
- Préférez les reformulations avec vos mots

---

## Code de Conduite

### Nous Encourageons

- Feedback constructif
- Questions (pas de questions bêtes)
- Partage d'expériences réelles
- Critiques argumentées
- Suggestions d'amélioration

### Nous Décourageons

- Contenu promotionnel déguisé
- Informations non vérifiées
- Manque de respect
- Discrimination
- Spam

---

## Questions Fréquentes

**Q: Mon cas est confidentiel, puis-je quand même le partager ?**
R: Oui, anonymisez l'entreprise et les personnes. Les patterns sont plus importants que les noms.

**Q: Je ne suis pas expert IA, puis-je contribuer ?**
R: Absolument ! Votre regard de non-expert est précieux pour la clarté.

**Q: Mon entreprise a échoué un projet IA, c'est utile ?**
R: Très utile ! Les échecs sont des apprentissages précieux.

**Q: Je veux juste corriger une faute, c'est trop petit ?**
R: Aucune contribution n'est trop petite. Merci !

**Q: Puis-je traduire le contenu ?**
R: Oui, les traductions sont bienvenues. Contactez-nous d'abord pour coordination.

---

## Contact

- **Issues GitHub** : Pour les questions techniques
- **Discussions** : Pour les échanges généraux
- **Email** : [À définir]

---

## Remerciements

Merci à tous les contributeurs qui rendent ce projet meilleur !

---

*Guide de contribution | Nov 2025*
