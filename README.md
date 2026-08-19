<div align="center">

# ⏱ Stint

### A landing page for a time-tracking & invoicing product, built for freelancers who bill by the hour.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![No Framework](https://img.shields.io/badge/Framework-None-2C3742?style=for-the-badge)
![Responsive](https://img.shields.io/badge/Responsive-390px→1440px-D3963F?style=for-the-badge)

</div>

---

## What this is

**Stint** is an invented product: a time tracker that turns billable hours into
client-ready invoices automatically. This repo is its home page — one static
HTML file, built to earn the "wow, I want an account" reaction in the first
few seconds, with no fabricated stats, testimonials, or logos anywhere on it.

> *"Every minute, accounted for."*

---

## Design language

<table>
<tr><td width="50%" valign="top">

**Palette — ink & brass**

Built around a pocket-watch feel: dark ledger tones with a warm brass accent,
never the default AI cream-and-terracotta or neon-on-black look.

![#10151A](https://img.shields.io/badge/%2010151A-10151A?style=flat-square) `--ink` · background
![#1A222A](https://img.shields.io/badge/%201A222A-1A222A?style=flat-square) `--panel` · cards
![#D3963F](https://img.shields.io/badge/%20D3963F-D3963F?style=flat-square) `--brass` · accent, CTA
![#7E9683](https://img.shields.io/badge/%207E9683-7E9683?style=flat-square) `--sage` · "paid" state
![#C06B54](https://img.shields.io/badge/%20C06B54-C06B54?style=flat-square) `--rust` · warnings
![#EDE6D6](https://img.shields.io/badge/%20EDE6D6-EDE6D6?style=flat-square) `--parchment` · text

</td><td width="50%" valign="top">

**Type system**

| Role | Typeface | Used for |
|---|---|---|
| Display | Bricolage Grotesque | Headlines |
| Body | Inter | Paragraph copy |
| Mono | IBM Plex Mono | Timer, numbers, labels |

Numbers get their own typeface on purpose — this is a product about counting
minutes and dollars, so the mono face shows up everywhere something is being
measured.

</td></tr>
</table>

---

## Page anatomy

```mermaid
flowchart TD
    A["🕐 Hero<br/>Value prop + live timer"] --> B["📊 Product<br/>Dashboard mock, 4 clients"]
    B --> C["✨ Features<br/>3 cards"]
    C --> D["🔢 How it works<br/>Track → Invoice → Get paid"]
    D --> E["📣 CTA<br/>Closing call to action"]
    E --> F["Footer"]

    style A fill:#10151A,stroke:#D3963F,stroke-width:2px,color:#EDE6D6
    style B fill:#1A222A,stroke:#D3963F,color:#EDE6D6
    style C fill:#1A222A,stroke:#D3963F,color:#EDE6D6
    style D fill:#1A222A,stroke:#D3963F,color:#EDE6D6
    style E fill:#10151A,stroke:#D3963F,stroke-width:2px,color:#EDE6D6
    style F fill:#1A222A,stroke:#2C3742,color:#A6AB9E
```

### The signature element

The hero doesn't describe the product — it runs it. A live timer counts up in
real time next to a mock client name and hourly rate, so the first thing a
visitor sees is the product actually working, not a claim about what it does.

---

## Feature highlights

| | |
|---|---|
| ⏱ **Auto time capture** | A lightweight timer runs per client, so hours don't have to be reconstructed from memory on Friday. |
| 🧾 **One-click invoices** | Tracked hours become a formatted invoice instantly — no spreadsheet. |
| 📋 **Client-ready reports** | Every client gets a clean hours-and-cost breakdown, nothing to explain. |

---

## Interaction & motion

- **Live timer** — ticks every second in the hero, the page's one ambient animation
- **Scroll reveal** — sections fade/lift into view once, consistently, not scattered per-element
- **Dark / light toggle** — a full theme swap via CSS custom properties, all-or-nothing
- **Konami code** `↑ ↑ ↓ ↓ ← → ← → b a` — a small hidden toast, for anyone who tries it
- Respects `prefers-reduced-motion` — ticking and reveal animations disable cleanly

---

## Honesty constraint

No part of this page invents a user count, a testimonial, or a logo. The
dashboard section is clearly a **product demo** with sample data, not a
marketing claim about real customers. Every number visible on the page is
either a UI mock or standard, non-specific SaaS copy ("no credit card,
cancel anytime").

---

<div align="center">

*Built as a design exercise — see `DECISIONS.md` for the reasoning behind each choice.*

</div>
