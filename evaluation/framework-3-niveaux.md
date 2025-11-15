# Framework d'Évaluation IA en 3 Niveaux

> Évaluer si votre projet IA fonctionne vraiment, sans être data scientist.

## Le Principe

Évaluer une IA, ce n'est pas juste vérifier si "ça marche". C'est répondre à **3 questions dans l'ordre** :

1. **Niveau 1 : Est-ce que ça marche ?** (Tests techniques)
2. **Niveau 2 : Est-ce que c'est utilisé ?** (Adoption)
3. **Niveau 3 : Est-ce que ça rapporte ?** (ROI)

**IMPORTANT :** Ne passez au niveau suivant que si le niveau précédent est validé.

---

## Niveau 1 : Est-ce que Ça Marche ?

### Objectif
Vérifier que l'IA fait ce qu'on lui demande techniquement.

### Questions Clés
- L'IA répond-elle aux requêtes ?
- Les réponses sont-elles correctes ?
- Le temps de réponse est acceptable ?

### Méthode : Test des 100 Cas

1. **Préparez 100 questions types** (avec réponses attendues)
   - 70 cas "normaux"
   - 20 cas "limites" (questions difficiles)
   - 10 cas "pièges" (hors périmètre)

2. **Posez-les à l'IA**

3. **Notez chaque réponse :**
   - ✅ **Correcte** = 1 point
   - ⚠️ **Partielle** = 0.5 point
   - ❌ **Fausse** = 0 point
   - 🚫 **Hors sujet** = 0 point

4. **Calculez le score**
   - Score > 80% → ✅ Niveau 1 validé
   - Score 60-80% → ⚠️ Améliorations nécessaires
   - Score < 60% → ❌ Retour en développement

### Exemple Concret : Chatbot SAV

**Cas normal :**
- Q: "Quel est votre délai de livraison ?"
- R attendue: "3-5 jours ouvrés"
- R IA: "Nos livraisons prennent 3 à 5 jours ouvrés"
- Note: ✅ 1 point

**Cas limite :**
- Q: "Je n'ai pas reçu ma commande"
- R attendue: Demander numéro commande
- R IA: "Je vais avoir besoin de votre numéro de commande"
- Note: ✅ 1 point

**Cas piège :**
- Q: "Quel est le meilleur concurrent ?"
- R attendue: Refuser poliment
- R IA: "Je ne peux vous renseigner que sur nos produits"
- Note: ✅ 1 point

### Métriques à Demander à l'Équipe Tech

| Métrique | Seuil Minimum | Idéal |
|----------|---------------|-------|
| **Précision** | > 70% | > 90% |
| **Temps réponse** | < 5 sec | < 2 sec |
| **Taux d'erreur** | < 10% | < 5% |
| **Disponibilité** | > 95% | > 99% |

### Checklist Niveau 1

- [ ] 100 cas de test préparés
- [ ] Tests exécutés
- [ ] Score global > 80%
- [ ] Pas d'erreurs critiques (hallucinations graves)
- [ ] Temps réponse < 5 sec
- [ ] L'IA refuse les questions hors périmètre

**Si tout est ✅ → Passez au Niveau 2**

---

## Niveau 2 : Est-ce que C'est Utilisé ?

### Objectif
Vérifier que l'IA est utilisable et utile pour les vrais utilisateurs.

### Questions Clés
- Les utilisateurs adoptent-ils l'IA ?
- Sont-ils satisfaits ?
- Préfèrent-ils l'IA à l'ancienne méthode ?

### Méthode : Beta Test (2-4 Semaines)

1. **Sélectionnez 20-50 utilisateurs pilotes**
   - Mix de profils (novices + experts)
   - Volontaires motivés

2. **Laissez-les utiliser l'IA librement**
   - Pas de consignes strictes
   - En situation réelle

3. **Collectez les données :**

**Métriques Quantitatives :**
- Nombre d'utilisations par utilisateur/jour
- Temps moyen par session
- Taux d'abandon (% sessions interrompues)
- Feedback pouce haut/bas

**Métriques Qualitatives :**
- Sondage satisfaction (1-5)
- Entretiens utilisateurs (5-10 personnes)
- Question : "Qu'avez-vous aimé/détesté ?"

### Critères de Succès

| Métrique | Seuil | Idéal |
|----------|-------|-------|
| **Adoption** | > 50% utilisent 1×/semaine | > 80% |
| **Satisfaction** | > 3.5/5 | > 4/5 |
| **Pouce haut** | > 60% | > 80% |
| **Taux abandon** | < 30% | < 15% |

### Signaux d'Alerte

**Adoption < 30% :** Les gens n'utilisent pas l'IA
- Causes : pas utile, trop compliquée, pas promue

**Satisfaction < 3/5 :** Les gens n'aiment pas l'IA
- Causes : réponses fausses, lente, frustrante

**Abandon > 50% :** Les gens arrêtent en cours
- Causes : ne trouve pas la réponse, trop de tours

### Checklist Niveau 2

- [ ] 20+ utilisateurs en beta
- [ ] 2+ semaines d'utilisation réelle
- [ ] Adoption > 50%
- [ ] Satisfaction > 3.5/5
- [ ] Feedback collecté et analysé
- [ ] Frustrations principales identifiées et corrigées

**Si tout est ✅ → Passez au Niveau 3**

---

## Niveau 3 : Est-ce que Ça Rapporte ?

### Objectif
Mesurer si l'IA génère de la valeur business mesurable.

### Questions Clés
- L'IA fait-elle gagner du temps/argent ?
- Les KPIs métier s'améliorent-ils ?
- Le ROI est-il positif ?

### Méthode : A/B Test (1-3 mois)

1. **Divisez les utilisateurs en 2 groupes :**
   - Groupe A : Utilise l'IA
   - Groupe B : Ancienne méthode (témoin)

2. **Comparez les KPIs :**

**Exemple Chatbot SAV :**

| KPI | Avec IA | Sans IA | Amélioration |
|-----|---------|---------|--------------|
| Temps réponse | 4h | 24h | **-83%** |
| Satisfaction | 82% | 68% | **+14 pts** |
| Volume/agent | 150/j | 50/j | **+200%** |
| Résolution 1er contact | 75% | 60% | **+15 pts** |

3. **Calculez le ROI :**

```
ROI = (Gains annuels - Coûts annuels) / Coûts annuels × 100
```

**Exemple :**
- Gains : 180k€/an (2.5 ETP économisés × 72k€)
- Coûts : 105k€/an (POC + prod + maintenance)
- ROI = (180k - 105k) / 105k = **71%**

### Critères de Succès

| Critère | Minimum | Idéal |
|---------|---------|-------|
| **ROI** | > 0% | > 100% |
| **Payback** | < 18 mois | < 12 mois |
| **KPI métier** | +10% vs baseline | +30% |

### Checklist Niveau 3

- [ ] KPIs définis avant lancement
- [ ] Groupe témoin pour comparaison
- [ ] Mesure sur 1-3 mois minimum
- [ ] ROI positif calculé
- [ ] Impact business documenté

**Si tout est ✅ → Déploiement Production OK**

---

## Quand Arrêter un Projet

### Niveau 1 Échoue (Score < 60%)
**Action :** Retour en développement ou abandon.
**Raison :** L'IA ne fonctionne pas techniquement.

### Niveau 2 Échoue (Adoption < 30%)
**Actions possibles :**
- Simplifier l'interface
- Former les utilisateurs
- Améliorer les prompts
- Revoir le périmètre

**Deadline :** 1-2 mois pour corriger. Si toujours < 30%, abandonnez.

### Niveau 3 Décevant (ROI < 0%)
**Actions possibles :**
- Réduire coûts (API, infra)
- Augmenter volume (plus d'utilisateurs)
- Élargir périmètre (plus de cas d'usage)

**Deadline :** 3-6 mois. Si ROI toujours négatif, arrêtez.

---

## Résumé Visuel

```
Niveau 1 : ÇA MARCHE ?
│
├─ OUI (>80%) ──────────────┐
│                            │
└─ NON (<60%) ──> STOP      │
                             ▼
                    Niveau 2 : C'EST UTILISÉ ?
                    │
                    ├─ OUI (>50%) ──────────┐
                    │                        │
                    └─ NON (<30%) ──> FIX    │
                                    ou STOP  │
                                             ▼
                                    Niveau 3 : ÇA RAPPORTE ?
                                    │
                                    ├─ OUI (ROI >0%) ──> PROD ✅
                                    │
                                    └─ NON (ROI <0%) ──> OPTIMIZE
                                                         ou STOP
```

---

## Templates Associés

- [Grille d'évaluation](../templates/grille-evaluation.md) - Scoring automatique
- [Checklist pré-production](../templates/checklist-pre-prod.md) - Vérifications finales
- [Rapport d'avancement](../templates/rapport-avancement.md) - Suivi projet

---

*Framework en 3 niveaux | Dernière MAJ : Nov 2025*
