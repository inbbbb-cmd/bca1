# Immigramind — landing page

Landing page for **Immigramind** — an AI immigration assistant by **Blue Card Agency**
(BCA‑Relocation GmbH, Berlin). Static site, no build step — deploys to GitHub Pages / Vercel.

> **Status: Beta / draft.** The page is currently `noindex`. Several items still need
> legal/business sign‑off before public launch — see **Open items** below.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The Immigramind landing — self‑contained (inline CSS/JS) |
| `fonts.css` + `fonts/` | Self‑hosted Inter + Syne (page) and Poppins (legal pages) — GDPR‑safe, no request to Google |
| `impressum.html` | Impressum (real entity data) |
| `datenschutz.html` | Datenschutzerklärung (draft template; red = to fill in) |
| `styles.css` | Styles used by the Impressum / Datenschutz pages |
| `favicon.svg` | Favicon (legal pages) |
| `.github/workflows/deploy-pages.yml` | Auto‑deploy to GitHub Pages on push to `main` |
| `.nojekyll` | Serve files as‑is on GitHub Pages |

## Run locally

```bash
python -m http.server 8000   # then open http://localhost:8000
```

## Deploy

- **GitHub Pages:** pushing to `main` triggers the workflow (auto‑enables Pages + deploys).
  Live at https://inbbbb-cmd.github.io/bca1/ . Remove the `noindex` meta in `index.html` when ready.
- **Vercel:** import the repo, Framework **Other**, empty build command, output `.`.

## Open items (before public launch)

- **RDG wording:** position as *information & orientation* + *human BCA experts handle the case*,
  not “fully replaces legal consultation”; soften the chat demo; add a disclaimer.
- **Verify all claims** (cases, years, languages, reviews, awards, partners) — must be truthful (UWG).
- **Datenschutz:** fill the red placeholders (hosting, log‑retention, date); have a German lawyer
  review Impressum + Datenschutz.
- **Lead capture:** optional real form with GDPR consent instead of mailto/Telegram.
- **Brand:** confirm name casing (using “Immigramind”) and which Telegram channel is canonical.
