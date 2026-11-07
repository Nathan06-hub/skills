# Modèle de Prompt pour Générateur UI (v0 / Bolt)

Agis en tant que designer UI et ingénieur frontend senior. 
Génère un composant d'interface respectant strictement les contraintes suivantes :

1. Style & Esthétique :
- Utilise Tailwind CSS et les composants shadcn/ui.
- Style sobre, technique et orienté sécurité (style Stripe / Linear).
- Pas de dégradés flashy ni d'ombres excessives. Utilise des bordures de 1px nettes.
- Espacements basés sur une grille de 8px.

2. Structure du Code :
- Découpe le code en composants propres et typés avec TypeScript.
- Utilise une police Monospace pour les clés API, IDs et données d'audit.

3. Contrat de Données Mockées (Prêt à brancher sur l'API) :
Déclare les données en haut du composant sous forme d'un tableau d'objets JSON au format exact suivant :
[Insérer votre schéma d'API ici, ex: { "id": "uuid", "label": "string", "status": "active" | "revoked", "created_at": "ISOString" }]

Ne crée pas de logique métier interne complexe ; prévois simplement les callbacks `onAction(id)` pour que je puisse brancher mes requêtes API externes.
