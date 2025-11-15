# 30 Questions à Poser à Votre Équipe Technique

> Questions business-friendly pour évaluer la qualité d'un projet IA sans être data scientist.

## Comment Utiliser Ce Guide

Posez ces questions lors de vos réunions avec l'équipe data/IA. Pour chaque question :
- **Bonne réponse** → Confiance
- **Réponse floue** → Creusez
- **Red flag** → Alertez-vous

---

## Performance et Qualité

### 1. "Quelle est la précision du modèle ?"
**Bonne réponse :** "85% sur notre jeu de test, avec 90% de recall sur les cas critiques."
**Red flag :** "C'est très bon" sans chiffres.
**Pourquoi c'est important :** Vous devez connaître les limites.

### 2. "Comment avez-vous mesuré cette précision ?"
**Bonne réponse :** "Sur un jeu de test séparé, représentatif de la production."
**Red flag :** "Sur les données d'entraînement."
**Pourquoi :** Si testé sur les mêmes données qu'à l'entraînement, c'est biaisé.

### 3. "Quel est le taux d'erreur acceptable ?"
**Bonne réponse :** "5% d'erreur max, et voici les types d'erreurs possibles..."
**Red flag :** "Il n'y aura pas d'erreur."
**Pourquoi :** Toute IA fait des erreurs. Il faut anticiper.

### 4. "Quels sont les pires cas où l'IA échoue ?"
**Bonne réponse :** Exemples concrets de cas où ça ne marche pas.
**Red flag :** "Ça marche toujours."
**Pourquoi :** Connaître les limites permet de mettre des garde-fous.

### 5. "Combien de temps met l'IA pour répondre ?"
**Bonne réponse :** "En moyenne 1.5 secondes, 95e percentile à 3 secondes."
**Red flag :** "C'est rapide."
**Pourquoi :** La latence impacte directement l'expérience utilisateur.

---

## Données

### 6. "Sur combien de données le modèle est-il entraîné ?"
**Bonne réponse :** "50 000 exemples annotés, couvrant 18 mois d'historique."
**Red flag :** "Beaucoup de données."
**Pourquoi :** La quantité et la période comptent.

### 7. "D'où viennent ces données ?"
**Bonne réponse :** "De notre CRM, nettoyées et validées par l'équipe métier."
**Red flag :** "De plusieurs sources, on a tout mélangé."
**Pourquoi :** Données de mauvaise qualité = mauvaise IA.

### 8. "Qui a annoté/étiqueté les données ?"
**Bonne réponse :** "L'équipe métier avec des règles claires et contrôle qualité."
**Red flag :** "Des stagiaires" ou "automatiquement."
**Pourquoi :** L'annotation impacte directement la qualité.

### 9. "Les données sont-elles représentatives de la production ?"
**Bonne réponse :** "Oui, nous avons vérifié la distribution et les cas limites."
**Red flag :** "Normalement oui."
**Pourquoi :** Si les données d'entraînement diffèrent de la réalité, ça ne marchera pas.

### 10. "Y a-t-il des biais connus dans les données ?"
**Bonne réponse :** "Oui, sous-représentation de X, nous avons compensé ainsi..."
**Red flag :** "Non, aucun biais."
**Pourquoi :** Il y a toujours des biais. Les ignorer est dangereux.

---

## Robustesse et Maintenance

### 11. "Que se passe-t-il si les données changent ?"
**Bonne réponse :** "Nous avons un monitoring et un process de ré-entraînement."
**Red flag :** "On verra."
**Pourquoi :** Les données évoluent, l'IA doit suivre.

### 12. "À quelle fréquence faut-il ré-entraîner le modèle ?"
**Bonne réponse :** "Tous les 3 mois, basé sur notre analyse de drift."
**Red flag :** "Jamais, une fois c'est bon."
**Pourquoi :** Sans maintenance, la performance se dégrade.

### 13. "Comment savez-vous si le modèle se dégrade ?"
**Bonne réponse :** "Dashboards de monitoring avec alertes automatiques."
**Red flag :** "On ne sait pas."
**Pourquoi :** Vous devez détecter les problèmes avant les utilisateurs.

### 14. "Que se passe-t-il si l'IA est indisponible ?"
**Bonne réponse :** "Fallback automatique vers le process manuel avec alerte."
**Red flag :** "Ça n'arrivera pas."
**Pourquoi :** Il faut toujours un plan B.

### 15. "Comment gérez-vous les cas où l'IA ne sait pas ?"
**Bonne réponse :** "Score de confiance + escalade automatique si < 70%."
**Red flag :** "L'IA répond toujours."
**Pourquoi :** L'IA doit savoir dire "je ne sais pas."

---

## Coûts et Scalabilité

### 16. "Quel est le coût par requête/prédiction ?"
**Bonne réponse :** "0.02€ par requête, incluant API et infra."
**Red flag :** "Négligeable."
**Pourquoi :** Ça peut exploser avec le volume.

### 17. "Comment évolue le coût si on multiplie le volume par 10 ?"
**Bonne réponse :** "Coût × 8 grâce aux économies d'échelle sur l'infra."
**Red flag :** "Linéaire" ou "On ne sait pas."
**Pourquoi :** Planifier la scalabilité.

### 18. "Quel est le coût de maintenance annuel ?"
**Bonne réponse :** "Environ 25% du coût initial, pour X ETP + infra + APIs."
**Red flag :** "Pas de maintenance nécessaire."
**Pourquoi :** Budget la maintenance.

### 19. "L'infrastructure peut-elle tenir la charge ?"
**Bonne réponse :** "Testé jusqu'à 1000 req/sec, auto-scaling configuré."
**Red flag :** "Oui, normalement."
**Pourquoi :** Éviter les surprises en production.

### 20. "Avez-vous fait un test de charge ?"
**Bonne réponse :** "Oui, voici les résultats : X req/sec, latence Y."
**Red flag :** "Pas encore."
**Pourquoi :** Indispensable avant production.

---

## Sécurité et Conformité

### 21. "Les données sont-elles protégées ?"
**Bonne réponse :** "Chiffrement at-rest et in-transit, accès restreint."
**Red flag :** "Oui" sans détails.
**Pourquoi :** Conformité RGPD et sécurité.

### 22. "Où sont stockées les données utilisateurs ?"
**Bonne réponse :** "Serveurs EU, conformes RGPD, logs de X jours max."
**Red flag :** "Chez le fournisseur cloud US."
**Pourquoi :** Conformité légale.

### 23. "L'IA peut-elle être manipulée (prompt injection, etc.) ?"
**Bonne réponse :** "Oui, nous avons mis ces protections..."
**Red flag :** "Non, impossible."
**Pourquoi :** Toute IA générative est vulnérable.

### 24. "Les décisions de l'IA sont-elles explicables ?"
**Bonne réponse :** "Oui, voici comment nous expliquons les décisions..."
**Red flag :** "C'est une boîte noire."
**Pourquoi :** Nécessaire pour audits et conformité.

### 25. "Avez-vous testé les biais du modèle ?"
**Bonne réponse :** "Oui, testé sur genre, âge, localisation. Voici les résultats."
**Red flag :** "Non" ou "Il n'y en a pas."
**Pourquoi :** Risque juridique et éthique.

---

## Déploiement et Intégration

### 26. "Comment l'IA s'intègre-t-elle à nos systèmes existants ?"
**Bonne réponse :** "API REST, documentation complète, exemples d'intégration."
**Red flag :** "On verra ça plus tard."
**Pourquoi :** L'intégration est souvent le plus compliqué.

### 27. "Quels tests avez-vous fait avant production ?"
**Bonne réponse :** "Tests unitaires, intégration, charge, A/B test avec 10% du trafic."
**Red flag :** "Ça marche sur mon poste."
**Pourquoi :** Production ≠ développement.

### 28. "Comment faites-vous un rollback si ça ne marche pas ?"
**Bonne réponse :** "Procédure documentée, retour à l'ancienne version en 5 min."
**Red flag :** "On n'y a pas pensé."
**Pourquoi :** Plan de secours indispensable.

### 29. "Qui est d'astreinte si ça tombe en panne ?"
**Bonne réponse :** "Rotation d'équipe, procédure escalade claire."
**Red flag :** "On verra."
**Pourquoi :** Support critique en production.

### 30. "Quelle documentation existe ?"
**Bonne réponse :** "Documentation technique, guide utilisateur, runbook opérationnel."
**Red flag :** "C'est dans nos têtes."
**Pourquoi :** Sans doc, pas de maintenabilité.

---

## Synthèse par Thème

| Thème | Questions Clés | Red Flags Principaux |
|-------|---------------|---------------------|
| **Performance** | Précision chiffrée, cas d'échec | "Ça marche bien" sans chiffres |
| **Données** | Source, qualité, représentativité | "Pas de biais" |
| **Maintenance** | Monitoring, ré-entraînement | "Pas besoin de maintenance" |
| **Coûts** | Coût unitaire, scalabilité | "Négligeable" |
| **Sécurité** | Protection, conformité | "Pas de risque" |
| **Déploiement** | Tests, rollback, support | "On verra" |

---

## À Télécharger

- [Template d'évaluation](../templates/grille-evaluation.md) - Pour noter les réponses
- [Checklist pré-production](../templates/checklist-pre-prod.md) - Vérifications avant lancement

---

*30 questions essentielles | Dernière MAJ : Nov 2025*
