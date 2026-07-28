# KAAI Workshop Website

Static save-the-date site for the KAAI Workshop on Foundation Models & Agentic Methods for
Astrophysical Simulation (Carnegie Mellon University, August 31 – September 3, 2026).

Plain HTML/CSS/JS. No build step, no dependencies.

## Local preview

Open `index.html` directly in a browser, or serve the directory:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Where to edit each TBD section

All content lives in `index.html`; styling in `css/style.css`; the nav toggle and countdown
script in `js/main.js`.

| Section | Look for | Notes |
|---|---|---|
| Schedule | `#schedule` section | Structure is set (times, session types); still needs real speaker names in place of "Speaker TBD" |
| Speakers | `#speakers` section, `.speaker-card.placeholder` cards | Replace placeholder cards with real name/affiliation/photo cards |
| Hackathon details | `#hackathon` section | Team formation, judging, submission process, compute resources |
| Registration | `#registration` section | Add real open date and/or registration link/form |

To swap the logo: drop a new source image anywhere and regenerate sizes with
`sips -z <px> <px> source.png --out img/<name>.png` (see sizes below). Don't use CMU's
official logo/wordmark (trademark restrictions).

The countdown target date is set in `js/main.js` (`workshopStart`).

## Images

`img/` holds pre-sized, web-optimized copies of the logo. Keep source art (large master
files) out of the repo and only commit the sizes actually referenced by the site:

| File | Size | Used for |
|---|---|---|
| `img/logo.png` | 160×160 | header + footer logo |
| `img/logo-hero.png` | 480×480 | hero logo, next to the title |
| `img/apple-touch-icon.png` | 180×180 | iOS home-screen icon |
| `img/favicon-32.png` | 32×32 | favicon |
| `img/favicon-16.png` | 16×16 | favicon |
