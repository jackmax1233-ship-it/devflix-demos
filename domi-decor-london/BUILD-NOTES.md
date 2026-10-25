# Domi Decor — Preview Site Build Notes

- **Business:** Domi Maintenance Ltd (Domi Decor) — painting & decorating, London, England, UK
- **Instagram:** [@domidecor_london](https://www.instagram.com/domidecor_london/) (6,228 followers at brief time)
- **Slug:** `domi-decor-london`
- **Intended preview link (deployment NOT done by this build):** https://jackmax1233-ship-it.github.io/devflix-demos/domi-decor-london/
- **Local dir:** `~/workspace/instagram/lead-campaign/sites/domi-decor-london/` — `index.html` + `images/` (9 WebP files, 8 placed on the page)
- **Status:** Built, NOT deployed, NO DM sent, NO tracker edited (per task scope).
- **Live visual pass:** NOT possible on this VM (no Chromium available to this agent). Responsive behaviour was verified by careful CSS audit only (mobile-first, stacking breakpoints at 900px and 560px, all widths use `min()`/percentages, no fixed-width elements). A live check at ~390px / ~768px / ~1440px is still recommended before the link is sent.

## (a) Contrast table (WCAG AA — computed, not estimated)

Computed with the standard relative-luminance formula. Pass = ≥4.5:1 for normal text, ≥3:1 for large text.

| Text / element | Foreground | Background | Ratio | Result |
|---|---|---|---|---|
| Body text, headings, facts list | `#23281F` ink | `#FAF6F0` cream | 13.98:1 | PASS |
| Muted text (captions, intros, card body) | `#5C6156` | `#FAF6F0` cream | 5.91:1 | PASS |
| Section headings on dark? n/a — headings on cream | `#1E3A2A` deep green | `#FAF6F0` cream | 11.52:1 | PASS |
| Buttons (header + hero) | `#FAF6F0` cream | `#1E3A2A` deep green | 11.52:1 | PASS |
| Ghost button text | `#1E3A2A` deep green | `#FAF6F0` cream | 11.52:1 | PASS |
| CTA band heading + button text | `#FAF6F0` / `#1E3A2A` | `#1E3A2A` / `#FAF6F0` | 11.52:1 | PASS |
| CTA band paragraph | `#C9CFC2` footer muted | `#1E3A2A` deep green | 7.79:1 | PASS |
| Footer text + links | `#C9CFC2` / `#FAF6F0` | `#1E3A2A` deep green | 7.79:1 / 11.52:1 | PASS |
| Eyebrow label | `#1E3A2A` deep green | `#FAF6F0` cream | 11.52:1 | PASS |
| Muted text on pale section bg | `#5C6156` | `#F1EDE3` cream-2 | 5.44:1 | PASS |
| Focus outline | `#9DB8A4` on green button hover state | — | decorative outline only, not text | n/a |

**Contrast pass: 11/11 text pairs pass AA.** No text is placed over photographs (captions sit below images on plain backgrounds), so no text-over-image contrast issue exists. The ochre/paint-swatch colours are decorative only and carry no text.

## (b) Image-fit audit (FULL VIEW — no finished work is cropped)

All harvested images are Instagram reel poster frames. 8 of 9 are portrait 360×640 (9:16); 1 is square 640×640. Every placed image uses `object-fit: contain` inside a frame, so the whole subject is always visible.

| Placement | File | Source size | Frame | Fit | Max height | Full view? |
|---|---|---|---|---|---|---|
| Hero | `reel-2026-10-22-barnes.webp` | 360×640 (9:16) | 9:16, width min(315px, 86vw) | contain | 560px | Yes — frame ratio matches source exactly |
| Gallery: kitchen | `reel-2026-10-21-richmond.webp` | 360×640 | 340px tall flex frame | contain | 340px | Yes |
| Gallery: bathroom | `reel-2026-10-21-c.webp` | 360×640 | 340px tall flex frame | contain | 340px | Yes |
| Gallery: exterior | `reel-2026-10-01-barnes.webp` | 360×640 | 340px tall flex frame | contain | 340px | Yes |
| Gallery: room being painted | `reel-2026-10-07.webp` | 360×640 | 340px tall flex frame | contain | 340px | Yes |
| Gallery: staircase finished | `reel-2026-09-24.webp` | 360×640 | 340px tall flex frame | contain | 340px | Yes |
| Gallery: staircase in progress | `reel-2026-09-23.webp` | 360×640 | 340px tall flex frame | contain | 340px | Yes |
| About / materials | `reel-2026-10-08.webp` | 640×640 (1:1) | 340px tall flex frame | contain | 340px | Yes |
| Held in reserve (not placed) | `reel-2026-10-21-richmond-b.webp` | 360×640 | — | — | — | n/a |

**Notes on the images themselves (disclosed, not hidden):**
- The poster frames carry Instagram's baked-in play-button overlay and, on two stills, on-video text from the original reel. These are part of the business's own source images; nothing was edited out, and the gallery note on the page says so plainly.
- No image was stretched, distorted, or cropped by CSS. `width`/`height` attributes are set on every `<img>`. No base64 images anywhere; all paths are relative (`images/…`) for GitHub Pages subpath deploys.

## (c) Fact sources — every claim traced

| Claim on the page | Source |
|---|---|
| Business name Domi Maintenance Ltd (Domi Decor) | Task brief (MyBuilder profile, same handle/company) |
| Painting & decorating, London | Task brief + Instagram bio |
| "An extremely high standard of painting and decorating" | Business's own Instagram bio wording (quoted in brief) |
| Interior / exterior work | Task brief + bio ("Interior / exterior") |
| Owner John Marku, 9+ years in painting & decorating | Task brief (MyBuilder profile) |
| Free, no-obligation quotations | Task brief (MyBuilder profile) |
| "Get in touch to get booked in" | Business's own Instagram bio wording (quoted in brief) |
| CTA https://ig.me/m/domidecor_london | Task brief — the only published contact route |
| No published phone or email | Task brief — page states this explicitly; no phone/email invented |
| Recent work areas Barnes, Mortlake & Sheen, Richmond | Instagram post location tags (brief + reel page metadata for 22 Oct / 21 Oct / 1 Oct posts) |
| Area line kept to "London" (no North/West London exclusivity claim) | Brief instruction, followed |
| Gallery captions (room type / interior vs exterior / area) | What is visible in each still + the post's own location tag where shown; no invented project names |
| "Preparation done properly — masking, filling, priming" | Visible in the stills (masking tape, dust sheets, filler/primer stages in the reels) |
| Swatch strip "Colours from recent rooms" | Colours observable in the placed stills (pale pink walls, warm white, grey plaster, charcoal cabinets) |
| No testimonials, ratings, prices, stats, or project names | None exist in the brief; none invented |

## (d) Photo harvest log

**Method change (honest):** the brief's oEmbed route returned the literal text `Private media` for ALL 9 post shortcodes — because every one of these posts is a **reel (video)**, and this oEmbed endpoint does not return media for reels. The profile oEmbed endpoint still worked (confirming author `domidecor_london`), but gave only the profile avatar. The stills were therefore harvested from each reel page's own `og:image` poster frame (the same Instagram CDN, same business account, fetched with the iPhone UA + Instagram Referer, converted to WebP quality 78 via Python PIL). No stock, AI, or other-business imagery was used at any point.

| Shortcode | Post date | Type | Result | File |
|---|---|---|---|---|
| `DezGNauIo8-` | 2026-10-22 | Reel | ✅ Poster frame harvested (360×640) | `images/reel-2026-10-22-barnes.webp` (11 KB) |
| `DexLn6MxlSp` | 2026-10-21 | Reel | ✅ Poster frame harvested (360×640) | `images/reel-2026-10-21-richmond.webp` (12 KB) |
| `DexH3j8xTY1` | 2026-10-21 | Reel | ✅ Poster frame harvested (360×640) | `images/reel-2026-10-21-richmond-b.webp` (10 KB) |
| `DexEZhxxlWS` | 2026-10-21 | Reel | ✅ Poster frame harvested (360×640) | `images/reel-2026-10-21-c.webp` (11 KB) |
| `DeOz7gQotx_` | 2026-10-08 | Reel | ✅ Poster frame harvested (640×640) | `images/reel-2026-10-08.webp` (41 KB) |
| `DeNJdcsRkVL` | 2026-10-07 | Reel | ✅ Poster frame harvested (360×640) | `images/reel-2026-10-07.webp` (11 KB) |
| `Dd9YXsDxaus` | 2026-10-01 | Reel | ✅ Poster frame harvested (360×640) | `images/reel-2026-10-01-barnes.webp` (30 KB) |
| `DdqT3QQRxcl` | 2026-09-24 | Reel | ✅ Poster frame harvested (360×640) | `images/reel-2026-09-24.webp` (17 KB) |
| `DdqRnZpxwEg` | 2026-09-23 | Reel | ✅ Poster frame harvested (360×640) | `images/reel-2026-09-23.webp` (17 KB) |

**Harvest: 9/9 attempted, 9/9 harvested, 0 failures, 0 substitutions.** One early slip was caught and fixed: two 21-Oct files initially shared one filename and one overwrote the other; both were re-saved under distinct names and all 9 files were re-verified on disk. Each still was visually checked: finished living room (Barnes), finished kitchen (Richmond), room mid-decoration, finished bathroom, paint cans, room being painted, exterior house with ladders (Barnes), finished staircase, staircase restoration in progress — all consistent with Domi Decor's painting & decorating work.

## (e) Personalized DM draft (for the parent agent to send — NOT sent by this build)

> Hi John, I came across Domi Decor on Instagram — the recent Barnes living-room transformation, from cracked walls to that smooth pale finish, really stood out, and your kitchen and staircase work shows the same standard throughout.
>
> One thing I noticed: there's nowhere for someone to see that work all in one place or get a quote except through Instagram, and your bio doesn't link anywhere. I put together a quick preview of how a simple website could look for Domi Decor, using your own recent photos — interior and exterior work, the free quotation offer, and a direct message button:
>
> https://jackmax1233-ship-it.github.io/devflix-demos/domi-decor-london/
>
> Would something like that be useful for getting booked in, or is Instagram working fine for you as it is?

**DM notes:** one genuine observation (the Barnes living-room reel, 22 Oct — crack repair to pale finish, verified from the reel itself); why a website helps *them* specifically (no link, no phone/email, Instagram is the only portfolio); no fake compliments, no invented stats, no claimed audit; one low-pressure question; preview link as specified in the brief.
