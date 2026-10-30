# Bella & Co Coffee Van — Preview Site Build Notes

Built: 30 Oct 2026 (Devflix outreach night batch). Builder did NOT send, deploy, or contact anyone.
Folder: `bella-co-coffee-van-serpentine/` — `index.html` + `img/*.webp` (5 photos, 295 KB total).

## Fact sources (verified only — nothing invented)

All facts come from the business's own Instagram (@bellandco_coffeevan, author verified as
`bellandco_coffeevan` on every oEmbed response) and the brief's verified-fact list:

- Mobile coffee & cocktail event van; based in Serpentine, VIC (rest area) — bio.
- Available for private events; enquiries by email bellandco24@gmail.com — bio (published email).
- Serves toasties and frappes — post captions (DckYvTxE5i4, DcXqXxTTXNk).
- Sets up at community/sporting events, e.g. Inglewood football oval — post caption (DaWgaEwEzBv).
- "Walk for Bell" rubber duck race fundraiser for the Code 9 Foundation, honouring Bell — post caption
  and poster (DbrckRcTREn). Copy describes it as a fundraiser they ran, NOT as an upcoming event
  (the poster's own date has passed; no future date is claimed anywhere on the site).
- NO own website, NO bio link — enquiries email/DM only. This is the pitch gap.
- Toastie flavours named in copy (chicken/avo/cheese, ham/cheese/tomato, salami/pineapple/cheese,
  ham/cheese) are read directly off the business's own chalkboard photo — not invented.

NOT on the site, deliberately: no prices written into copy, no hours, no street address, no phone,
no reviews, no ratings, no popularity claims. Engagement is modest and nothing claims otherwise.

### Transparency flag — prices visible inside one photo
The toasties chalkboard photo is the business's own published Instagram photo, and the board itself
shows its prices ($12 / $10) as part of the image. No price was transcribed into any site copy, but
the prices are legible in the photo itself. If the batch runner wants zero prices anywhere on the
page, swap `img/toasties.webp` for a different photo before deploying. Same note for the duck-race
poster, which carries its own "$10 per duck" badge and event date as part of the artwork.

### Could not verify / not used
- No cocktail menu, hours, street address, or phone number from any business-published source —
  all omitted. Directory-sourced hours/address were excluded per the brief.
- Follower count (218) and post count (118) were brief-supplied, not re-verified live; neither
  figure appears on the site.

## Photos (5/5 harvested, all business-owned)
Harvested via the public Instagram oEmbed endpoint (iPhone UA per ~/TOOLS.md), CDN thumbnails
downloaded with browser Referer/UA, converted to WebP quality 78 (640px max, the oEmbed ceiling):

| File | Source post | Size | Orientation |
|---|---|---|---|
| hero-van.webp | DaWgaEwEzBv (Inglewood oval) | 640×853, 37 KB | Portrait 3/4 |
| toasties.webp | DckYvTxE5i4 | 640×853, 50 KB | Portrait 3/4 |
| frappes.webp | DcXqXxTTXNk | 640×853, 43 KB | Portrait 3/4 |
| events.webp | DeOCG8_qFmK (view from inside the van) | 640×800, 46 KB | Portrait 4/5 |
| duck-race.webp | DbrckRcTREn (fundraiser poster) | 640×640, 119 KB | Square |

No post failed oEmbed. No stock, AI, or other-business imagery used.

## Design
Own coffee-van identity (not a copy of the aussie-tan reference): warm cream/espresso/terracotta/
sage palette drawn from the van's own colours; DM Serif Display + DM Sans (2 families); solid
colours only — no gradients, no glassmorphism. Scroll-reveal gated behind a `.js` class (content
visible without JS); respects `prefers-reduced-motion`. Width/height attributes on all images;
lazy-load below the fold; hero `fetchpriority="high"`.

## Per-section contrast (WCAG AA, computed from hex values)
- Ink #2E1D12 on cream #FBF6EE: 15.01:1 ✓
- Body #5C4232 on cream: 8.56:1 ✓
- Terracotta #A63A22 on cream (eyebrow, links): 6.01:1 ✓
- White on terracotta #A63A22 (buttons, strip): 6.46:1 ✓
- White/cream on espresso #2E1D12 (CTA band, hero note): 15.01–16.15:1 ✓
- Sage-dark #3F5A38 on cream: 7.15:1 ✓ (palette token, used sparingly)
- Caption cream #FBEEDD on terracotta: 5.65:1 ✓
All pass AA for normal text (≥4.5:1). Text over images appears only as the solid dark hero-note
box over the van's plain lower bodywork — never over faces or busy detail.

## Per-image fit / focal notes (FULL-VIEW rule)
Every frame's aspect ratio matches its photo's natural orientation, so `object-fit: cover`
crops nothing meaningful:
- hero-van (3/4 frame = 3/4 source): two team members at the serving window, faces centred
  ~40% down; `object-position: 50% 40%`, max-height 560px. Faces fully in frame.
- toasties (3/4 = 3/4): full chalkboard visible; `object-position: 50% 46%`.
- frappes (3/4 = 3/4): four drinks mid-frame; `object-position: 50% 52%`.
- events (4/5 = 4/5): crowd viewed from inside the van; `object-position: 50% 52%`, max-height 480px.
- duck-race (1/1 = 1/1): poster shown with `object-fit: contain` on a white field inside a sand
  card — the whole poster, including all text, is visible; nothing cropped.
Each photo was visually inspected (opened and viewed) before placement.

## Responsive check — honest method
I did NOT do a live-browser check: as a subagent I have no live-browser tool, and no Chromium/
Firefox binary exists on this VM to run headless screenshots. What was checked instead (static audit):
- Viewport meta present; `overflow-x: hidden` on body; `img { max-width: 100% }`.
- No fixed pixel widths on any container (grep audit: only `max-width`, padding, font sizes and
  media-query breakpoints use px).
- Grids collapse to a single column below their breakpoints: hero stacks below 900px, menu cards
  stack below 700px, road/fundraiser sections stack below 900px; nav links hide below 680px leaving
  brand + email CTA.
- Hero image capped at 560px tall (desktop), cards ≤520px, content images ≤480px.
- All copy lengths were kept short so no heading or button can overflow a ~390px viewport, but
  this was NOT verified by rendering. The batch runner should do a live visual pass at ~390px /
  ~768px / ~1440px before deploying.

## DM draft (DO NOT SEND — for the batch runner, preview link to be inserted)
> Hi Bella & Co! I spotted your van at the Inglewood oval posts and loved the community feel of it —
> the Walk for Bell duck race especially stood out. I noticed you don't have a website yet, so
> enquiries can only come through email or DM — I put together a quick preview of what a simple
> site for the van could look like, with your coffee, toasties and frappes, where to find you, and
> an easy way for private-event enquiries to reach you: [PREVIEW LINK]. Would something like that
> be useful for the van?
