# Pack d'Architecture & Standards d'Équipe

Pack d'architecture et de gouvernance de développement partagé pour l'équipe (Nathan, Lydie, Eric).

## Structure du Répertoire

```text
├── .cursor/
│   └── rules/
│       └── team-rules.mdc           # Règle maître pour Cursor / Claude Code / Agents
├── .skills/
│   ├── 01-backend-api.md            # Architecture backend, routes, validation, base de données
│   ├── 02-frontend-clean.md         # Découpage UI, état, intégration API
│   ├── 03-cicd-pipeline.md          # Règles d'automatisation et de déploiement
│   ├── 04-system-architecture.md    # Alignement global, API-First et sécurité
│   ├── 05-anti-ai-design.md         # Charte esthétique sobre (Anti-slop)
│   └── 06-v0-prompt-contract.md     # Template de prompt pour générateurs UI (v0 / Bolt)
└── .github/
    └── workflows/
        └── ci-cd.yml                # Pipeline GitHub Actions automatisé
```

## Utilisation

1. **Cursor & Assistants IA** : Le fichier `.cursor/rules/team-rules.mdc` applique automatiquement les standards définis dans `.skills/`.
2. **Génération d'UI** : Utiliser le template `.skills/06-v0-prompt-contract.md` pour générer des composants frontend directement intégrables.
3. **Intégration Continue (CI/CD)** : Le workflow GitHub Actions (`.github/workflows/ci-cd.yml`) valide la qualité, la sécurité et le build Docker sur chaque PR et push sur `main` / `develop`.
