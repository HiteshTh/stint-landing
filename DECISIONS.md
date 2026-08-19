# DECISIONS.md

## 1. Why this approach over the obvious alternative I rejected?

The obvious default was a React/Next.js scaffold with a component library — it's what
most "premium SaaS landing page" tutorials reach for. I rejected it for a plain
HTML/CSS/JS single file instead. Reasoning: the brief grades UI craft and taste, not
framework choice ("Stack: your call... We're grading judgment, not tool choice"), and a
static page removes an entire layer of build tooling, dependency, and hydration issues
that add risk without adding visible quality on a page this size. It also means the
deployed page is the exact same file as the repo — nothing gets lost or altered in a
build step, and there's nothing in the stack I can't explain line-by-line.

I also rejected a design-tool handoff (e.g. Figma-to-code) — I wanted every spacing and
color decision to trace back to a real CSS variable I chose on purpose, not an exported
approximation.

## 2. One trade-off I made under the time limit, and what I'd do with a real week

**Trade-off:** The theme toggle doesn't persist across page reloads — it resets to dark
on refresh. A real implementation would store the preference (localStorage, or a cookie
if I wanted it to survive on the server side too) and also respect the user's OS-level
`prefers-color-scheme` on first visit instead of always defaulting to dark.

**With a real week**, I'd also: add a second, content-driven page (e.g. a pricing page)
so the "premium" feel holds up under navigation, not just on one screen; run actual
Lighthouse/axe accessibility audits and fix contrast ratios properly rather than by eye;
and replace the CSS-only bar chart in the dashboard mock with a tiny real chart (or a
short looping video/GIF) showing an invoice actually being generated, since a static mock
is the weakest form of "show, don't just claim."

## 3. Where I used AI tools, and what I verified/changed afterward

I used Claude to generate the initial HTML/CSS/JS in one pass from a design brief I
specified first (color tokens, type pairing, layout concept, signature element) rather
than asking for "a landing page" and taking whatever came back — so the distinctive
choices (the brass/ledger palette, the live timer as the signature element, the honest
copy constraint) were decided before any code was written, not discovered in the output.

After generation, I personally checked: that the page parses without broken markup; that
the 860px breakpoint actually collapses cleanly at 390px and holds structure at 1440px
with no horizontal scroll; that `prefers-reduced-motion` disables the ticking timer and
scroll-reveal animation; that focus states are visible for keyboard navigation; and that
no copy in the page claims a fake user count, testimonial, or logo — every number on the
page (the 4 mock clients, the hourly rate, the tracked hours) is clearly framed as a
product demo, not a marketing claim. I also read every line of the JS (timer formatting,
the IntersectionObserver reveal, the Konami-code listener) and can walk through what each
one does and why it's structured that way.
