# BUILD-NOTES — Kererū Farm Stay NZ preview site
Built: 2026-10-23 ~01:20 PKT · Builder: subagent (no live browser) · Batch: night-22oct-AUNZ
Research source: `~/workspace/instagram/lead-campaign/research/batch-night-22oct-AUNZ.json` (qualified[3], rank 4)

## Business (verified 2026-10-23 — facts used, nothing invented)
- Name: Kererū Farm Stay · IG @kereru_farm_stay_nz · author_id 17841478383222032 · near Dunedin, Otago, NZ · 540 followers
- Bio (published): super pet-friendly rural accommodation, sea views, 20 hectares private forest trails, 15 mins drive to Dunedin, "Stay & Train with your dog" niche
- Units: Kererū Cottage + Kererū Guesthouse (Airbnb listing names)
- Booking: Airbnb only — airbnb.com/h/cottagekereru, airbnb.com/h/kereruguesthouse (published bio links; no official site)
- Partner: All Sorts Dog Training (bio link allsortsdogtraining.co.nz; tagged @allsorts_dogtraining_nz in a post)
- Published post facts used: Eywa (German Shepherd, from Bay of Plenty, stayed at Kererū Cottage, log fire); Solo (decompression stay, "peaceful rural retreat"); Louis & Tato (Golden Retrievers, trails + wood fire); Booms & Marlin (with Mum and baby Freda, from North Island); multi-day discount — book 7 nights at Kererū Cottage, save 20%; Guesthouse views from both bedrooms; "wintry scenes from every window"; daffodils brighten the Guesthouse; "Autumn is a special time at Kererū Farm… book a weekend break"
- ABSENT (not published — never invented): phone, street address, room/bed details, exact prices beyond the 20%-off-7-nights offer, reviews/ratings, hours

## Design
- Identity: rustic NZ farm stay — wool cream #FAF5EA, eucalyptus deep #2E4633, sage #43604A, rust #A44E28, gold #E4B04B, charcoal ink #222B1E
- Fonts: Fraunces (display serif) + Karla (body sans), Google Fonts display=swap — ≤2 families
- No generic AI look: flat hand-drawn SVG hero scene (hills, cottage, sea band, dog), leaf logo mark, no gradients/glassmorphism
- Motion: IntersectionObserver reveal gated behind `.js` (content fully visible without JS), `prefers-reduced-motion` disables all animation

## Photos — BLOCKED in this environment (documented per task)
- Instagram oEmbed API WORKS: all 8 post URLs verified live 2026-10-23, real thumbnail URLs + full captions captured
- Image BYTES unreachable: scontent CDN returns HTTP 403 from this environment (direct curl + iPhone UA), images.weserv.nl proxy returns 404
- Decision: shipped 11 `<!-- PHOTO-SLOT -->` markers mapping to 8 verified IG posts + visible styled placeholders (no stock/AI photos — AGENTS.md forbids AI imagery replacing real business photos). Full carousel images have DIFFERENT frames than oEmbed thumbnails — harvester should pull from the post pages.
- Slots → post URLs (all https://www.instagram.com/p/<id>/, harvested via `https://www.instagram.com/api/v1/oembed/?url=<post>`):
  1. photo-hero-winter-views — DbnLvKmDs2G — "Enjoy the wintry scenes from every window" (hero SVG replaced by this image)
  2. photo-cottage-eywa — Dd-s2SzDoPk — Eywa the German Shepherd at Kererū Cottage
  3. photo-guesthouse-views — DYiMLB8E5Z- — "views from both bedrooms of Kererū Guesthouse"
  4. photo-solo-decompression — DbFegm3jm19 — "Solo loved his decompression stay at Kererū Cottage"
  5. photo-story-eywa — Dd-s2SzDoPk — (use a different carousel frame than slot 2)
  6. photo-story-louis-tato — DaUrouBFjvQ — "Louis and Tato… exploring our trails… wood fire"
  7. photo-story-booms-marlin — DahA3tODuWz — "Booms & Marlin are here with their Mum and baby Freda"
  8. photo-story-daffodils — DckfMOOuL1N — daffodils brightening the Guesthouse (Daffodil Day)
  9. photo-season-winter — DbnLvKmDs2G — (different carousel frame than slot 1)
  10. photo-season-trails — DY0Fs8XBweo — multi-day discount post image
  11. photo-season-autumn — DYiMLB8E5Z- — (different carousel frame than slot 3)
- WebP target on harvest: ≤1100w, q78, width/height attrs, lazy-load below fold, full-subject (no cover-crop of animals), relative `img/` paths

## Contrast audit (WCAG AA, computed relative luminance — all PASS ≥ 4.5)
| Text | Background | Ratio | Verdict |
|---|---|---|---|
| Ink #222B1E | Cream #FAF5EA | 13.48 | PASS |
| Deep #2E4633 (text, buttons) | Cream | 9.47 | PASS |
| Rust #A44E28 (eyebrow) | Cream | 5.22 | PASS |
| Sage #43604A (muted text) | Cream | 6.42 | PASS |
| Cream #FAF5EA (button text) | Deep #2E4633 | 9.47 | PASS |
| Gold #E4B04B (eyebrow, footer links) | Deep band / Footer #1E2A20 | 5.20 / 7.54 | PASS |
| Rust tag #A44E28 | Tint #F6E9DD | 4.76 | PASS |
| Deep #2E4633 | Chip #E9F0E4 | 8.85 | PASS |
| Cream body | Footer #1E2A20 | 13.72 | PASS |
| Footer muted #C9BFA8 | Footer #1E2A20 | 8.17 | PASS |
| Placeholder deep text | Slot bg #E9F0E4 | 8.85 | PASS |

## Responsive audit (structural — NO live browser in this build)
- Mobile-first; all layouts use CSS grid/flex + media queries (no fixed px widths anywhere — verified by grep); fluid clamp() type; `max-width:100%` on all media
- Hero art capped 560px, card frames capped 340px (full-view wins once real photos land)
- NOT visually verified at 390/768/1440 in a real browser — parent's live-browser pass required before DM (photos also pending harvest)

## DM draft (Instagram, to author_id 17841478383222032)
> Hi! I came across Kererū Farm Stay and loved the 'stay & train with your dog' idea — Eywa's week at the cottage and Solo's decompression stay are such lovely stories, but right now they only live on Instagram.
>
> I noticed bookings run through Airbnb only, so Google can't find you directly. I put together a small website concept for the farm — the cottage and guesthouse, your forest trails and sea views, and direct booking buttons: [PREVIEW LINK]
>
> Would something like this be useful, especially with the 20% multi-day offer? No pressure at all — just wanted you to see it.

## Deliverables
- `index.html` + `img/favicon.svg` (+ `img/` awaits harvested photos)
- Zip: `~/workspace/instagram/lead-campaign/sites/kereru-farm-stay-nz.zip` — Cloudflare Pages (deploys as https://the-cut-co.pages.dev/kereru-farm-stay-nz/; relative asset paths only)
- Do NOT deploy / do NOT send DMs (per task)
