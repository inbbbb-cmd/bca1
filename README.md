# BCA — Coming Soon landing page

Interactive "coming soon" placeholder for **BCA — Business Consulting Automation**
(an AI Legal & Immigration SaaS platform by Blue Card Agency). Built from the BCA
investor deck, in the deck's brand style (deep indigo `#393B86` + gold `#F3D956`).

It's a **static site** — plain HTML/CSS/JS, no build step — so it deploys as‑is to
both **Vercel** and **GitHub Pages**.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Page markup and content |
| `styles.css` | Brand design system, layout, animations |
| `main.js` | Scroll reveals, counters, mobile nav, hero particles |
| `favicon.svg` | Logo favicon |
| `og-image.png` | Social share preview (1200×630) |
| `.nojekyll` | Tells GitHub Pages to serve files as‑is |

## Run locally

No tooling required — just open `index.html`. For a closer-to-production check:

```bash
# Python (any 3.x)
python -m http.server 8000
# then open http://localhost:8000
```

## Deploy

### Vercel
- **Dashboard:** New Project → import this repo → Framework Preset **Other** →
  leave Build Command empty, Output Directory `.` → Deploy.
- **CLI:** `npm i -g vercel` then `vercel` in this folder.

### GitHub Pages
Push to GitHub, then **Settings → Pages → Build and deployment → Source: Deploy
from a branch**, pick your branch and `/ (root)`. The included `.nojekyll`
ensures files are served untouched.

## Customize

- **Contacts / copy:** edit directly in `index.html`.
- **Colors:** change the CSS variables under `:root` in `styles.css`.
- **Call to action:** the hero and footer buttons open the visitor's email client
  via `mailto:info@bluecardagency.de`. Change the address in `index.html`.

## Notes
- The source `*.pdf` deck is git‑ignored on purpose (it's not part of the site).
- Content is intentionally marketing‑facing; investor specifics from the deck
  (funding ask, detailed financials) are kept off the public page.
