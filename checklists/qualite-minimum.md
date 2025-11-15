# Checklist Qualité Minimum

> **Ce qu'il FAUT avoir avant de lancer votre IA en production**

## Pourquoi cette checklist ?

Avant de déployer une IA, certains éléments sont **non négociables**. Cette checklist vous évite les erreurs classiques qui tuent les projets.

---

## Critères Techniques (Non Négociables)

### Performance

- [ ] **Précision > 80%** sur cas de test standards
- [ ] **Temps de réponse < 5 secondes** pour 95% des requêtes
- [ ] **Disponibilité > 95%** (pas de plantages fréquents)
- [ ] **Pas d'hallucinations critiques** (données fausses sur sujets importants)

### Sécurité

- [ ] **Données sensibles protégées** (pas d'exposition d'infos confidentielles)
- [ ] **Authentification en place** (qui accède à quoi)
- [ ] **Logs de sécurité actifs** (traçabilité des actions)
- [ ] **Conformité RGPD** (si données personnelles)

### Fiabilité

- [ ] **Plan de rollback** (pouvoir revenir en arrière si problème)
- [ ] **Monitoring actif** (alertes en cas de dysfonctionnement)
- [ ] **Backup des données** (sauvegarde régulière)
- [ ] **Documentation technique** (comment ça marche)

---

## Critères Utilisateur (Essentiels)

### Expérience

- [ ] **Interface intuitive** (pas besoin de formation complexe)
- [ ] **Messages d'erreur clairs** (l'utilisateur comprend ce qui se passe)
- [ ] **Feedback visible** (l'IA indique qu'elle traite la requête)
- [ ] **Option de recours** (contacter un humain si besoin)

### Adoption

- [ ] **Beta test réalisé** avec vrais utilisateurs (minimum 10)
- [ ] **Satisfaction > 3/5** sur sondage pilote
- [ ] **Documentation utilisateur** disponible
- [ ] **Support identifié** (qui appeler en cas de problème)

---

## Critères Business (Importants)

### Gouvernance

- [ ] **Responsable identifié** (qui est accountable du projet)
- [ ] **Budget maintenance prévu** (coûts récurrents anticipés)
- [ ] **KPIs définis** (comment mesurer le succès)
- [ ] **Revue planifiée** (date de réévaluation prévue)

### Légal & Éthique

- [ ] **Biais vérifiés** (l'IA ne discrimine pas)
- [ ] **Transparence** (les utilisateurs savent qu'ils parlent à une IA)
- [ ] **Conformité réglementaire** (lois sectorielles respectées)
- [ ] **Propriété intellectuelle** clarifiée

---

## Comment Utiliser cette Checklist

### Avant le Go/No-Go

1. Parcourez chaque critère avec votre équipe technique
2. Cochez uniquement si vous avez une preuve concrète
3. Documentez les exceptions (et pourquoi vous les acceptez)

### Règles de Décision

| Situation | Décision |
|-----------|----------|
| **Tous les Non Négociables** ✅ | Vous pouvez déployer |
| **1+ Non Négociable** ❌ | **STOP** - Réglez d'abord |
| **Essentiels à 80%** ✅ | OK avec plan d'amélioration |
| **Importants à 50%** ✅ | OK mais risque accru |

### Ce qui Peut Être Dérogé (avec justification)

- Satisfaction > 3/5 (si feedback en cours de collecte)
- Documentation complète (si équipe formée verbalement)
- Certains critères "Importants" (si risque accepté par direction)

### Ce qui NE PEUT PAS Être Dérogé

- Précision > 80%
- Pas d'hallucinations critiques
- Sécurité des données
- Plan de rollback

---

## Template de Validation

**Projet :** [Nom du projet]
**Date de validation :** [Date]
**Validé par :** [Nom + Fonction]

**Score :**
- Non Négociables : [ ] / 12
- Essentiels : [ ] / 8
- Importants : [ ] / 8

**Décision :** [ ] GO / [ ] NO-GO / [ ] GO avec réserves

**Réserves (si applicable) :**
- [Critère manquant] → [Plan de correction] → [Date limite]

**Signature :** _______________

---

## Signaux d'Alerte

### 🚨 Ne déployez JAMAIS si :

- L'équipe technique ne peut pas expliquer comment fonctionne l'IA
- Aucun test avec de vrais utilisateurs n'a été fait
- Personne ne sait qui est responsable si ça plante
- Le coût de maintenance n'est pas budgété
- L'IA donne des réponses fausses sur des sujets critiques

### ⚠️ Soyez vigilant si :

- La satisfaction beta est juste au-dessus du seuil (3.1/5)
- L'équipe est pressée de déployer sans tests complets
- On vous dit "on corrigera après le lancement"
- Les métriques de performance sont "en cours de calcul"

---

## Ressources Associées

- **[Framework 3 Niveaux](../frameworks/3-niveaux-evaluation.md)** - Évaluation complète
- **[Checklist Pré-Production](pre-production.md)** - Vérifications techniques détaillées
- **[Critères Go/No-Go](../guides/criteres-go-production.md)** - Matrice de décision

---

*La qualité minimum n'est pas la qualité idéale. C'est le plancher en dessous duquel vous prenez des risques inacceptables.*
