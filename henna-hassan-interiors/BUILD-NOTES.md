# BUILD NOTES — henna-hassan-interiors
Lead: **Henna Hassan — Interior Architect & Designer** (@hennahassanofficial), Lahore, Pakistan, ~11.8K followers.
Preview URL (after deploy): https://the-cut-co.pages.dev/henna-hassan-interiors/

## Photos — 6/6 downloaded and converted (0 failures, no stock/AI substitutes)
Source: verified Instagram CDN thumbnails from `batch-morning-23oct-PKGULF.json` (author_name verified = hennahassanofficial).
Downloaded 2026-10-23 with iPhone UA + Instagram Referer; all verified as real JPEGs via `file`. Converted with PIL to WebP quality 78, at native 640px width (no upscaling).

| File | Source post | Native | Contents (verified by eye) |
|---|---|---|---|
| photo-1.webp | https://www.instagram.com/p/DejRMXFgI8S/ | 640×800 | Cream silk curtains with teal velvet equestrian horse-bit tieback, gold beaded tassel finial |
| photo-2.webp | https://www.instagram.com/p/DebwjlBCM_O/ | 640×800 | Dachshund-embroidered navy velvet cushions + paw-print tieback bands on ikat sofa |
| photo-3.webp | https://www.instagram.com/p/Dd6VoLxDHU1/ | 640×800 | "The Master Bedroom Edit": grey silk curtains, wave heading, chess trim, rose-embroidered cushions |
| photo-4.webp | https://www.instagram.com/p/Dd30TW5CHek/ | 640×800 | Close-up: embroidered floral tieback (magenta/cream roses) on grey wave-heading silk curtain |
| photo-5.webp | https://www.instagram.com/p/DdgiYSPiBis/ | 640×800 | Terracotta silk curtain with ombré tassel tieback, embroidered sheer |
| photo-6.webp | https://www.instagram.com/p/DcGTpRNgcH_/ | 640×1138 | "Inside the details — a full home project, Bahria Town, Lahore": blush curtains, balcony chair |

Note: photos carry the studio's own logo watermark / on-image captions — kept as-is (their own branding).

## Contrast table (computed, WCAG 2.1)
Palette: cream #FBF6ED · cream-2 #F3EADC · ink #2C2620 · muted #5D544A · terracotta #A8441A · terra-soft #E9B48B · line #E0D3BC.

| Foreground → Background | Ratio | Need | Result |
|---|---|---|---|
| #2C2620 (body/ink) on #FBF6ED (cream) | 13.88 | 4.5 | PASS |
| #5D544A (muted text) on #FBF6ED | 6.89 | 4.5 | PASS |
| #A8441A (terracotta: eyebrow, links, buttons) on #FBF6ED | 5.56 | 4.5 | PASS |
| #FBF6ED (white button label) on #A8441A (terracotta button) | 5.56 | 4.5 | PASS |
| #2C2620 (ink) on #F3EADC (band/project bg) | 12.53 | 4.5 | PASS |
| #FBF6ED (cream text) on #2C2620 (philosophy section) | 13.88 | 4.5 | PASS |
| #E9B48B (terra-soft eyebrow/attr) on #2C2620 | 8.09 | 4.5 | PASS |
| Fraunces headings (ink/terracotta) — large text ≥3.0 needed | ≥5.56 | 3.0 | PASS |

ALL rows PASS. All text over images sits in figcaption/cards, never over imagery.

## Image-fit audit (FULL VIEW — hard gate)
- Every image is displayed at or below native 640px width, in a frame matching its natural orientation (all portrait). Nothing is upscaled.
- Hero (photo-1): `height:520px; width:auto` — full subject, no crop, ≤560px tall desktop gate met.
- Collections (photo-2/3/4/5): natural 4:5 ratio frames, 440px display height, `object-fit:contain` — full view, no cut.
- Project (photo-6): `height:480px; width:auto` — full view, ≤480px content gate met.
- All imgs carry explicit `width`/`height` attributes (aspect-ratio known, no layout shift); below-fold images `loading="lazy"`; hero `fetchpriority="high"`.
- No cover-cropping, no stretch/distort, no per-image object-position needed since nothing is cropped.

## Responsive check — 390 / 768 / 1440px
Headless Chromium not installed on this VM (`which chromium chromium-browser google-chrome` → nothing), so no live screenshot verification. Careful CSS audit done instead:
- Single breakpoint at 860px: hero grid → 1 column (photo max 330px wide), collections → 1 column, project/order grids → 1 column, nav hidden at ≤860px (header keeps brand + DM CTA; all nav targets remain reachable by scroll — documented caveat).
- No fixed pixel widths on text containers; `.wrap` max 1160 + side padding; all images `max-width:100%`; no absolute-positioned overlays; no horizontal-scroll risk identified at 390px (longest unbreakable strings are the IG URL in alt/title — not rendered).
- Reveal animations gated behind `html.js` (content fully visible without JS); `prefers-reduced-motion: reduce` disables them.
- Caveat: audit is by code review only, not a live browser render. A parent-side browser check at 390/768/1440 before DM send is recommended.

## Fact sources (everything on the page is from the JSON; nothing invented)
- Bio line "Transforming your spaces with hand crafted designer window dressings and bespoke interior collections. Made with love in Pakistan!" → lede, band, footer, philosophy attr.
- Products: silk curtains w/ signature wave heading, embroidered floral tiebacks, tasselled cords, Roman blinds, 'Raptor' kids bed set, 'Tile Collection' tea-time cushions, dachshund cushions, equestrian-motif tiebacks → collections grid + "More from the studio".
- Bahria Town project (reel 2026-06-07; 1,918 likes / 144 comments): bespoke curtain sets, truck-motif cushions, Roman blinds, "simple elegance without excessive drapery" → project section (the like/comment counts are from engagement_facts).
- "beautiful windows don't just decorate a space, they transform how it feels" → hero H1 + philosophy quote.
- "DM to place an order"; "Site visits back to back" → order section + CTAs.
- CTA links to the business's own Instagram: https://www.instagram.com/hennahassanofficial/
- NOT included (unverified): no prices, reviews, ratings, hours, phone, email — none in the JSON.

## Files
- `index.html` (self-contained; relative `assets/` paths; Google Fonts Fraunces + Inter, display=swap)
- `assets/photo-1..6.webp` (39–115 KB each; total ~412 KB)
- Zip for merged-subpath deploy: `~/workspace/instagram/lead-campaign/sites/henna-hassan-interiors.zip` (index.html at zip root)

## DM draft (for parent)
> Hi Henna — I came across your page through the Bahria Town full-home project; the blush silk curtains and that line "beautiful windows don't just decorate a space, they transform how it feels" genuinely stood out.
>
> Right now everything runs through DMs, so I put together a quick concept site for your work — your collections, the Bahria Town project, and a "DM to place an order" button, all in one place: https://the-cut-co.pages.dev/henna-hassan-interiors/
>
> No cost, no catch — just wanted you to see how your work could look with a proper home online. Would you be open to something like this?
