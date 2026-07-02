# Nishant & Banani — Wedding Invitation

A premium digital wedding invitation for **Nishant & Banani**  
10–11 December 2026 · Guwahati, Assam

---

## Live Site

> `https://<your-username>.github.io/<repo-name>`  
> *(update after first deploy)*

---

## Project Structure

```
├── index.html                   # Full invitation — CSS & JS inline, zero dependencies
├── .nojekyll                    # Disables Jekyll so WebP/AVIF assets serve correctly
├── .gitignore
├── README.md
├── .github/
│   └── workflows/
│       └── deploy.yml           # Auto-deploys on every push to main
└── assets/
    └── img/
        ├── hero-bg.webp/.avif
        ├── couple.webp/.avif
        ├── seal-bg.webp
        ├── logo.webp
        ├── ganesha.webp
        ├── eng-01…14.webp       # Engagement gallery
        └── meh-01…14.webp       # Mehendi gallery
```

**Total repo size:** ~3.5 MB

---

## Push to GitHub

```bash
cd github-pages

git init
git add .
git commit -m "Initial commit: Nishant & Banani wedding invitation"

git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git
git branch -M main
git push -u origin main
```

Then on GitHub:  
**Settings → Pages → Source → GitHub Actions** → save.

The workflow triggers automatically. Your site is live in ~60 seconds.

---

## Manual redeploy (no code change needed)

**Actions tab → "Deploy to GitHub Pages" → Run workflow**

---

## Local preview

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

> Open via `http://localhost` not `file://` — RSVP fetch() requires an HTTP origin.

---

## RSVP

Responses are written to a Google Sheet via Google Apps Script.  
The endpoint URL is inside `index.html` — search for `SCRIPT_URL` to update it.

---

## Tech

| | |
|---|---|
| HTML | Semantic HTML5, all CSS & JS inline |
| Images | WebP + AVIF via `<picture>` — ~70% smaller than source JPEGs |
| Fonts | Google Fonts — Playfair Display, Inter (`display=swap`) |
| Audio | Web Audio API — Bansuri flute, Yaman raga |
| Hosting | GitHub Pages — free, CDN-backed, HTTPS |
