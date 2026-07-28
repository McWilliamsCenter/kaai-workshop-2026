# KAAI Workshop Website

Static save-the-date site for the KAAI Workshop on Foundation Models & Agentic Methods for
Astrophysical Simulation (Carnegie Mellon University, August 31 – September 3, 2026).

Plain HTML/CSS/JS — no build step, no dependencies.

## Local preview

Open `index.html` directly in a browser, or serve the directory:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Enabling GitHub Pages

1. Push this repo to GitHub.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch".
4. Choose branch `main`, folder `/ (root)`, then **Save**.
5. The site will be published at `https://<org-or-user>.github.io/<repo-name>/`.

No Actions workflow or build step is required — `index.html` at the repo root is served as-is.

## Where to edit each TBD section

All content lives in `index.html`; styling in `css/style.css`; the nav toggle and countdown
script in `js/main.js`.

| Section | Look for | Notes |
|---|---|---|
| Logo | `img/logo.png`, used in header (`.wordmark-logo`) and footer (`.footer-logo`) | To replace: drop a new source image anywhere, regenerate sizes with `sips -z <px> <px> source.png --out img/<name>.png` (see sizes below), and don't use CMU's official logo/wordmark (trademark restrictions) |
| Contact email | `mailto:mah2406@columbia.edu` links in Registration and Footer | Update both if the contact changes |
| Schedule | `#schedule` section | Replace placeholder with talk-by-talk detail once finalized |
| Speakers | `#speakers` section, `.speaker-card.placeholder` cards | Replace placeholder cards with real name/affiliation/photo cards |
| Hackathon details | `#hackathon` section | Team formation, judging, submission process, compute resources |
| Registration | `#registration` section | Add real open date and/or registration link/form |
| Committee homepage links | `#committee` section, `.committee-card` | Add `<a>` links per person once URLs are supplied |
| Venue/room details | Hero and Format sections | Currently only "Carnegie Mellon University, Pittsburgh, PA" |

The countdown target date is set in `js/main.js` (`workshopStart`).

## Images

`img/` holds pre-sized, web-optimized copies of the logo — keep source art (large master
files) out of the repo and only commit the sizes actually referenced by the site:

| File | Size | Used for |
|---|---|---|
| `img/logo.png` | 160×160 | header + footer logo |
| `img/logo-hero.png` | 320×320 | hero logo, next to the title |
| `img/apple-touch-icon.png` | 180×180 | iOS home-screen icon |
| `img/favicon-32.png` | 32×32 | favicon |
| `img/favicon-16.png` | 16×16 | favicon |
