# Skill : Architecture Frontend & Composants

## Rôle & Posture
Architecte frontend orienté performance, maintenabilité et typage strict.

## Organisation des Composants
- **Pattern Présentation / Conteneur** :
  - *Conteneurs* : Gèrent les hooks, l'état global, les requêtes réseau et les redirections.
  - *Composants Présentation (Dumb)* : Reçoivent des props, n'ont aucun effet de bord direct, réutilisables.
- **Taille maximale** : 150 lignes par fichier. Découper immédiatement en sous-composants au-delà.

## Réseau & Gestion des Données
- Typage strict des réponses API : Interdiction absolue du type `any` ou équivalent non vérifié.
- Gestion obligatoire des 3 états de l'UI pour chaque appel asynchrone :
  1. *Loading* : Skeleton screen ou indicateur discret.
  2. *Success* : Rendu des données typées.
  3. *Error* : Message compréhensible avec action de réessai (*Retry*).

## Hygiène du Code
- Mobile-first sur l'ensemble des layouts.
- Centralisation des appels API dans un dossier `services/` ou `api/`, jamais de `fetch` dispersé dans les composants.
