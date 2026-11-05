# PROTOCOL Dashboard — GitHub Pages

Private repo. The live site is still public to anyone with the link on free GitHub Pages.

## Files
- `index.html` — Intelly layout shell (black sidebar, header, Refresh button). Rarely changes.
- `app.js` — fetches `data/data.json` with a cache-busting `?v=` timestamp and renders it.
- `data/data.json` — the dashboard content for the current week. **This is the only file that changes daily.**
- `.nojekyll` — tells GitHub Pages not to run Jekyll.

## How to update (manual, for now)
1. Get a new `data.json` from Beans (daily 9am job).
2. In GitHub, open the repo → `data/` → `data.json` → pencil icon → paste the new file → Commit changes.
3. Open the dashboard link and hit Refresh. GitHub Pages redeploys in about a minute.

No Monday.com or Google tokens are in this repo or in the browser. Data fetching happens in Beans' daily job, with secrets stored securely there.

## Turn on Pages (first time only)
Repo → Settings → Pages → Build and deployment → Source: **Deploy from a branch** → Branch: **main**, folder: **/(root)** → Save.
Your link will be: `https://<your-github-username>.github.io/protocol-dashboard/`
