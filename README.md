# Stint — Premium Home Page

A landing page for **Stint**, an invented product concept: time tracking and one-click
invoicing for freelancers. Built for the Acdyon Technologies frontend challenge (Part 2).

## Stack

Plain HTML, CSS, and vanilla JavaScript — one file, no build step, no framework, no
dependencies beyond a Google Fonts CDN link. This was a deliberate choice, not a shortcut:
see `DECISIONS.md`.

## Run it locally

No install needed. Either:

- Double-click `index.html` to open it directly in a browser, or
- From this folder, run a tiny local server so relative paths behave the same as they
  will in production:

  ```bash
  python3 -m http.server 8000
  # then open http://localhost:8000
  ```

## What's in the page

- **Hero** — value prop + a live-ticking demo timer (the product's core mechanic, shown
  in action rather than described)
- **Product section** — a mock dashboard card: 4 clients, hours, invoice status
- **Features** — 3 cards, plain copy, no invented stats
- **How it works** — a real 3-step sequence (track → invoice → get paid)
- **CTA + footer**
- **Dark/light toggle** — full theme swap via CSS custom properties, not partial
- **Easter egg** — Konami code (↑ ↑ ↓ ↓ ← → ← → b a) triggers a small toast

## Deploying (free, ~2 minutes)

**Option A — Netlify Drop (fastest, no account needed to preview):**
1. Go to https://app.netlify.com/drop
2. Drag `index.html` onto the page
3. It gives you a live URL immediately. Sign up (free) to keep it permanently.

**Option B — GitHub Pages (what most reviewers expect to see, since they also want a repo link):**
1. Create a new repo on GitHub, e.g. `stint-landing`
2. Add `index.html`, `README.md`, and `DECISIONS.md` to it and push
3. In the repo: Settings → Pages → Source: `main` branch, `/ (root)` → Save
4. GitHub gives you a URL like `https://<username>.github.io/stint-landing/` within a minute or two

Do Option B — it gives you both the deployed URL *and* the GitHub repo link the form asks for, from one action.

## Responsive behavior

Tested against 390px (mobile) and 1440px (desktop) breakpoints via a single media query
at 860px that collapses the hero to one column, stacks the feature/step grids, and hides
one less-critical column in the dashboard table. No horizontal scroll at either width.
