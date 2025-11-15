# Cas Pratique : Chatbot Service Client

> Retour d'expérience complet d'un projet de chatbot IA pour le support client.

---

## Contexte

**Entreprise :** Société e-commerce (500 employés, 200k clients actifs)
**Département :** Service Client
**Durée projet :** 10 mois (Janvier - Octobre 2024)
**Budget total :** 185k€

---

## Le Problème Initial

### Situation Avant Projet

**Équipe SAV :**
- 12 agents service client
- Volume : 800 tickets/jour
- Temps de réponse moyen : 36 heures
- Satisfaction client : 62%
- Taux de résolution 1er contact : 55%

**Douleurs identifiées :**
1. **Délais excessifs** : Les clients attendent trop longtemps
2. **Questions répétitives** : 70% des questions sont des FAQ
3. **Agents surchargés** : Focus sur le volume, pas la qualité
4. **Coûts élevés** : 720k€/an (12 agents × 60k€)
5. **Pics difficiles** : Black Friday, soldes = chaos

**Impact business :**
- NPS : 25 (faible)
- Taux de churn : 18%/an
- Coût estimé du churn lié au SAV : 180k€/an

---

## La Solution Proposée

### Objectif

Déployer un chatbot IA pour traiter automatiquement 60-70% des demandes simples (FAQ) et libérer les agents pour les cas complexes.

### Type d'IA Choisi

**Architecture :** LLM (Large Language Model) + RAG (Retrieval Augmented Generation)

**Pourquoi ce choix :**
- Compréhension du langage naturel (pas de script rigide)
- Réponses personnalisées basées sur la base de connaissances
- Pas besoin de 100 000 exemples d'entraînement
- Mise en place relativement rapide

**Stack technique :**
- LLM : GPT-4 (via API OpenAI)
- RAG : Base de connaissances FAQ + politiques
- Intégration : Widget sur site web + API vers CRM
- Fallback : Escalade vers agent humain

---

## Déroulement du Projet

### Phase 1 : Cadrage (4 semaines) - 15k€

**Activités :**
- Analyse de 5000 tickets historiques
- Catégorisation des demandes
- Identification des FAQ (70% du volume)
- Rédaction du business case
- Constitution de l'équipe

**Résultats :**
- Top 50 questions = 65% du volume
- Temps moyen traitement FAQ = 12 min/ticket
- Business case validé : ROI projeté 180% sur 3 ans
- GO pour POC

**Équipe mobilisée :**
- 1 Chef de projet (50%)
- 1 Responsable SAV (30%)
- 1 Data Analyst (20%)

---

### Phase 2 : POC (8 semaines) - 45k€

**Objectif POC :** Prouver que le chatbot peut répondre correctement aux 50 FAQ principales.

**Activités :**
- Setup environnement cloud (Azure)
- Développement pipeline RAG
- Création base de connaissances (150 articles)
- Intégration API OpenAI
- Tests sur 100 questions types

**Équipe :**
- 1 ML Engineer (100%) - externe
- 1 Data Engineer (50%) - interne
- 1 Chef de projet (30%)

**Résultats POC :**

| Métrique | Objectif | Obtenu | Verdict |
|----------|----------|--------|---------|
| Précision FAQ | > 75% | 82% | ✅ |
| Temps réponse | < 5s | 3.2s | ✅ |
| Hallucinations | < 5% | 3% | ✅ |
| Escalade appropriée | > 90% | 88% | ⚠️ |

**Apprentissages :**
- Les questions sur les retours produits mal gérées → enrichir la base
- Prompt engineering crucial pour la qualité
- Coût API plus élevé que prévu (GPT-4 cher)

**Décision :** GO Pilote avec améliorations

---

### Phase 3 : Pilote (12 semaines) - 85k€

**Objectif Pilote :** Valider l'adoption utilisateur et l'impact business en conditions réelles.

**Déploiement progressif :**
- Semaine 1-2 : 10% du trafic (widget avec opt-in)
- Semaine 3-4 : 25% du trafic
- Semaine 5-8 : 50% du trafic
- Semaine 9-12 : 100% du trafic (avec fallback)

**Améliorations apportées :**
- Base de connaissances enrichie (350 articles)
- Prompts optimisés
- Détection de sentiment ajoutée
- Dashboard de monitoring complet

**Métriques suivies :**

| Semaine | Conversations | Auto-résolues | Satisfaction | Escalade |
|---------|--------------|---------------|--------------|----------|
| 1-2 | 120/j | 58% | 3.8/5 | 32% |
| 3-4 | 280/j | 62% | 4.0/5 | 28% |
| 5-8 | 520/j | 68% | 4.1/5 | 24% |
| 9-12 | 750/j | 71% | 4.2/5 | 21% |

**Feedback utilisateurs :**

**Positif :**
- "Réponse instantanée, c'est génial !"
- "Ça répond bien à mes questions simples"
- "24/7 disponible, pratique"

**Négatif :**
- "Parfois trop générique"
- "Je préfère parler à un humain pour les réclamations"
- "Ne comprend pas toujours ma question"

**Incidents notables :**
- Semaine 3 : Hallucination sur politique de remboursement → correction immédiate
- Semaine 6 : Pic de trafic (soldes) → latence dégradée → scaling

**Décision :** GO Production avec ajustements

---

### Phase 4 : Production (ongoing) - 40k€ setup + 35k€/an maintenance

**Déploiement :**
- Date : Octobre 2024
- 100% du trafic
- Supervision humaine sur conversations sensibles
- Monitoring continu

**Configuration finale :**
- Chatbot traite automatiquement les FAQ
- Escalade automatique si : sentiment négatif, question complexe, demande explicite
- Agent reçoit l'historique conversation
- Feedback loop pour amélioration continue

---

## Résultats Business

### Comparaison Avant/Après (6 mois post-lancement)

| KPI | Avant | Après | Amélioration |
|-----|-------|-------|--------------|
| Volume tickets traités | 800/j | 1100/j | **+38%** |
| Temps réponse moyen | 36h | 4h | **-89%** |
| Satisfaction client | 62% | 78% | **+16 pts** |
| Résolution 1er contact | 55% | 72% | **+17 pts** |
| Tickets escaladés aux agents | 800/j | 320/j | **-60%** |
| Coût par ticket | 8.50€ | 3.20€ | **-62%** |

### Impact Équipe

**Agents SAV :**
- Avant : 12 agents
- Après : 8 agents (4 redéployés vers upsell/rétention)
- Focus : Cas complexes et à forte valeur
- Satisfaction employé : Augmentée (moins de répétitif)

**Pas de licenciement** : Redéploiement vers activités à plus forte valeur (rétention clients, vente additionnelle).

### ROI Réel

**Coûts totaux projet :**
- Développement : 145k€
- Production Y1 : 40k€
- **Total Y1 : 185k€**

**Maintenance annuelle (Y2+) :** 35k€/an

**Gains annuels :**
- Réduction coût SAV : 240k€/an (4 agents redéployés × 60k)
- Revenus rétention : 80k€/an (↓ churn grâce à meilleur service)
- Revenus upsell (agents redéployés) : 120k€/an
- **Total gains : 440k€/an**

**Calcul ROI :**
```
Y1 : Gains 440k€ - Coûts 185k€ = +255k€
Y2 : Gains 440k€ - Coûts 35k€ = +405k€
Y3 : Gains 440k€ - Coûts 35k€ = +405k€

ROI 3 ans = (1065k€ - 255k€) / 255k€ = 318%
Payback = 185k€ / 440k€ = 5 mois
```

---

## Leçons Apprises

### Ce qui a bien fonctionné ✅

1. **Approche progressive** : POC → Pilote → Prod a permis d'ajuster
2. **Implication du métier** : Le responsable SAV était dans l'équipe projet
3. **Base de connaissances solide** : Investissement initial sur le contenu payant
4. **Escalade intelligente** : Ne pas forcer l'IA sur tout, savoir passer la main
5. **Monitoring dès le début** : Détection rapide des problèmes

### Ce qui aurait pu être mieux 🔧

1. **Budget API sous-estimé** : GPT-4 coûte cher à l'échelle
   - Solution : Switchant vers GPT-3.5 pour FAQ simples, GPT-4 pour complexe

2. **Temps de mise en place RAG** : Plus long que prévu
   - Solution : Commencer plus tôt la base de connaissances

3. **Formation utilisateurs finaux** : Clients pas toujours à l'aise
   - Solution : UX améliorée avec messages d'aide

4. **Multilinguisme** : Non prévu au départ, demandé ensuite
   - Solution : À intégrer dans roadmap V2

### Conseils pour Reproduction

1. **Commencez par les FAQ vraiment** : Ne cherchez pas à tout automatiser
2. **Investissez dans la base de connaissances** : C'est le cœur du RAG
3. **Prévoyez le fallback humain** : L'IA n'est pas parfaite
4. **Monitorez les coûts API** : Ça peut exploser
5. **Impliquez les agents SAV** : Ils connaissent les vraies questions
6. **Testez les cas sensibles** : Réclamations, sujets légaux

---

## Évolutions Prévues (V2)

**Court terme (6 mois) :**
- Support multilingue (EN, ES)
- Intégration WhatsApp et Messenger
- Personnalisation basée sur l'historique client

**Moyen terme (12 mois) :**
- Proactivité : Contacter les clients à risque de churn
- Analyse prédictive des besoins
- Self-service sur plus de cas (suivi commande, modification)

**Budget V2 :** 80k€ estimé

---

## Conclusion

Ce projet illustre qu'un chatbot IA bien exécuté peut :
- **Améliorer drastiquement l'expérience client** (temps réponse ÷10)
- **Réduire les coûts** (62% de réduction coût/ticket)
- **Libérer les humains pour des tâches à forte valeur**
- **Générer un ROI significatif** (300%+ sur 3 ans)

**Facteurs clés de succès :**
- Problème business clair et mesurable
- Approche itérative avec validations
- Équilibre IA + humain (pas de 100% automatisation)
- Investissement dans les données et le contenu
- Monitoring et amélioration continue

---

## Ressources

- [Lancer un projet IA](../pilotage/lancer-projet-ia.md)
- [Framework évaluation](../evaluation/framework-3-niveaux.md)
- [Budget et ROI](../pilotage/budget-et-roi.md)

---

*Cas pratique chatbot SAV | Nov 2025*
