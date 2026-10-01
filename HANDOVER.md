# AI KAMAI — MASTER HANDOVER (for any new agent)

> Read this top to bottom before doing ANY work. Owner: Somil Sharma (+91 77370 77479, IST).
> Last updated: 1 Oct 2026. Status: ALL PRODUCTS BUILT, TESTED, LIVE. Founder launch actions pending (see "Founder gates").

---

## 1. WHAT WE ARE DOING (the mission)

**AI Kamai** is a creator brand that sells honest digital products to individuals (Hinglish-speaking, Instagram-first, India) to earn a **₹50K fuel fund**, which then funds B2B SaaS (Beyond Pixells OS family). This is **Phase 0 "Fuel"** of the company master plan.

Revenue ladder (one-time prices, UPI, WhatsApp delivery):
| Product | Price | What it is | Live URL |
|---|---|---|---|
| AI Prompt Vault | ₹499 | 177-prompt web app (search, 1-tap copy, profile auto-fill, favorites) | https://somilsharma2000.github.io/aikamai/vault/ |
| AI Agency Launch Kit | ₹999 | 10-tab agency OS (25 scripts, objection bank, 12-niche directory, pricing calculator, 30-day calendar) | https://somilsharma2000.github.io/aikamai/kit/ |
| SaaS Starter Kit | ₹4,999 | Production multi-tenant SaaS codebase (Next.js 14 + TS + Prisma, scrypt auth, UPI checkout, 15 tests, 5 docs). Private repo: somilsharma2000/aikamai-starter-kit, release v1.0.0 | delivered as zip from GitHub release |
| Store (front door) | — | one-page store, all 3 products LIVE | https://somilsharma2000.github.io/aikamai/ |

Free sample (funnel entry): https://somilsharma2000.github.io/aikamai/vault/free.html
Fee-corrected target: 20 Agency Kits + 7 Starter Kits ≈ ₹51.6K net (Instamojo ~2-3% fees).

## 2. LAWS (break these and the work is rejected)

1. **NEW BRAND LAW:** AI Kamai stands COMPLETELY ALONE. Zero references to Beyond Pixells, Gym OS, Dentist OS, or any old property in store/products/reels/copy/footer. Proof = AI Kamai's own live products + free sample + "built in a day, zero budget" record. Starter Kit was built fresh from scratch (never extracted from old repos).
2. **NO EMOJI LAW:** no emoji as icons/stickers anywhere. Use inline SVG icons.
3. **NO INVENTION LAW:** no fake customers, stats, testimonials, urgency, discounts, or production status. Honest claims only. 7-day refund promise is real.
4. **MASTER PROMPT LAW (highest):** "Autonomous Product Transformation Engine" — inspect → judge → research → redesign → implement → test → self-critique → improve again. Act, don't report. 5-pass rule: FUNCTION → UX → VISUAL → ENGINEERING → CRITICAL REVIEW. Zero-generic rule: if another company could use the UI unchanged, redesign it.
5. **40-LAYER AUDIT LAW:** QA-ENGINE-style module passes, never monolithic "improve everything". Pass B recheck is the floor, not the ceiling. Visual regression = before/after at desktop + tablet + 390px after any UI change.
6. **One product in build at a time. 60-day kill criteria per pipeline stage.**
7. **Hinglish copy** everywhere (user-facing); code/docs in English.
8. **Update the notes** whenever plan work happens (see §6).

## 3. ARCHITECTURE / REPOS

- **somilsharma2000/aikamai** (public, Pages from main, .nojekyll present) — store index.html, vault/ (index.html + prompts.js + prompts2.js + free.html), kit/index.html, og-image.png, robots.txt, sitemap.xml, llms.txt. Pure HTML/JS, zero framework, no build step. Vault + kit are SHA-256 key-gated (key via ?key= param or localStorage after first unlock).
- **somilsharma2000/aikamai-starter-kit** (PRIVATE) — the ₹4,999 product. GitHub release v1.0.0 has the clean delivery zip (no .env/node_modules/dev.db). Access needs GITHUB_TOKEN env (already a stored secret in the agent workspace).
- **Access keys** (Vault/Kit unlock keys) are NOT written in public files. They live in the owner's private notes: `/app/notes/digital-product-launch/launch-runbook.md`. If you are a Base44 superagent for this owner, read them there.
- **Ledger:** every real sale gets recorded in the `Sale` entity (gross/fees/net/source) of the owner's agent app. Buyer list/CRM: `Lead` + `LeadActivity` entities.
- **Monitoring:** site-health-check skill (`bash /app/.agents/skills/site-health-check/run.sh`) checks 6 AI Kamai URLs — must stay 14/14.

## 4. WHAT IS DONE (do not redo)

Built, tested, Pass-B'd, live-verified as of 1 Oct 2026:
- Store v2: responsive composition (1→2→3 cols across 320-1440px), motion system (reveals w/ prefers-reduced-motion, hover lifts, focus rings), live-state copy, Starter Kit marked LIVE, Organization+Products+FAQPage JSON-LD, canonical, trust strip. 6 viewports zero overflow, 0 JS errors.
- Vault v1.1: 200 prompts, 15 categories, search, favorites (localStorage), profile auto-fill (naam/service/niche/city → "Personalized" copy), SVG icons.
- Kit v1.1: 10 tabs (playbook, scripts 25, objections 10, niches 12, pricing calculator + benchmarks, templates, delivery system, legal/money, 30-day calendar, AI Kamai case study).
- Starter Kit v1.0.0: 15/15 vitest green, build clean, cross-tenant isolation verified, payment idempotency verified (double webhook cannot double-charge), vertical-swap dry run proven in under 4 min (gym example), delivery zip packaged.
- 30 reel scripts ready (shoot-ready, honest-claims law applied; reels 28/30 ship ONLY with real buyers/numbers).
- Launch-day runbook with copy-paste DM/delivery/refund templates (in notes).
- robots/sitemap/llms.txt/og-image all live, 200.

## 5. FOUNDER GATES (what only Somil can do — nothing else blocks launch)

1. Register **@aikamai** Instagram handle.
2. Create **Instamojo** account (free) → get UPI checkout link for each product.
3. **Shoot reels 1, 5, 24** (scripts in notes/reel-scripts.md and repo content/).
4. Optional: founder photo to replace the "SS" avatar on the store.
5. After handle: set up auto-DM (LinkDM free 1000 DMs/mo; ManyChat free plan useless since Mar 2026).

## 6. NOTES / SOURCE OF TRUTH (owner's private notes, keep updated)

- `/app/notes/digital-product-launch/` — main.md (status log), launch-blueprint.md, launch-runbook.md, product-specs.md, checklists.md, content-engine.md, reel-scripts.md, revenue-ledger.md, brand-guidelines.md, dev-conventions.md
- `/app/notes/company-master-plan/` — main.md, operating-system.md, product-portfolio.md, audit-layers.md (the 40-layer law)
- Update main.md with a dated status-log line whenever ANY plan work happens. Never mark COMPLETE without the full quality cycle.

## 7. CONVENTIONS FOR CHANGES

- Deploy = push to main (Pages auto-serves). Pages uses Jekyll → **.nojekyll must exist** at root (it does; any new repo needs it).
- Commit messages: lowercase, descriptive, no emoji.
- After any UI change: verify 390px (scrollWidth == viewport, 0 JS errors) at minimum; full pass = 320/390/430/768/1024/1440.
- After any store copy change: re-verify honest claims (prices 499/999/4,999, no invented proof).
- Run site-health-check after deploys. Keep 14/14.
- Cache-bust with `?cb=` when verifying Pages (CDN can serve stale HTML briefly).

## 8. WHAT'S NEXT (priority order, after founder gates)

1. Founder launches (reels daily, reply to comments within 5 min, DM keyword funnel: "SAMPLE" → free link).
2. Feed every sale to the agent → Sale entity → weekly totals vs ₹50K target.
3. Iterate products from real buyer feedback (refunds = improvement loop, not losses).
4. At ₹50K: Phase 1 (Coaching OS) begins — that's a new blueprint, not this one.

**Golden rule: if something is wrong, do not ask permission to fix it — fix it, test it, log it.**

## Operating law (1 Oct 2026 — supersedes earlier process notes)

ALL product work runs the **Autonomous Product Transformation Engine**: DISCOVER→INSPECT→RESEARCH→DIAGNOSE→PRIORITIZE→DESIGN→IMPLEMENT→TEST→SELF-CRITIQUE→IMPROVE→RE-TEST. Act, don't report; fix before asking; report per cycle as FOUND/WHY/ACTION/VERIFICATION/REMAINING. Hard rules: zero-generic, 5-pass (FUNCTION→UX→VISUAL→ENGINEERING→CRITICAL REVIEW), one product at a time (Store→Free→Vault→Kit→Starter→ops→ecosystem), P0 before P3, no invented claims ever, distinguish VERIFIED FACT / INFERENCE / DESIGN JUDGMENT. Master audit standard: complete commercial operating system (~40 domains + recursive unknown-domain check) — full register in the owner's notes at company-master-plan/business-audit-universe/.

Estate state after cycle 4: content AES-256-GCM encrypted (no plaintext in public repo; plaintext + build script archived at aikamai-starter-kit/content-archive/, PRIVATE), Terms/Privacy/Refund live + favicon + OG everywhere, all quantitative claims verified true (17 tests, 200 prompts, 15 categories, 25 scripts, 10 objections, 12 niches, 30-day calendar), health check 14/14, CRM Lead.source includes aikamai-ig / aikamai-store.

## Estate v2 (1 Oct cycle 7)

Vault + Kit are now FULL premium redesigns (store design language: dark, gradient, blur sticky bars, reveal motion w/ reduced-motion fallback, focus rings, typed-key unlock on lock screens). Vault: 200 prompts (23 new deep prompts), how-to-use guide, 15 category tips, 1/2/3-col grid. All claims say 200. Plaintext + build script in private content-archive. Grid law: 1fr tracks need minmax(0,1fr).
