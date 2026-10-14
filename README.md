# Soundbox Dynamic QR Integration — Static Site

Universal software solution for Soundbox & Dynamic QR devices. Drop-in REST API
integration for any ERP/ECR billing system. Zero ERP modifications. Free Windows
software. Universal device support.

## ⚠️ Fixing a 404 on Vercel

If Vercel shows `404 NOT_FOUND`, it almost always means `index.html` is **not at the
repository root**. Vercel serves static files from the repo root by default.

**Checklist:**
1. In your GitHub repo, `index.html` must be at the top level (not inside a `site/`
   or any subfolder). If you extracted a zip, move the files up so `index.html` sits
   directly in the repo root.
2. In the Vercel project settings → **General** → **Root Directory**: leave it
   blank (or set to `.`). Do NOT point it at a subfolder unless your files live there.
3. **Build Command**: leave empty. **Output Directory**: leave empty (or `.`).
4. Framework Preset: **Other**.
5. No `vercel.json` is required for a pure static site — Vercel auto-detects
   `index.html`. (A bad/extra `vercel.json` can itself cause 404s.)
6. After fixing, go to **Deployments** → **Redeploy** (or push a new commit).

## Deploy to Vercel (via GitHub)

### 1. Create a GitHub repository
1. Go to https://github.com/new
2. Name it (e.g. `soundbox-dynamic-qr-site`), set Public/Private, **do not** initialize with README.
3. Copy the repo URL.

### 2. Push this project (files must be at repo root)
```bash
git init
git add .
git commit -m "Initial commit: Soundbox Dynamic QR marketing site"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/<YOUR_REPO>.git
git push -u origin main
```

### 3. Import into Vercel
1. Open https://vercel.com/new (or your dashboard: https://vercel.com/shivjanams-projects)
2. Click **Import Git Repository** → select your repo.
3. Framework Preset: **Other**. Build Command: empty. Output Directory: empty/`.`.
4. Root Directory: empty/`.`.
5. Click **Deploy**.

Every subsequent `git push` to `main` triggers a new deployment.

### Alternative: Vercel CLI (no GitHub)
```bash
npm i -g vercel
vercel login
vercel --prod
```
Run from the folder containing `index.html`.

### Local preview
```bash
npx serve .
# or
python3 -m http.server 8080
```
