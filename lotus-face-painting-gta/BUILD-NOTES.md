# BUILD NOTES — Lotus Face Painting GTA preview site

Built 2026-10-23 (night batch) by Devflix. Business: **Lotus Face Painting**,
face painting & glitter art by Shreya Savaj — IG @lotusfacepainting_gta
(author_id 17841403038151938), 1,149 followers, GTA & surrounding areas,
Ontario, Canada. Contact: NOT contacted — build only; parent deploys + sends DM.

## Files
- `index.html` — single page (hero, marquee strip, designs gallery, services,
  Halloween band, booking card, footer). All asset paths relative (`img/...`)
  for merged-subpath deploy at https://the-cut-co.pages.dev/lotus-face-painting-gta/
- `img/*.webp` — 7 optimized images (all ≤1100w, q78). No base64 anywhere.
- Zip: `~/workspace/instagram/lead-campaign/sites/lotus-face-painting-gta.zip`
  (index.html at top level + img/)

## Qualification / gap evidence
- IG bio: "🎨 Face Painting & Glitter Art ✨ 🇨🇦 Serving Canada | Parties &
  Events 🎂 Birthdays • Festivals • Corporate Events 📍 GTA & Surrounding
  Areas 📲DM to Book". **IG website field = http://gmail.com/ (junk
  placeholder — effectively no website).** browser.search found no official
  site. Every booking goes through IG DM ("DM to Book").
- Activity: very active Oct 2026 (posts Oct 17–21), real engagement (5–22
  likes/post at 1,149 followers). Seasonal hook: "HALLOWEEN FACE PAINTING
  BOOKINGS ARE OPEN — limited spots" (post 2026-10-21).

## Photos — all HER work, none stock
Harvested from her own Instagram posts via hatch-zeitgeist signed CDN URLs;
every image visually inspected before use.

| file | natural px → webp | source post | subject |
|---|---|---|---|
| hero.webp | 3216x3456 → 1100x1182 | instagram.com/p/DenE7XnvlGN/ (2026-10-17, 7 likes) | Tiger + rainbow full-face paint, girl eyes closed |
| butterfly.webp | 1448x1931 → 1100x1467 | instagram.com/p/Dee2gfLRr2K/ (18 likes) | Pink/purple butterfly & blossoms |
| spidey.webp | 3072x4096 → 1100x1467 | instagram.com/p/Dej0mB6xJJt/ (8 likes) | Spider-Man half-face, birthday boy |
| rainbow.webp | 1254x1254 → 1100x1100 | instagram.com/p/DeZfNWZxNQW/ (13 likes) | Rainbow, clouds, stars & gems |
| fairy.webp | 2991x2991 → 1100x1100 | instagram.com/p/DeWf9qfxMz8/ (13 likes) | Fairy silhouette + pink flowers |
| bunny.webp | 3569x3963 → 1100x1221 | instagram.com/p/DeAF1lQRD3Z/ (14 likes) | Mom & daughter matching bunny paint |
| halloween.webp | 2272x2272 → 1100x1100 | instagram.com/p/Dexl9aFNGez/ (2026-10-21, 9 likes) | Two adults, skeleton/skull Halloween paint |

The Halloween promo flyer post (instagram.com/p/DexnFR5tLhq/) was inspected
but NOT used as imagery (text-heavy graphic); its published service list was
used as fact source instead (see below).

## Image-fit treatment
- Hero: portrait photo → portrait frame (aspect 4/5, max-height 560px,
  object-position 50% 28%) — full face in frame, mild side crop only.
- Gallery: per-photo frames matched to natural orientation — portraits 4/5,
  squares 1/1, all max-height 340px; per-image object-position keeps every
  painted face fully visible (never cropped). Verified at 390/768/1440.
- width/height attrs on all imgs; below-fold imgs lazy-load; hero
  fetchpriority=high.

## Contrast table (relative-luminance, WCAG 2.x — all ≥ 4.5:1)

| Section / element | Foreground | Background | Ratio | Gate |
|---|---|---|---|---|
| Body text | #2B2320 | #FFF8F1 | 14.63 | pass |
| Secondary text | #6F5B52 | #FFF8F1 | 6.06 | pass |
| Kicker | #C02A44 | #FFF8F1 | 5.46 | pass |
| Primary button label | #FFFFFF | #C02A44 | 5.74 | pass |
| Ghost button | #C02A44 | #FFF8F1 | 5.46 | pass |
| Button hover | #FFFFFF | #2B2320 | 15.40 | pass |
| Marquee strip text | #FFF8F1 | #0B5B5A | 7.50 | pass |
| Card text / captions | #2B2320 / #6F5B52 | #FFFFFF | 15.40 / 6.39 | pass |
| Card "See the post" link | #0B5B5A | #FFFFFF | 7.90 | pass |
| Service card number | #E4576B (decorative only, no meaning) | #FFF8F1 | n/a | decorative |
| Badge text | #2B2320 | #FFC94D | 10.48 | pass |
| Halloween band text | #FFFFFF / #FFE9EC | #A81F38 | 7.20 / 6.61 | pass |
| Halloween button | #A81F38 | #FFFFFF | 7.20 | pass |
| Footer text | #FFF8F1 | #103B3A | 11.67 | pass |
| Footer link | #FFD9A8 | #103B3A | 9.21 | pass |
| Nav links | #2B2320 | #FFF8F1 | 14.63 | pass |

15/15 meaningful pairs pass 4.5:1 (lowest 5.46). No text sits on photos
(the "by Shreya Savaj" tag sits on the photo — white text on the teal pill,
pill #0B5B5A vs #FFFFFF = 7.50, pass).

## Responsive verification (headless Chromium, real screenshots)
- 390px: no horizontal overflow (document scrollWidth == viewport), header
  wraps nav cleanly to two lines, hero stacks photo-first, gallery single
  column, all faces fully in frame, no overlap/clipping.
- 768px: header single line, hero stacks, gallery 2-col, services 3+2 —
  no overflow, no clipping.
- 1440px: split hero (text + photo), gallery 3-col, no overflow.
- Bugs found & fixed during verification: (1) `.hrow{padding:16px 0}`
  shorthand wiped the `.wrap` horizontal padding → nav flush to viewport
  edge; (2) same shorthand-override pattern on `.hero`/`.designs`/`.book`
  (`padding:72px 0` / `padding:52px 0 64px`) removed side gutters;
  (3) grid blowout — `1fr` tracks resolve `minmax(auto,1fr)` so the hero
  figure and Halloween image (grid items wrapping large intrinsic-size
  photos) forced their columns to 430/440px at 390px viewport; fixed with
  `min-width:0` on both grid items. Re-verified clean after each fix.

## Facts used — and their sources (NOTHING invented)
- Name "Lotus Face Painting", artist "Shreya Savaj" (profile name "Shreya
  savaj"), handle @lotusfacepainting_gta, 1,149 followers — IG profile via
  API.
- "Face Painting & Glitter Art | Serving Canada | Parties & Events |
  Birthdays, Festivals, Corporate Events | GTA & Surrounding Areas | DM to
  Book" — her IG bio, verbatim.
- Service menu — her own Halloween flyer post (instagram.com/p/DexnFR5tLhq/,
  2026-10-21): "Single Face (simple design)", "Special Design (more
  detail)", "Premium / Full Face (intricate & detailed)", "Glitter Add-On",
  "Group bookings & larger events"; plus "Safe & Non-Toxic Face Paints",
  "Clean & Hygienic", "Fun & Creative Designs", "Suitable for All Ages".
- "Brampton • Mississauga • Toronto • GTA" — her Halloween caption
  (2026-10-21 post).
- "Halloween face painting bookings are open — limited spots" — her
  2026-10-21 caption, paraphrased.
- Design captions — the actual artwork in her photos + her own captions
  (tiger/rainbow, butterfly, Spidey birthday boy, rainbow+gems, fairy,
  mom & daughter bunnies, Halloween skeletons).
- DM CTA: https://ig.me/m/lotusfacepainting_gta; profile link
  https://www.instagram.com/lotusfacepainting_gta/.
- NOT claimed: no prices (none published), no packages beyond her list, no
  hours, no phone/email/address (none published), no reviews/ratings.

## Design decisions (AGENTS.md standard)
- Playful party-artist identity, distinct from prior builds: Baloo 2
  (rounded friendly display) + Nunito (clean body), cream/coral/teal/sun
  palette; solid colours only — no gradients, no glass, no floating cards.
- Photo-led: split hero with sun blob + rotated tag, teal marquee strip,
  6-tile designs gallery, service cards, deep-coral Halloween band, booking
  card, dark-teal footer.
- Restrained motion: IntersectionObserver reveal behind `.js` (content fully
  visible without JS), marquee animation, `prefers-reduced-motion` respected;
  900/560px breakpoints; overflow-x hidden.

## DM DRAFT (not sent — sender Devflix @devfl_ix, via Instagram DM to author_id 17841403038151938)
> Hi Shreya — your tiger-and-rainbow design stopped my scroll, and the mom &
> daughter bunny painting is such a sweet idea for family events. Real
> portfolio-worthy work.
>
> Right now it all lives only on Instagram — there's no website where a
> parent in Brampton or Mississauga planning a birthday can see your designs
> and service options in one place. I built you a preview page with your own
> photos to show what that could look like: [PREVIEW LINK]
>
> Want me to keep it live for you, or would you change anything first? — Devflix

(~92 words. Genuine observations — the tiger/rainbow design and the mom &
daughter bunny post, both verified from her grid; gap — no website, IG
website field is a junk placeholder, bookings DM-only; one low-pressure
question.)
