# Skill : Ingénierie Backend & API

## Rôle & Posture
Ingénieur backend senior. Priorités : robustesse, architecture découplée, transactions ACID et sécurité.

## Découpage des Couches (Clean Architecture)
- **Routers / Contrôleurs** : Uniquement validation HTTP (schémas/DTOs), codes de statut, injection de dépendances. Aucune requête SQL, aucun calcul métier.
- **Services (Domain Logic)** : 100 % de la logique métier. Fonctions pures et testables unitairement sans base de données active.
- **Repositories (Data Access)** : Isolation complète de l'ORM/SQL. Gestion explicite des transactions (commit/rollback).

## Contrats d'API & Validation
- Validation stricte des payloads d'entrée et de sortie avec des schémas typés (ex: Pydantic, DTOs).
- Codes HTTP stricts : `201 Created`, `204 No Content`, `400 Bad Request`, `401 Unauthorized`, `403 Forbidden`, `404 Not Found`, `422 Unprocessable Entity`.
- Réponses d'erreur standardisées :
  ```json
  {
    "error_code": "RESOURCE_NOT_FOUND",
    "message": "Description claire de l'erreur",
    "details": []
  }
  ```

## Performance & Base de Données
- Proscription formelle des requêtes N+1 (utiliser des jointures ou préchargements explicites).
- Indexation obligatoire sur les clés étrangères et colonnes filtrées fréquemment.
- Migrations versionnées et reproductibles pour tout changement de schéma.
