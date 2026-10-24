# BUILD NOTES — interiors-nusrat-jamil (preview site for Devflix outreach)
Built: 23 Oct 2026 (morning batch) · Slug: `interiors-nusrat-jamil` · Preview URL: https://the-cut-co.pages.dev/interiors-nusrat-jamil/
Lead: **Interiors by Nusrat Jamil** — @interiorbynj_, Lahore Pakistan, interior design studio, ~12.9K followers.

## 1. Photo audit — 8/8 downloaded, ALL REAL (0 failed, 0 substituted)
Source: verified Instagram CDN thumbnail URLs from `~/workspace/instagram/lead-campaign/research/batch-morning-23oct-PKGULF.json` (all with `author_name_verified: interiorbynj_`). Downloaded with iPhone UA + Instagram Referer. All 8 verified as real JPEGs via `file`. Converted with PIL to WebP q78 at native 640px width (displayed at/below native everywhere — no upscaling). Original `.jpg` downloads removed; only `.webp` ships.

| File | Post | Native | Subject (seen) | Site use |
|---|---|---|---|---|
| atrium-open-house.webp | p/DdTzcxojYyz/ | 640×800 | Double-height atrium, marble art panel, "OPEN HOUSE COMING SOON" overlay | Hero |
| digital-print-curtains.webp | p/Dc_AZoTEkN0/ | 640×853 | Beige/bronze digital-print curtains, textured wall, lamp | Expertise card |
| sheer-fringe-curtains.webp | p/Dci415yDdWM/ | 640×853 | Sheer curtains, hand fringe border | Expertise card |
| statement-corner-sofa.webp | p/DcgNDsptC0Z/ | 640×853 | Curved emerald sofa, sheers, amber bead installation | Expertise card |
| wall-art-installation.webp | p/DeylJPxtw9s/ | 640×853 | Team installing blue/gold circular wall art | Craft section |
| metal-leaf-wall-art.webp | p/DYm7wUgjQob/ | 640×853 | Silver metallic leaf wall sculptures | Expertise card |
| studded-panel-detail.webp | p/DZHl2NAEha6/ | 640×1138 | Hand-studded panel, brass oval frame | Craft section |
| residence-site-visit.webp | p/DeExrmUtNMM/ | 640×1136 | Designer on site at Lahore residence in progress | Studio section |

Every image links to its source Instagram post (factual provenance). No stock/AI images anywhere.

## 2. Contrast table — ALL PASS (WCAG AA, computed via relative luminance)
| Foreground | Background | Ratio | Gate | Where used | Result |
|---|---|---|---|---|---|
| Ink #232B26 | Ivory #F8F4EB | 13.24:1 | 4.5:1 | Headings, body, nav, footer text | PASS |
| Muted #4A524B | Ivory #F8F4EB | 7.36:1 | 4.5:1 | Secondary body copy | PASS |
| Brass-deep #8A6A33 | Ivory #F8F4EB | 4.57:1 | 4.5:1 | Eyebrow labels on light, button bg w/ ivory text | PASS |
| Ivory #F8F4EB | Forest #1B221E | 14.78:1 | 4.5:1 | Dark sections (band, craft, CTA), footer | PASS |
| Brass #C6A15B | Forest #1B221E | 6.68:1 | 4.5:1 | Eyebrows, numerals, captions on dark | PASS |
| Brass #C6A15B | Ink #232B26 | 5.99:1 | 3:1 | Hover states | PASS |

Brass is decorative-only on light backgrounds; all *text* on light uses ink/muted/brass-deep (all ≥4.57:1).

## 3. Image-fit audit — FULL VIEW, no crops
- Every `<img>` uses its exact native aspect-ratio wrapper + `object-fit: contain` (zero cropping possible), `width/height` attributes set, no stretch/distort.
- Hero (atrium, 640×800): displayed ≤448px wide / ≤560px tall (desktop cap met).
- Expertise cards (4 images, 640×853): 3-col grid → natural display ≈360×480px ≤ 480 cap. On mobile: single column, capped 360px wide.
- Studio image (640×1136): `max-height:480px`, width auto → ≈270×480, full view.
- Craft images: 640×853 → ≤480 tall; 640×1138 → ≈270×480, full view.
- Lazy-loading on all below-the-fold images; hero eager with `fetchpriority="high"`.
- Per-image check: all subjects (art panel, curtains, sofa, install team, leaf sculptures, studded panel, designer on site) fully in frame — nothing cut.

## 4. Responsive check — CSS audit (no headless Chromium on this VM)
- 1440px: hero 2-col (text + 448px image), expertise 3-col, craft/studio 2-col, band 3-col. No fixed widths; `.wrap` max 1180px.
- 768px: nav links hidden (brand + CTA remain); hero/studio/craft stack to 1 col; expertise → 2 col; band → 1 col.
- 390px: added dedicated query — brand + CTA sized down to fit one row (monogram 34px, brand-name 14px, CTA 13px, `white-space:nowrap`); expertise → 1 col (images ≤360px wide); hero CTAs full-width; studio image ≤440px tall. `overflow-x` has no trigger: no fixed-width elements, no negative margins.
- Verified programmatically: HTML balanced (no unclosed/mismatched tags), 8/8 imgs carry alt + width/height + lazy/eager, zero base64. **Not screenshot-verified (no Chromium available) — flag for a live visual check before the DM goes out.**

## 5. Fact sources (nothing invented)
All copy grounded in the JSON's `facts_for_site` / bio:
- "Interior Designer | Est. 2005 / Bespoke Interiors | Timeless aesthetics / Lahore / DM for consultation & inquiries" → hero eyebrow, H1, CTA wording, footer.
- Services: bespoke interiors, custom digital-print curtains, signature wall art installations, furniture design, marble/soft interior curation, fabric books & floor plans → Expertise cards + Process step 02.
- Project markers: 1-Kanal and 2-Kanal modern residences in Lahore → fact band + Studio copy. ("323-D coming soon" project marker deliberately NOT named on-site: the on-site photo's own overlay reads "332 G" — naming 323-D beside it could confuse. Photo caption is neutral: "a Lahore residence in progress".)
- "Head interior designer referenced as Nusrat Jamil; posts signed 'Signature Interiors by NJ'" → Studio copy + signature line + footer.
- No prices, reviews, ratings, hours, phone, or email invented. CTA is "DM for Consultation" → their own Instagram (factual channel per bio).

## 6. Honest caveats
- **Recency**: latest API-dated post is 2026-09-15 (38 days). Site avoids "latest work October 2026" claims; captions are timeless ("Open house — coming soon", "On site — a Lahore residence in progress"). Caveat NOT stated on the site (per brief), recorded here.
- **Visual check**: no headless Chromium on this VM — responsive verified by CSS audit + markup checks only. Recommend a live check at 390/768/1440px before DM send.
- Fonts loaded from Google Fonts (Fraunces + Inter, display=swap); if offline, falls back to Georgia/system sans.

## 7. DM draft (for parent — do not send without his order)
> Hi! I came across Interiors by Nusrat Jamil — a Lahore studio running since 2005 with that timeless, bespoke signature is rare to see done so consistently, from the digital-print curtains to the wall art installations.
>
> One thing stood out: everything runs through Instagram DM right now. A proper website would give your 20 years of work a home of its own — portfolio, services, and a consultation page that works even when you're busy on site.
>
> I put together a concept preview of what that could look like, using your own photos: https://the-cut-co.pages.dev/interiors-nusrat-jamil/
>
> Would you be open to a quick look? Happy to adjust anything — or build the real thing if you like the direction.
