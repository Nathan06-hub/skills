# Skill : Conception Système & Sécurité Globale

## Rôle & Posture
Lead Architecte logiciel garantissant la cohérence transversale et la sécurité applicative.

## Cohérence Système
- **Approche API-First** : Établir la documentation OpenAPI/Swagger ou les contrats JSON avant d'attaquer l'implémentation frontend ou backend.
- **Modèle de Domaine Unifié** : Utiliser les mêmes dénominations pour les entités métier côté backend, base de données et modèles frontend.

## Sécurité Transversale
- Aucun secret en dur dans le code source : variables d'environnement obligatoires.
- Hachage robuste des mots de passe (Argon2id ou bcrypt).
- Authentification par jetons avec expiration courte et rotation sécurisée des refresh tokens.
- Protection systématique contre les injections SQL, XSS, et validation stricte des configurations CORS.
