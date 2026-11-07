# Skill : Design System Professionnel & Anti-Pattern IA

## Objectif
Concevoir une interface technique sobre, lisible et orientée ingénierie/sécurité. Bannir tous les tics visuels générés par défaut par les IA.

## 1. Liste Noire Visuelle (Strict Don'ts)
- INTERDIT : Dégradés flashy (violet/rose/bleu néon) sur les arrière-plans, boutons ou cartes.
- INTERDIT : Glassmorphism lourd (flous excessifs `backdrop-blur` avec bordures blanches semi-transparentes).
- INTERDIT : Ombres baveuses et diffuses (`shadow-2xl`).
- INTERDIT : Rayons de bordure trop ronds pour des conteneurs de données (utiliser `rounded-md` ou `rounded-lg`, pas de pilules géantes).

## 2. Principes Visuels "Engineering & Security"
- **Palette Neutre & Solide** : Dominante de gris ardoise/zinc profonds ou clairs. Une seule couleur d'accent sobre (bleu cobalt, ambre ou vert sombre).
- **Structure par Bordures Fines** : Remplacer les ombres par des bordures de 1px nettes (`border border-zinc-200 dark:border-zinc-800`).
- **Couleurs Sémantiques Strictes** :
  - Vert : Validé / Sécurisé / Chiffré.
  - Ambre : Avertissement / En attente / Action requise.
  - Rouge : Erreur / Danger / Action irréversible.
- **Typographie Technique** : Sans-serif neutre (Inter, Geist) pour le texte général ; police Monospace pour les identifiants, hashs, clés API et timestamps.
- **Grille de 8px** : Tous les paddings, margins et gaps doivent être des multiples de 8px (8, 16, 24, 32, 48px).
