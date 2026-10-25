# City Print & Signs — cityprint.sg

Website for City Print & Signs Pte Ltd (Singapore). A single, fast page made of plain HTML, with no framework and no build step.

- Live: https://cityprint.sg/ (DNS at Qoxy → GitHub Pages)

## Files

```
index.html             The whole site (styles and script are inline for speed)
404.html               Not-found page
assets/img/work/       Project photos, compressed to WebP (480px and 960px versions)
assets/img/            Logo, favicon, social-share image
assets/Cityprint/      Original uploaded photos (kept in the repo, NOT published)
robots.txt, sitemap.xml
.github/workflows/pages.yml   Publishes the site on every push
```

## Editing

- **WhatsApp number:** search `6589302515` in `index.html`.
- **Add a project photo:** export it as WebP at 480px and 960px wide into `assets/img/work/`, then copy one `<figure class="w" ...>` line in the Projects section and change the file name, caption and `data-cat` (`shop`, `light`, `pillar`, `office` or `expo`).

## Hosting (GitHub Pages)

1. Settings → Pages → Source: **GitHub Actions** (one-time).
2. Custom domain: Settings → Pages → Custom domain = `cityprint.sg`, then at the domain registrar add:
   - `A` records for `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www` → `workarounds81.github.io`
   - When the check turns green, tick **Enforce HTTPS**.
