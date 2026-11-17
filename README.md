# AETHER REBIRTH v0.3 — Chrome iPhone

Prototype PWA dérivé de la version mobile v0.2 et utilisant des ressources du dépôt OpenJarvis (licence Apache-2.0). **Ce n’est pas le moteur OpenJarvis Python/Rust.**

## Fonctionnalités
- Thèmes AETHER, RAGNAR, FENRIR et MIMIR
- Notes, missions et historique en stockage local du navigateur
- Export ET import JSON des données
- Cache hors ligne après premier chargement HTTPS
- Endpoint IA HTTPS optionnel, contrat POST `{ "message": "...", "agent": "aether" }` -> `{ "reply": "..." }`

## Publication gratuite sur GitHub Pages (sans PC)
1. Créer un **nouveau dépôt public** sur GitHub (ne pas publier dans un dépôt contenant des secrets).
2. Importer **les fichiers de ce dossier à la racine du dépôt**, y compris `.github/workflows/pages.yml`. Le ZIP lui-même ne doit pas être le seul fichier envoyé.
3. Dans Settings > Pages > Build and deployment, sélectionner **GitHub Actions**.
4. Vérifier l'onglet Actions et attendre la réussite de « Publish AETHER REBIRTH ».
5. Ouvrir l'URL fournie par GitHub Pages dans Chrome iOS.
6. Pour l'installation écran d'accueil, utiliser Safari > Partager > Ajouter à l'écran d'accueil si Chrome ne propose pas l'option.

## Sécurité et limites
- Ne jamais placer de clé API dans les fichiers web ou le champ endpoint.
- Les notes et conversations sont stockées en clair sur cet appareil, dans ce navigateur : pas de secrets.
- Le stockage Chrome et celui de Safari/PWA peuvent être distincts : exporter les données avant de changer de navigateur.
- La reconnaissance vocale dépend du navigateur ; le micro peut ne pas fonctionner sous Chrome iOS. La dictée du clavier est une alternative.
- Le backend IA distant doit être sécurisé, authentifié et autoriser explicitement le domaine web (CORS).
- Les actions système iOS ne sont pas directement disponibles depuis cette PWA.
