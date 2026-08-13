# The Term Ledger — setup

This folder is a ready-to-host Progressive Web App (PWA). Once it's live on a
`https://` URL, you can "install" it to your phone's home screen like a real app,
and it'll keep working offline.

## 1. Create the repo

1. Go to https://github.com/new
2. Name it anything, e.g. `term-ledger`
3. **Public** repo is fine — your attendance/marks data is never stored in the
   repo or visible on the page source. It lives only in your own browser's
   local storage on your device. The repo just holds the empty app shell.
   (A private repo works too, but on the free plan it can't run GitHub Pages —
   that needs GitHub Pro. Public + this app is effectively just as private for
   your actual data.)
4. Don't initialize with a README (you already have one here) — or just
   overwrite it, either is fine.

## 2. Upload the files

Easiest way (no git needed): on your new repo's page, click
**"Add file" → "Upload files"**, then drag in everything from this folder:

```
index.html
manifest.json
service-worker.js
icons/icon-192.png
icons/icon-512.png
```

Commit the upload.

(If you're comfortable with git instead: `git init`, `git add .`,
`git commit -m "init"`, `git remote add origin <your-repo-url>`, `git push`.)

## 3. Turn on GitHub Pages

1. In your repo, go to **Settings → Pages**
2. Under "Build and deployment" → **Source**, choose **Deploy from a branch**
3. Branch: **main**, folder: **/ (root)** → Save
4. Wait ~1 minute, then your app is live at:
   `https://<your-username>.github.io/<repo-name>/`

## 4. Install it on your phone

- **Android (Chrome):** open the URL → tap the ⋮ menu → **"Add to Home
  screen" / "Install app"**
- **iPhone (Safari):** open the URL → tap the Share icon → **"Add to Home
  Screen"**

It'll appear with the gold ledger icon and open full-screen, no browser bar.

## Notes

- Data is stored **per browser/device** (local storage) — your phone and
  laptop won't automatically sync. Use the **Export/Import backup** button
  in the app's settings (⚙) to move data between devices manually.
- Whenever I hand you updated files later, just re-upload them the same way
  (Add file → Upload files) and they'll overwrite the old versions.
