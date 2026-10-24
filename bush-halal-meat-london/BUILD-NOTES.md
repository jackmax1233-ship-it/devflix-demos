# BUILD NOTES — Bush Halal Meat (bush-halal-meat-london)
**Date:** 23 Oct 2026 · **Batch:** morning-23oct-UKIE · **Final URL:** https://the-cut-co.pages.dev/bush-halal-meat-london/

## Fact sources (nothing invented)
All facts come from `~/workspace/instagram/lead-campaign/research/batch-morning-23oct-UKIE.json` (lead `ig_handle: bush_halal_meat`):
- **Business:** Bush Halal Meat, halal butcher, Shepherd's Bush, London UK · **1,818 followers**
- **Address:** 53 East Side, Shepherd's Bush Market, London W12 8DG — from Food Hygiene Ratings directory entry (as recorded in the research JSON). Directions hint "come through the Goldhawk Road station side" is paraphrased from a commenter's direction to the shop ("shepherd bush market W12 8DG come threw the Goldhalk station side").
- **Phone:** 02087435208 from IG bio (published) → tap-to-call `tel:02087435208` used throughout.
- **Gap:** No website at all; IG bio has zero links; orders phone/in-person only.
- **Published deals (shown on site, attributed as "as posted on Instagram"):**
  - "2kg lamb neck £20" — reel 20 Oct 2026 (93 likes, 11 comments)
  - "£20 tray GOAT BACK CHOPS" — reel 1 Oct 2026 (189 likes, 40 comments)
  - A third £20 tray reel ("New tray £20", beef chunks) is used as a third deal card — the photo's own on-image text says "New tray £20"; no product name beyond what's visible.
- **Engagement facts reused honestly:** 1 Oct reel "189 likes, 40 comments"; 15 Sep 2026 reel "1,627 likes, 222 comments" (viral reach); commenter buying-intent behaviour (price questions, cut requests, directions) is described generically, not quoted as fake reviews. Follower count rendered as "1,800+" in hero proof strip (rounded, not inflated).
- **Tomahawk steaks:** shown without any price (the business never published one) — captioned "Call for today's price."
- **No invented content:** no hours, no delivery claims, no ratings, no extra prices, no invented products/services. Footer carries a "preview concept, not the official site" disclaimer.

## Photos
- **Count: 8/8 downloaded, 0 failed.** All from the research JSON `photo_urls` (oEmbed-verified Instagram CDN thumbnails), fetched with iPhone UA + instagram.com referer — all HTTP 200 on first attempt.
- Converted with PIL to WebP quality 78, kept at native **640×1138** (all are portrait 9:16 reel thumbnails), displayed at/below native size. `cwebp` was not installed on this VM; PIL output verified as valid VP8 WebP via `file`.
- Content audit (every photo inspected):
  - photo-1: butcher holding "2kg lamb neck £20" tray → deal card 1
  - photo-2: butcher at the stall, hanging poultry, Bush-stickered trays → hero
  - photo-3: "20 pound trays … star of the show" (goat) → deal card 2
  - photo-4: "New tray £20" beef tray → deal card 3
  - photo-5: butcher holding a £20 note → counter gallery
  - photo-6: "Tomahawk is back" → counter gallery
  - photo-7: "GOAT BACK CHOPS New tray £20" → counter gallery
  - photo-8: "TOMAHAWK STEAKS" close-up → counter gallery
- Each photo used exactly once. Saved to `assets/` with relative paths; **no base64**, no stock/AI substitution.

## Design
Traditional butcher, premium craft. Palette: oxblood `#460D18` / ink `#2E0A12` + warm cream `#FAF3E6` + brass `#C9973A` accents. Fonts: Playfair Display (display serif) + Inter (body), Google Fonts `display=swap`. Editorial asymmetric layout, photo-led. No gradients, no glassmorphism, no floating cards.

### Contrast table (WCAG AA — ALL PASS)
Computed in Python (relative luminance), including effective values for opacity-blended text:

| Text / element | Foreground | Background | Ratio | Needed | Result |
|---|---|---|---|---|---|
| Body text (cream sections) | #2E0A12 ink | #FAF3E6 cream | 16.29 | 4.5 | PASS |
| Secondary text (.kicker, muted) | #6E3B2A | #FAF3E6 cream | 8.19 | 4.5 | PASS |
| Hero/headline text | #FAF3E6 cream | #460D18 oxblood | 14.29 | 4.5 | PASS |
| Hero lede (92% opacity, blended) | effective | #460D18 | 12.25 | 4.5 | PASS |
| Hero fine print (72% opacity, blended) | effective | #460D18 | 7.89 | 4.5 | PASS |
| Eyebrow (brass-soft #E4C57C) | on oxblood | #460D18 | ~12.4 | 4.5 | PASS |
| Brass accent text on oxblood | #C9973A | #460D18 | 5.99 | 4.5 | PASS |
| Call button (brass bg, ink text) | #2E0A12 | #C9973A brass | 6.82 | 4.5 | PASS |
| Deal price (oxblood on white) | #460D18 | #FFFFFF | 15.78 | 4.5 | PASS |
| Deal-note link (oxblood on cream) | #460D18 | #FAF3E6 | 14.29 | 4.5 | PASS |
| Counter captions (85% opacity, blended) | effective | #2E0A12 ink | 11.85 | 4.5 | PASS |
| Footer disclaimer (60% opacity, 12.5px) | effective | #2E0A12 ink | 6.37 | 4.5 | PASS |
| Photo tag (cream on ink) | #FAF3E6 | #2E0A12 | 16.29 | 4.5 | PASS |

### Image-fit audit (ALL PASS)
- All 8 images are portrait 640×1138; every container matches that orientation — **full view, nothing cut** (faces, trays, stickers, on-image deal text all fully visible).
- No `object-fit: cover` anywhere; images sized by fixed `height` + `width:auto` at natural aspect ratio (never stretched/distorted). `object-position` not needed — no cropping occurs.
- Height caps respected: hero 540px desktop (≤560) / 400px mobile; deal cards 420–440px; gallery 300–360px (all ≤480). Displayed width always below 640px native.
- Every `<img>` carries `width="640" height="1138"`, descriptive `alt`, and `loading="lazy"` below the fold (hero uses `fetchpriority="high"`).

### Responsive audit — 390 / 768 / 1440px (manual CSS audit; no headless Chromium on this VM)
- **390px:** single-column everywhere; nav links hidden, brand + call button remain (brand tagline hidden to fit); CTA buttons full-width; images 300–400px tall, centred, no overflow. Address card padding reduced. No horizontal overflow sources (no fixed widths, no negative margins).
- **768px:** hero stacks (text over photo); deals single column (max 560px); gallery 2-up; visit section stacks. All images centred within columns.
- **1440px:** hero two-column (1.05fr/0.95fr); deals 3-up; gallery 4-up; visit 2-up. Hero image 304px wide in a 511px column — asymmetric editorial, intentional.
- Reveal animations are gated behind `.js` (content fully visible without JS) and disabled under `prefers-reduced-motion`.

## Deliverables
- `index.html` — single self-contained page, relative paths only
- `assets/photo-1.webp … photo-8.webp` — WebP q78, 640×1138
- ZIP: `~/workspace/instagram/lead-campaign/sites/bush-halal-meat-london.zip` (index.html at zip root)

## DM draft (for parent's outreach batch)
> Hi — came across your £20 tray reels (the goat back chops ones) and noticed customers are already trying to buy through your comments and DMs — asking prices, requesting cuts, asking for directions. Right now all of that demand funnels into phone-only, which is fine until a busy Saturday buries it. We mocked up what a simple site for Bush Halal Meat could look like — your deals, your prices, one-tap call and directions: https://the-cut-co.pages.dev/bush-halal-meat-london/ — worth a look? Happy to tweak anything or bin it if it's not your thing.

## Caveats
- Photos are Instagram reel thumbnails (640px max) with burned-in deal text/stickers — they read as authentic social proof, but resolution caps how large they can be displayed; all sizing respects that.
- Opacity-blended text was contrast-verified computationally, not in a live browser (no headless Chromium on this VM).
