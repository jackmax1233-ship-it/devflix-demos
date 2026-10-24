# In a Flurry Snow Removal — preview site build notes

Business: **In a Flurry Snow Removal** (a division of Nove Landscaping Inc) — Woodbridge, Ontario, Canada (GTA)
Instagram: **@in_a_flurry_snowremoval** · author_id `17841432401038399` · 860 followers · snow removal service, quotes/bookings via Instagram DM only, no website at all.
Deploy target (relative paths only): `https://the-cut-co.pages.dev/in-a-flurry-snow-removal/`

## Photos (5 — all the business's own public Instagram posts, harvested via oEmbed)

| File | Subject | Source post | Natural dims (shipped) | Frame | Fit / focal |
|---|---|---|---|---|---|
| img/hero-seasonal.webp | Their seasonal-plans promo graphic: plow truck clearing a driveway at night, worker with red Honda snow blower, worker shoveling front steps, service-area list | instagram.com/p/Des5s_YtwAq/ (2026-10-19 booking announcement) | 640×764 (~5:6) | portrait, `object-fit:contain`, max-height 560px desktop / 70vh mobile | full view, zero crop — all text/logo in frame |
| img/service-driveway.webp | Their "SNOW REMOVAL" early-bird promo graphic: cleared residential driveway at night | instagram.com/p/Dc5tua7Bddi/ (2026-09-05 early bird rates) | 640×853 (3:4) | 3:4 portrait, contain | full view, zero crop |
| img/early-bird.webp | Their "EARLY BIRD SNOW REMOVAL RATES" graphic: suburban home, cleared driveway | instagram.com/p/Dc2Qwt9NkXv/ (2026-09-03 seasonal promo) | 640×853 (3:4) | 3:4 portrait, contain | full view, zero crop |
| img/townhouse-clear.webp | Cleared townhouse driveway at night with their logo overlaid | instagram.com/p/DczhaAgt2gB/ (2026-09-02 service promo) | 640×853 (3:4) | 3:4 portrait, contain | full view, zero crop |
| img/home-clear.webp | Cleared residential driveway, home with garage, their logo | instagram.com/p/Dcw4qOXNOMd/ (2026-09-01 service promo) | 640×853 (3:4) | 3:4 portrait, contain | full view, zero crop |

- WebP q78 via ffmpeg, ≤640w (≤1100w requirement met — source oEmbed thumbnails are 640px; full-res versions unavailable without a login session).
- No stock/AI photos anywhere. No base64. Hero `fetchpriority="high"` + eager; all others `loading="lazy"` + `decoding="async"`. `width`/`height` attrs on every `<img>`.
- Frames match each photo's natural orientation (all portrait); `object-fit: contain` in matching-ratio frames = zero cropping (per 21 Oct hard gate — full view wins).

## Palette & type

- **Palette:** deep navy `#0B1B33` (bg) · snow `#F3F7FB` (light bg) · ice `#8FD3FF` (accent text/CTA ghost on navy) · ice-pale `#CDE8FF` (chips/icons bg) · ink `#13253E` (body text on snow) · muted `#4A6079` (secondary text on snow) · on-navy muted `#9FB9D4` · button blue `#1668AC`.
- **Type:** Archivo Black (display — bold winter grotesque) + Inter (body), 2 Google Fonts families with `display=swap`. Snowflake motif in custom inline SVG; subtle CSS falling snow in hero only (disabled under `prefers-reduced-motion`). No gradients/glassmorphism AI look; identity is a bold deep-navy winter night.

## Contrast audit (computed WCAG ratios, python luminance)

| Pair | Ratio | Requirement | Pass |
|---|---|---|---|
| #FFFFFF on #0B1B33 (hero H1/nav/footer) | 17.23 | ≥4.5 | PASS |
| #8FD3FF on #0B1B33 (kicker/accent/eyebrow on dark, ghost button) | 10.61 | ≥4.5 | PASS |
| #9FB9D4 on #0B1B33 (lede/secondary on dark) | 8.50 | ≥4.5 | PASS |
| #13253E on #F3F7FB (body text on light) | 14.32 | ≥4.5 | PASS |
| #4A6079 on #F3F7FB (card body text) | 6.02 | ≥4.5 | PASS |
| #FFFFFF on #1668AC (primary buttons) | 5.82 | ≥4.5 | PASS |
| #0B1B33 on #CDE8FF (area chips, icon tiles) | 13.61 | ≥4.5 | PASS |
| #1668AC on #F3F7FB (eyebrow "what we do") | 5.82 | ≥4.5 | PASS |

Text over images: hero image sits beside text, not behind it — no overlay text on photos. All pairs PASS AA.

## Responsive verification (headless Chromium, real renders)

- 390px / 768px / 1440px: **0px horizontal overflow** at every width; no clipped text/buttons/images; nav usable on mobile (scrollable link row).
- Hero image height: 417px (390) / 480px (768) / 560px (1440) — within the ≤560px desktop / 70vh mobile caps.
- Service cards: 200px (desktop, 3-col) — within ≤340px; stack 2-col at 768, 1-col at 390.
- Gallery: 4-col → 2-col → 2-col, full-view 3:4 frames at every width.
- All 5 images load with `naturalWidth > 0`; zero page errors (only a sandbox network error for Google Fonts, which loads fine on a live deploy).
- Reveal animation gated behind `.js` (content fully visible with JS disabled) and honours `prefers-reduced-motion`; verified 20/20 `.reveal` elements reach visible state on real scroll.

## Fact sources (nothing invented)

- Name/division: bio via `instagram-cli post` — "A Division of Nove Landscaping Inc"; author name "❄️In a Flurry Snow Removal Service".
- Tagline headline: their bio — "When it snows we'll be there 'in a flurry!'".
- Services (6 cards): exact service list from their 2026-10-19 caption — Residential & Commercial Snow Removal; Snow Plowing & Snow Blowing; Walkways, Front Steps & Entrances; Full-Service Unlimited Seasonal Plans; Same-Day Service Guarantee; "Instant Response & Reliable Service".
- Service areas (9 chips): exact list from the same caption — Woodbridge, Maple, Kleinburg, Bolton, Nobleton, Thornhill, Richmond Hill, North York, East Brampton.
- Season hooks: "NOW BOOKING FOR THE 2026–2027 WINTER SEASON", "Early bird rates now available!", "LIMITED SPOTS AVAILABLE", "MESSAGE US TODAY FOR A FREE, NO-OBLIGATION QUOTE" — all from their captions.
- Location: Woodbridge, Ontario (post location tag + research). No phone number published anywhere — contact is Instagram DM only (`https://ig.me/m/in_a_flurry_snowremoval`), no contact form invented.
- NOT on the site: prices/rates (they advertise "early bird rates" with no numbers — none invented), reviews/ratings/testimonials, phone, email, hours, crew size. Caption "Real clearings from our own crew" refers to their own photos.

## DM draft (for the outreach batch — do NOT send from here)

author_id: `17841432401038399` · channel: Instagram DM.

> Hi! I came across In a Flurry's snow-removal posts — that plow truck clearing a driveway at night and the Honda snow blower shots really show the work, and I like that you're already booking the 2026–27 season around Woodbridge. One thing stood out: anyone Googling snow removal in the GTA can't find you — there's no website, just your Instagram. A simple one-pager with your services, areas and a DM booking button would turn those winter searches into seasonal contracts. I mocked one up from your own photos: [PREVIEW LINK] — free to use if you like it. Would something like that be useful for the season? — Devflix

(~85 words; genuine observation about their equipment/posts, why a site wins seasonal contracts, [PREVIEW LINK] placeholder, one low-pressure question, signed — Devflix.)

## Notes / blockers

- No blockers. One honest caveat: the 5 photos are the business's own *branded promo graphics* (their full recent post set is graphics, not raw job photos) — shown full-view so all their own text stays legible; no text of ours duplicates theirs.
- Not deployed (per task); not DM'd (per task).
