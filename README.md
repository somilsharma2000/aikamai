# AI Kamai — one-page store

The digital products storefront for **AI Kamai** (creator brand, separate from Beyond Pixells).
Live at: https://somilsharma2000.github.io/aikamai/

## What's here
- `index.html` — the entire store: hero, live-proof chips, 3 products, free sample CTA, FAQ, sticky WhatsApp CTA.

## Products (prices locked)
1. AI Prompt Vault — ₹499
2. AI Agency Launch Kit — ₹999
3. SaaS Starter Kit — ₹4,999

## How to edit
Everything is in one HTML file with inline CSS. Open a PR or edit directly; GitHub Pages redeploys on push to main.

## Rules (from /app/notes/digital-product-launch/)
- Honest copy only: no invented testimonials, stats, revenue. Claims must match the Revenue Ledger.
- Buy CTAs currently go to WhatsApp (+91 77370 77479) until the Instamojo checkout goes live — no dead ends ever.
- Product cards flip from "Launching this week" to real buy links when products ship.
- Mobile-first: verify 390px zero horizontal overflow + 0 JS console errors after every change.

## Conventions
- Lowercase specific commit messages ("add instamojo checkout to vault card").
- `.nojekyll` stays at repo root (Pages deploy law).
