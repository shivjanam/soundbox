# Soundbox Dynamic QR Integration — Static Site

Universal software solution for Soundbox & Dynamic QR devices. Drop-in REST API
integration for any ERP/ECR billing system. Zero ERP modifications. Free Windows
software. Universal device support.

## Deploy to Vercel (via GitHub)

### 1. Create a GitHub repository
1. Go to https://github.com/new
2. Name it (e.g. `soundbox-dynamic-qr-site`), set to Public or Private, **do not** initialize with README.
3. Copy the repo URL.

### 2. Push this project
Run these commands in the project folder (where `index.html` lives):

```bash
git init
git add .
git commit -m "Initial commit: Soundbox Dynamic QR marketing site"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/<YOUR_REPO>.git
git push -u origin main
```

> If you use SSH, replace the remote URL with `git@github.com:<YOUR_USERNAME>/<YOUR_REPO>.git`.

### 3. Import into Vercel
1. Open https://vercel.com/new (or your dashboard: https://vercel.com/shivjanams-projects)
2. Click **Import Git Repository** → select your repo.
3. Framework Preset: **Other** (static). Build Command: leave empty. Output Directory: `.` (root).
4. Click **Deploy**.

Vercel will auto-detect `index.html` at the root and serve it as a static site. Every subsequent `git push` to `main` triggers a new deployment.

### Alternative: Deploy with Vercel CLI (no GitHub)
```bash
npm i -g vercel
vercel login
vercel --prod
```

### Local preview
```bash
npx serve .
# or
python3 -m http.server 8080
```
