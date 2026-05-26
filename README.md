# Cassino Pro — Legal Pages

Single-file Privacy Policy + Terms of Use for the Cassino Pro mobile app.
Hosted via GitHub Pages so the Google Play listing can link to a live
URL.

## Deploy to GitHub Pages

There are two ways to host this. Pick whichever fits your repo layout.

### Option A — serve from this repo's `/docs` folder

1. Push the project (with this `docs/` directory) to a public GitHub
   repository.
2. In GitHub: **Settings → Pages**.
3. Under **Build and deployment → Source**, pick **Deploy from a
   branch**.
4. **Branch:** `main` (or whatever the default branch is). **Folder:**
   `/docs`. Save.
5. After ~1 minute, GitHub will show the URL. It looks like
   `https://<your-username>.github.io/<repo-name>/`.

### Option B — separate public repo (recommended if the app repo is private)

If the app repo is private and you don't want to make it public just to
host one HTML file:

1. Create a new public repo, e.g. `cassino-pro-legal`.
2. Copy `index.html` into the root of that repo (NOT into `/docs`).
3. Push.
4. In the new repo: **Settings → Pages → Source: Deploy from a branch
   → Branch: `main`, Folder: `/ (root)`**.
5. URL: `https://<your-username>.github.io/cassino-pro-legal/`.

## Use the URL in the Play Console

- **Data safety form → Privacy Policy URL:** paste the hosted URL.
- **Store listing → Privacy Policy:** same URL.
- Optionally, append `#privacy` for direct deep-link to the privacy
  section, or `#terms` for the terms section.

## Update later

The `Effective date` at the top of `index.html` should be updated
whenever you change the content. Material changes (new third-party
services, new data collected) should be called out in-app on next
launch so existing users notice.

## Why a single HTML file

- No build step, no dependencies, no JS. Pure HTML + inline CSS.
- Renders fine on phones (responsive breakpoints baked in).
- Respects the user's system dark-mode preference.
- Fast to load on slow connections — important since Play Console will
  validate the URL responds.
