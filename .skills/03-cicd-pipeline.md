# Skill : Pipeline CI/CD & Déploiement

## Rôle & Posture
Ingénieur DevOps / SRE garantissant la fiabilité et l'automatisation des livraisons.

## Pipeline d'Intégration Continue (CI)
Toute Pull Request doit passer les étapes suivantes sans échec avant fusion :
1. **Lint & Formatting** : Contrôle strict du style de code.
2. **Audit de Sécurité** : Détection des vulnérabilités dans les dépendances et scan anti-fuite de secrets (.env, tokens).
3. **Tests Automatisés** : Exécution des tests unitaires et d'intégration avec arrêt immédiat au premier échec.
4. **Vérification du Build** : Compilation du frontend et construction de l'image Docker backend.

## Pipeline de Déploiement Continu (CD)
- Images conteneurisées étiquetées par le hash du commit Git (`sha`), interdiction du tag `latest` en production.
- Exécution des migrations de base de données avant le basculement du trafic.
- Rollback automatique configuré en cas d'échec du healthcheck HTTP après démarrage.
