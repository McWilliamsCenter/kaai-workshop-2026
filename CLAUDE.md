# KAAI Workshop Website — Project Spec

## What this is

A static website announcing the **KAAI Workshop on Foundation Models & Agentic Methods for
Astrophysical Simulation**, hosted at Carnegie Mellon University, August 31–September 3.
This is the first workshop in the sequence run under the Simons Foundation
**Keystone Astronomy & AI (KAAI) Fellows Program**
(https://www.cmu.edu/astro-cosmology/research/simons-kaai-fellows/index.html).

This is a **draft / save-the-date stage site**. Several sections are intentionally TBD and
will be filled in over the coming months. The site should look complete and professional
even with placeholder content — TBD sections should read as "more info coming soon," not
as broken or unfinished parts of the page.

Design reference (structure only, not content density): https://sbi-galev.github.io/2026/index.html
That site is a good model for section layout and typography but is more information-dense
than we need right now. Prefer a shorter, less cluttered page.

---

## Tech stack (decided)

- **Plain HTML + CSS + minimal vanilla JS.** No build step, no framework, no static site
  generator. This keeps it trivial to hand-edit later and trivial to deploy.
- Single page (`index.html`) with anchor-linked sections, following the reference site's
  pattern. Do not split into multiple pages yet — everything fits on one page at this stage.
- **Hosting: GitHub Pages.** Repo root (or `/docs`) serves directly, no CI/build pipeline
  needed. Structure the repo so `index.html` is deployable as-is via Pages settings.
- Fonts: use a system font stack or a single Google Font pairing (serif for headings, clean
  sans for body) loaded via `<link>` — avoid heavy font-loading JS.
- No JS framework, no npm dependencies unless there's a strong reason. Small vanilla JS is
  fine for: smooth-scroll nav, mobile nav toggle, maybe a simple countdown to the workshop
  dates.

## Design direction (decided)

**Clean, minimal academic style** — closer to the reference site than to a flashy conference
page. Lots of whitespace, restrained color use, clear typographic hierarchy, no stock photos,
no heavy gradients or animation.

Since there's no existing workshop-specific logo or visual identity yet, build the placeholder
identity around **CMU's institutional palette** rather than inventing an unrelated brand:

- Primary accent: **CMU Red** `#C41230`
- Secondary: near-black `#1A1A1A` / dark gray for body text
- Neutral backgrounds: white and a very light warm gray (`#FAFAFA` / `#F5F4F2`)
- Use red sparingly — section labels, links, hover states, key dates — not as large background
  blocks. Let whitespace and typography carry the design.
- No logo yet. Use a simple text wordmark for the workshop name in the header (e.g. small caps
  or letter-spaced sans). Leave a clearly marked spot/placeholder in the HTML (`<!-- TODO: logo -->`)
  where a real logo or KAAI program mark can be dropped in later.
- Typography: a serif or slab-serif for the H1/hero title (gives it academic conference gravitas,
  similar to the reference site's feel), clean sans-serif for nav, body, and cards.

## Tone / copy voice

Precise, understated, technically confident — written for a technically literate audience.
Avoid marketing language ("game-changing," "revolutionary"). Avoid unnecessary adjectives.
Short declarative sentences. This mirrors how the workshop itself is being framed: small,
informal, focused on substance.

---

## Site structure (single page, anchor nav)

Nav bar: `Overview` · `Topics` · `Schedule` · `Speakers` · `Hackathon` · `Committee` · `Registration`

### 1. Header / Hero
- Workshop title: **Foundation Models & Agentic Methods for Astrophysical Simulation**
- Subtitle line: "A KAAI Workshop · Carnegie Mellon University"
- Dates: **August 31 – September 3**
- Location: Carnegie Mellon University, Pittsburgh, PA
- One-line framing: first workshop in the Simons Foundation Keystone Astronomy & AI (KAAI)
  Fellows Program workshop series.
- Optional: a subtle countdown or "Save the date" badge — keep understated, not gimmicky.

### 2. Overview
Short paragraph(s) covering:
- The workshop is small and informal, emphasizing cutting-edge work presented to a
  technically literate audience, identifying important directions in the emerging field,
  and building new collaborations.
- It combines a conference (talks + discussion) with a hackathon.
- Link out to the KAAI Fellows Program page for broader program context:
  https://www.cmu.edu/astro-cosmology/research/simons-kaai-fellows/index.html

### 3. Scientific Topics
Two-column or two-card layout, one per theme:
- **Foundation models for astrophysics** — how foundation models can be used to represent,
  manipulate, compress, compare, and interpret astrophysical simulations and observations.
- **Agentic science loops** — how agentic methods can responsibly augment the scientific
  research process.

### 4. Format (Conference + Hackathon)
Make the dual structure visually clear — e.g. a simple two-block timeline:
- **Mon–Tue, Aug 31–Sep 1: Talks & Discussion** — invited talks and discussion on novel
  research at the intersection of foundation models, agentic methods, and astrophysical
  simulation.
- **Wed–Thu, Sep 2–3: Astro+AI Hackathon** — a Pittsburgh-wide hackathon open to CMU/Pitt
  participants across physics and ML, featuring benchmark and open-discovery challenge
  tracks with prizes.

### 5. Schedule — **TBD**
Placeholder section, clearly labeled "Schedule — coming soon" / "Detailed schedule to be
announced." Keep the Mon–Thu date structure visible (from section 4) but no talk-by-talk
detail yet. Don't fake a schedule table with fabricated entries.

### 6. Invited Speakers — **TBD**
Placeholder card grid (e.g. 4–6 empty/placeholder cards or a simple "Speaker list to be
announced — check back soon" message). Don't invent speaker names.

### 7. Hackathon — **TBD** (format details)
We know: Pittsburgh-wide, open to CMU/Pitt across physics and ML, benchmark track +
open-discovery track, prizes. Format details (team formation, judging, submission process,
compute resources) are TBD — mark clearly as forthcoming.

### 8. Organizing Committee
List all six, CMU affiliation, no fabricated titles/bios unless supplied:
- Matt Ho
- Barnabás Póczos
- Rupert Croft
- Tiziana Di Matteo
- Hy Trac
- Rachel Mandelbaum

Simple card or list layout: name + affiliation (Carnegie Mellon University). Leave room to
add a homepage link per person later (see reference site's `[Name] [[Homepage]]` pattern) —
but don't fabricate links; leave as plain text unless a URL is provided.

### 9. Registration — **TBD**
Placeholder: "Registration will open in [Month]. Check back for details." No form, no fake
dates — just a clear holding message and maybe a mailto or contact line if/when available.

### 10. Footer
- Workshop name, dates, CMU
- Link to KAAI Fellows Program page
- Contact email placeholder (`<!-- TODO: contact email -->`)
- Optional: link back to McWilliams Center for Cosmology & Astrophysics

---

## Explicit non-goals for this draft

- No fabricated speaker names, schedule times, or hackathon rules — leave TBD sections
  honestly marked rather than inventing plausible-sounding placeholder content.
- No dependency on a CMS, database, or backend — must remain a fully static site deployable
  via GitHub Pages with zero server-side logic.
- No build tooling (webpack/vite/etc.) — keep it simple enough to edit by hand.
- Don't reuse CMU's official logo/wordmark images (trademark/branding restrictions) — the
  placeholder identity should be *inspired by* CMU red, not a reproduction of official CMU
  or McWilliams Center marks.

## Open items to fill in later (leave TODO comments in code)

- Real logo / visual mark for the workshop
- Contact email
- Speaker names + affiliations + photos
- Full schedule
- Hackathon rules, prize details, judging criteria
- Registration link/form
- Venue/room details at CMU
- Individual committee member homepage links

## Deployment notes

- Repo should be structured so GitHub Pages can serve it directly from `main` (root or
  `/docs`) with no Actions/build step required.
- Keep all assets (CSS, images, JS) in relative paths so it works both locally
  (open `index.html` directly) and on GitHub Pages.
- Recommend a `README.md` with basic instructions for enabling GitHub Pages in repo settings
  and where to edit each TBD section.