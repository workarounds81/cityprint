# CityPrint

Website for CityPrint — a local printing business. Plain HTML/CSS/JS, no build step, deployed with GitHub Pages.

## Project layout

```
index.html                    Home page (hero, services, how it works, contact/quote form)
404.html                      Not-found page
assets/styles.css             Styles
assets/main.js                Mobile menu + footer year
assets/favicon.svg            Logo / favicon
.github/workflows/pages.yml   Auto-deploys to GitHub Pages on every push to main
```

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Before going live

- [ ] Replace placeholder email, phone, address and hours in `index.html` (search for `TODO`).
- [ ] Hook the quote form up to a form service (e.g. Formspree) — it currently opens the visitor's email app.
- [ ] Swap `assets/favicon.svg` for the real logo.

## One-time GitHub setup

1. **Default branch** → Settings → General → Default branch: make it `main`.
2. **Pages** → Settings → Pages → Build and deployment → Source: **GitHub Actions**.
3. **Branch protection** (optional) → Settings → Branches → add a rule for `main` (require PR before merging).
4. **Custom domain** (optional) → Settings → Pages → Custom domain, then add DNS records at your registrar and tick **Enforce HTTPS**.

After that, every push to `main` publishes the site to `https://workarounds81.github.io/cityprint/` (or your custom domain).
