# Dairy S-Factor Tool — installable app

Static site, no build step. Deploy this folder as-is.

## Netlify (GitHub auto-deploy)
1. New GitHub repo (e.g. `s-factor-tool`) → upload everything in this folder to the repo root (including `.nojekyll` and `netlify.toml`).
2. Netlify → Add new site → Import from Git → pick the repo. Build command: blank. Publish directory: `.`
3. Every push to the repo redeploys. Open users get an "Update ready — reload" button.

## Netlify (drag and drop)
Netlify → Sites → drag this folder onto the deploy area.

## GitHub Pages (alternative)
Repo → Settings → Pages → Deploy from branch → `main` / root. All paths are relative, so `/repo-name/` works.

## Install
- Windows PC (Chrome/Edge): open the site → "Install app" button in the header (or the install icon in the address bar). After install, `.sfactor.json` files can be opened with the app (right-click → Open with → Dairy S-Factor Tool) and autosave straight back to them.
- Samsung tablet (Chrome): "Install app" button, or menu ⋮ → Add to home screen / Install app.
- iPhone (Safari): Share → Add to Home Screen.

Works offline after first open (map imagery and address search need internet).

## Updating the tool
Replace `index.html` (and bump nothing else — `sw.js` version changes automatically when rebuilt from `build.py`). If you edit `index.html` by hand, also change the `VERSION` string at the top of `sw.js` so installed copies pick it up.
