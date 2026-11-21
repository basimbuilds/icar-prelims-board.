# ICAR Prelims Study Board — deployable PWA

This package turns the study board into an installable Progressive Web App (PWA).

## Easiest free deployment: GitHub Pages

1. Sign in or create an account at https://github.com.
2. Create a new **public** repository, for example `icar-prelims-board`.
3. Upload all four files from this folder to the repository's top level:
   - `index.html`
   - `manifest.webmanifest`
   - `sw.js`
   - `icon.svg`
4. In the repository, open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select branch **main** and folder **/(root)**, then click **Save**.
7. Wait for GitHub Pages to publish. Your site address will look like:
   `https://YOUR-USERNAME.github.io/icar-prelims-board/`
8. Share that address with your friends.

## Add to Android home screen

1. Open the published HTTPS link in Chrome.
2. Allow the page to finish loading once while online.
3. Open Chrome's ⋮ menu.
4. Choose **Install app** or **Add to Home screen** (wording varies).
5. Confirm. The board will appear on the home screen.

On iPhone/iPad, open the link in Safari → Share → Add to Home Screen.

## Offline use

Open the site once while connected to the internet. The service worker caches the app shell so it can load offline afterward. For best results, leave the page open until it has fully loaded once.

## Important data note

Each browser/device stores its own board data locally. Your friends will each have separate notes and progress; this version does not provide shared live boards or cloud synchronization.

Use **Backup** inside the app to export a JSON copy of your board. Use **Restore** to load that backup later. Clearing browser/site data can erase locally stored progress.

## Updating the app

When you change the app, upload the new files to the same repository and replace the old versions. The service worker cache version can be incremented in `sw.js` (`icar-prelims-board-v1` → `v2`) to prompt installed copies to refresh their cached app shell.
