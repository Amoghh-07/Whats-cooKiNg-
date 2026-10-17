# What's CooKiNg?

A responsive, client-side recipe discovery website. It runs as a static site and does not need a backend, database, account, API key, or AI service.

## Run locally

Open `index.html` in a modern browser, or serve this folder with any static server (for example, VS Code Live Server). No npm install or build step is required.

## Features

- Search and browse 120+ ingredients across categories.
- Select ingredients, type comma-separated ingredients, or upload/preview an ingredient photo.
- Recipe matching, match scoring, time/cuisine/diet filters, and result sorting.
- Expanded local recipe collection (nearly 500 dishes) with cooking steps, ingredient checklists, serving count, and a cooking timer.
- Favorites, recent cooking history, pantry list, use-soon flags, and saved shopping list data in browser localStorage.
- Responsive mobile/desktop layout.

## Important photo limitation

This version deliberately contains **no AI and no image-recognition model**. The photo tab validates that an image file was selected and previews it; it cannot tell whether an image contains ingredients or a pen. The interface explicitly asks the user to confirm visible ingredients through the ingredient picker instead of falsely claiming automatic recognition. True semantic photo recognition (including rejecting non-food objects) requires an image-classification model or an external vision service, which is outside this no-AI build.

## Data and customization

Ingredient data and recipe records live in `app.js` as local JavaScript arrays. Rice and basmati rice are treated as equivalent for recipe matching, so entering “rice” returns recipes that call for either type. Add new ingredient records to `INGREDIENTS` and new recipe records to `RECIPES`. The collection is broad but finite, not literally infinite. Photos use Unsplash image URLs; replace them with locally hosted image files if you want the site to work entirely offline.

## Publish

Upload this folder to GitHub and deploy it as a static site using GitHub Pages, Cloudflare Pages, or Netlify. Since there is no build step, set the publish/root directory to this folder and no build command is needed.
