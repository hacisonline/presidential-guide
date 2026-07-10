# CLAUDE.md — Presidential user guide site (guide-site/)

You are working on the **customer-facing user guide** for Tesseract Home for The
Presidential: a standalone, single-page interactive site. Read this whole file first.

## What this is (and is not)

- **Its OWN git repo**, deployed via GitHub Pages (hacisonline.github.io/presidential-guide,
  remote `presidential-guide`). It sits inside the app folder for convenience but is
  **gitignored by the app repo** — never push it to the app remote, never import any of
  it into the app, and never copy app code here.
- **The one deliberate brand exception:** this site wears the **Tesseract platform brand**
  (navy + blue/green, Inter + JetBrains Mono, the official cube mark) because it is a
  product document ABOUT the deployment, not part of the building app. The app itself
  stays pure Presidential (ink + crown gold) — do not leak either brand into the other.
- **Audience: customers** (tenants, their staff, building management evaluating the
  product). No RERA/registry numbers, no internal jargon, no dev language.

## Rules

1. Single self-contained `index.html` — no build step, no dependencies. Keep it that way.
2. **Content truth comes from the app repo's `docs/FEATURES.md`** (the audited
   inventory). The guide must track the app honestly: never document a feature the app
   does not have, and carry the app's honest Phase-1 notes (mock seams) where relevant.
3. Reveal animations MUST carry a guaranteed-legibility fallback (timer + hashchange) —
   a jump-to-anchor once left sections invisible (caught live, session 16). Preserve it.
4. Verified mobile-perfect at 360/390/414px (no overflow, 44px targets) and desktop.
   Hold both, like the app's doctrine.
5. Preview loop during app-repo sessions: copy `index.html` into the app's `public/`
   temporarily to view on the dev server, then REMOVE the copy — it must never ship
   with the app.

## Deploy

Commit in THIS folder's repo, push to `presidential-guide`, GitHub Pages serves main.
Owner pushes from his Mac (agents have no credentials).

`AGENTS.md` is an identical mirror of this file — change both together.
