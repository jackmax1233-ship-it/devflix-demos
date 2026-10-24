# BUILD NOTES — RQ Junk Removal preview site

Built 2026-10-23 (night batch) by Devflix. Business: **RQ Junk Removal**
("Real Quick & Reliable Junk Removal"), Western Sydney NSW, Australia —
IG @rq_junk_removal (482 followers, 38 posts, public; author_id
17841437696296458). Contact: NOT contacted — build only; parent deploys +
sends DM.

## Design decision (documented deviation)
Task brief said safety-orange/charcoal/off-white, but RQ's ACTUAL brand —
their logo, shirts, and post graphics — is hot pink/magenta on black
(sampled #FD176F from their own logo file). Per AGENTS.md ("palette must
come from the business's branding"), the site uses **their pink** with
charcoal/off-white. Bold condensed trades identity preserved.

Fonts: Barlow Condensed (700/600, display) + Barlow (400/500/700, body) —
2 families, Google Fonts with display=swap.

## Files
- `index.html` — single page: sticky header, hero (before/after),
  pink fact strip, work gallery, services, 3-step how-it-works, CTA band,
  footer. All asset paths relative (`img/...`) — deploys as subpath
  https://the-cut-co.pages.dev/rq-junk-removal-sydney/.
- `img/*.webp` — 5 optimized WebP (q78, ≤1100w), separate files, no base64.
  width/height attrs on all; lazy-load below fold; hero eager.
- Zip: `~/workspace/instagram/lead-campaign/sites/rq-junk-removal-sydney.zip`
  (index.html at top level + img/)

## Photos — ALL THEIR OWN, none stock/AI
Harvested via hatch-zeitgeist --post-url cover/thumbnail URLs (signed CDN),
downloaded, cropped to remove text-banner/letterbox edges, converted with
ffmpeg (libwebp q78). Visually inspected each.

| file | natural px | source | subject |
|---|---|---|---|
| before-after.webp | 1086x1448 | instagram.com/p/Dc-Osdokpd9/ (2026-09-06, "Before → After" carousel cover) | Before/after yard clear-up, incl. their "NEED IT GONE?" contact banner |
| truck-loaded.webp | 1100x658 (cropped from 3072x4096 top portion to remove text-banner overlay) | instagram.com/p/Dd52ueakru8/ (2026-09-30 carousel cover) | RQ truck loaded with kerbside junk pile |
| kerbside-pile.webp | 640x1136 | instagram.com/reel/DeidvxXyAJL/ (2026-10-15 viral reel cover) | Kerbside furniture pile + loaded cage trailer, "CAN WE DO IT?" |
| gutter-clean.webp | 720x1280 | instagram.com/reel/Des0cehyL9X/ (2026-10-19 reel cover) | Crew member on ladder clearing roof gutters, RQ shirt |
| loading-bag.webp | 720x660 (top+bottom letterbox bars cropped) | instagram.com/reel/DelIKxfycW7/ (2026-10-16 "2 months in" reel cover) | Crew member loading rubbish bag, RQ shirt |

NOT used: p/DcX94QoEvEk/ (logo graphic only, no job photo);
reel/DerAL3_Sws5/ (WWE meme frame — third-party footage, not their work;
excluded to avoid misrepresentation).

## Image-fit audit
- Every frame's `aspect-ratio` matches its image's natural ratio exactly →
  **zero cover-cropping anywhere**; all subjects fully in frame by
  construction (before/after both halves, full truck + pile, full ladder
  worker, full kerbside pile, full crew shot).
- Display widths ≤ source widths (truck-loaded 768px < 1100; portraits
  ≤ 460px < 640–1086) — no upscaling softness.
- Hero (before/after) max 420px wide → 560px tall: within the ≤560px gate.

## Contrast audit (relative luminance, WCAG 2.x — all ≥ 4.5:1)

| Element | Foreground | Background | Ratio |
|---|---|---|---|
| Body/headings on dark | #FFFFFF / #FAF8F4 | #15161A | 18.08 / 17.04 |
| Kickers, H1 accent, badges (dark) | #FD176F (brand pink) | #15161A | 4.76 |
| Button labels, fact-strip text | #15161A | #FD176F | 4.76 |
| Body text (light sections) | #1C1D21 | #FAF8F4 | 15.88 |
| Secondary text (light) | #5B5D64 | #FAF8F4 | 6.20 |
| Kickers/links (light sections) | #C20E58 (brand-deep) | #FAF8F4 / #FFFFFF | 5.66 / 6.00 |
| Secondary text (dark) | #C9CBD1 | #15161A | 11.15 |
| Service-card numbers | #FF5C9D (brand-bright) | #1C1E24 | 5.77 |
| Service-card body | #C9CBD1 | #1C1E24 | 10.27 |
| Footer note | #8E9098 | #0E0F12 | 6.02 |
| Footer IG link | #FD176F | #0E0F12 | 5.05 |

13/13 pairs pass. No text sits on photos. (One fix applied: card numbers
were #FD176F on #1C1E24 = 4.39 → switched to #FF5C9D = 5.77.)

## Responsive gate (headless Chromium, Playwright)
- 390 / 768 / 1440 px: **0 px horizontal overflow**, no element wider than
  viewport, no JS errors. Sections stack cleanly; header CTA hides ≤560px
  (hero CTA directly below); gallery 1-col mobile / 3-col desktop.
- Reveal animations: IntersectionObserver adds `.in`; content visible
  without JS (`.js` gate), `prefers-reduced-motion` disables transitions.

## Facts used — and their sources (NOTHING invented)
- "RQ Junk Removal", "Real Quick & Reliable Junk Removal", "Junk •
  Furniture • Rubbish • Clean Ups", "Western Sydney", "DM us or email:
  rqjunkremoval1@gmail.com" — their IG bio (via hatch-zeitgeist post
  record, 2026-10-23).
- "Servicing Western Sydney & surrounding areas", "make junk removal
  simple, affordable and Real Quick", "Household junk • Furniture •
  General rubbish • Property clean ups & more" — their launch post
  instagram.com/p/DbzuVfDS3cH/ (2026-08-08).
- "DM us for a free quote" — their captions (e.g. p/Dc-Osdokpd9/).
- "Need it gone? DM us or get in touch", phone **0402 575 777** — printed
  on their own before/after graphic (p/Dc-Osdokpd9/, inspected visually).
  (Research JSON said "no phone published" from bio/text; the graphic
  itself publishes it — treated as a business-published fact.)
- Launched August 2026 — launch post 2026-08-08; "2 months in" reel
  2026-10-16.
- "Boys cleaning out them roof gutters" — their reel caption (quoted).
- IG: https://www.instagram.com/rq_junk_removal/ ; DM:
  https://ig.me/m/rq_junk_removal
- NOT claimed: no prices, no ratings/reviews, no hours, no exact suburbs
  beyond "surrounding areas".

## DM draft (~80 words) — for parent to send via instagram-messages-cli
author_id: 17841437696296458

> Hey! Noticed RQ is only a couple of months in and already pulling huge
> engagement on your before/afters — that Western Sydney crowd clearly
> loves the work. One thought: right now anyone Googling "junk removal
> Western Sydney" can't find you — there's no website at all. I mocked up
> a one-page preview site using your own photos: [PREVIEW LINK]. If you
> like the direction, I can build the real thing with a quote form so jobs
> come straight to you. Worth a look?

## Blockers
None. No deploy and no DM sent per task (parent handles both).
