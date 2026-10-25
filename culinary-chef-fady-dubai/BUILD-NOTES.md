# BUILD NOTES — The Culinary by Chef Fady (Dubai)

- Slug: `culinary-chef-fady-dubai`
- Local dir: `~/workspace/instagram/lead-campaign/sites/culinary-chef-fady-dubai/`
- Intended preview link (NOT deployed by this task): https://jackmax1233-ship-it.github.io/devflix-demos/culinary-chef-fady-dubai/
- Instagram: @the_culinary_uae — booking CTA used on site: https://ig.me/m/the_culinary_uae
- Built: Sun 25 Oct 2026, morning batch. No DM sent, no tracker edited, no deploy made by this task.

## Design
Warm cream `#FAF6EE` + deep charcoal `#1E1C18` + olive `#3A3F2A` + brass `#7A5E1F` (labels) / `#C9A86A` (labels on dark). Fonts: Playfair Display (display serif) + Inter (body), Google Fonts with `display=swap`. Editorial split hero, food-led sections, no gradients, no glassmorphism, no floating cards. All image paths are relative (`images/xxx.webp`) for GitHub Pages subpath deploys. No base64 images in HTML.

## (a) Contrast table — 12 checked pairs, 12 PASS (WCAG AA)
Ratios computed from relative luminance (WCAG formula). Thresholds: ≥4.5:1 normal text, ≥3:1 large text.

| Text / element | On background | Ratio | Verdict |
|---|---|---|---|
| Charcoal `#1E1C18` body/headings | Cream `#FAF6EE` | 15.78:1 | PASS |
| Muted `#5C564A` body captions | Cream `#FAF6EE` | 6.75:1 | PASS |
| Brass label `#7A5E1F` eyebrow | Cream `#FAF6EE` | 5.65:1 | PASS |
| Olive `#3A3F2A` hover / section bg | Cream `#FAF6EE` (as text-adjacent) | 10.12:1 | PASS |
| Cream `#FAF6EE` headings/body | Charcoal `#1E1C18` band | 15.78:1 | PASS |
| Pale gold `#E8DCC0` band body | Charcoal `#1E1C18` | 12.50:1 | PASS |
| Brass-light `#C9A86A` eyebrow | Charcoal `#1E1C18` | 7.53:1 | PASS |
| Cream `#FAF6EE` button label | Charcoal `#1E1C18` button | 15.78:1 | PASS |
| Charcoal `#1E1C18` button label | Cream `#FAF6EE` light button | 15.78:1 | PASS |
| Charcoal `#1E1C18` text | Pale card `#FFFDF8` / `#EFE7D6` image bed | >14:1 (approx., both near-white) | PASS |
| White `#FFFFFF` (hover state reference) | Olive `#3A3F2A` booking band | 10.91:1 | PASS |
| Charcoal `#1E1C18` footer text | Cream `#FAF6EE` | 15.78:1 | PASS |

Note: a lighter brass `#8A6D2B` (4.53:1) was considered and rejected for small labels in favour of darker `#7A5E1F` (5.65:1) for a safer margin. No text sits over a photograph except figure captions below images, so no overlay-contrast risk.

## (b) Image-fit audit — FULL VIEW, no cropping of dishes
All source thumbnails are portrait (see harvest log). Frames were matched to that orientation:

| File | Source size | Placement | Container | Fit | Full view? |
|---|---|---|---|---|---|
| `charcuterie-board.webp` | 640×853 (3:4) | Hero + gallery reprise | aspect-ratio 3/4, max-height 560px desktop | cover in an identical 3:4 frame = no effective crop | Yes |
| `private-dinner.webp` | 640×853 (3:4) | Dark band | height 380px (≤420 band cap) | contain on `#2A2823` | Yes |
| `pasta-fresca.webp` | 640×853 (3:4) | Menu card | height 320px (≤340 card cap) | contain on `#EFE7D6` | Yes |
| `chicken-gyoza.webp` | 640×853 (3:4) | Menu card | height 320px | contain | Yes |
| `lebanese-cooking.webp` | 640×847 (~3:4) | Menu card | height 320px | contain | Yes |
| `chicken-quesadillas.webp` | 640×853 (3:4) | Menu card | height 320px | contain | Yes |
| `chef-at-home.webp` | 640×853 (3:4) | Gallery | height 340px | contain | Yes |
| `chef-plating.webp` | 640×853 (3:4) | Gallery | height 340px | contain | Yes |

Hero height: ≤560px desktop (520px at ≤860px width; at 390px width the 3:4 frame is ~468px tall — under the cap). Cards ≤340px, band 380px (≤420px). No `object-fit: cover` is used on a mismatched-ratio frame anywhere.
Honest note: the gallery re-uses `charcuterie-board.webp` as its third image because all 8 harvested photos are already used elsewhere on the page; no outside/stock image was substituted.

## (c) Fact sources — every claim traced
| Claim on site | Source |
|---|---|
| "Dubai's premium in-home chef experience" | Task brief (published description) |
| Private dining and daily cooking at home in Dubai; menus curated for the client | Task brief + IG post Dd1qLMZAt_w caption ("Your PRIVATE DINNER is right at home with a curated menu just for YOU") |
| Charcuterie board — "rich, fresh, sweet, and savoury" | IG post DexBSykiF4M caption |
| Pasta Fresca, handmade | IG post DeUr8cxAmYV caption ("Handmade to Perfection // Pasta Fresca") |
| Handcrafted Japanese chicken gyoza | IG post DefN28QAkLC caption |
| Lebanese cuisine, "cooking with intention" | IG post DdhK2QfgqTW caption + hashtags |
| Chicken quesadillas, "lunch for two… at your own home" | IG post Ddo96UTgoWm caption |
| Booking by Instagram DM; "You are a message away" | Task brief (bio has no website/phone/email; booking = "Send us a DM") + IG post DctyJkkkzsW caption |
| Dubai, UAE location; @the_culinary_uae | Task brief |
| "How it works" steps (DM → curated menu → dine at home) | Composed only from the verified facts above (DM route + curated menu + at-home service); no new service promise added |
| NOT on site, deliberately | No prices (none published — none invented), no phone, no email, no reviews/ratings, no follower counts, no invented dishes or service areas |

## (d) Photo harvest log — 8 harvested / 8 attempted, 0 failures
Method: public Instagram oEmbed endpoint with iPhone UA; `author_name` verified = `the_culinary_uae` for every shortcode; thumbnail downloaded with browser UA + Instagram Referer; converted to WebP quality ~78 via Python PIL (native 640px kept, no upscaling).

| Shortcode (post date) | author_name verified | File | Source px |
|---|---|---|---|
| DexBSykiF4M (2026-10-21) | the_culinary_uae | `images/charcuterie-board.webp` | 640×853 |
| DefN28QAkLC (2026-10-14) | the_culinary_uae | `images/chicken-gyoza.webp` | 640×853 |
| DeUr8cxAmYV (2026-10-10) | the_culinary_uae | `images/pasta-fresca.webp` | 640×853 |
| Dd1qLMZAt_w (2026-09-28) | the_culinary_uae | `images/private-dinner.webp` | 640×853 |
| Ddo96UTgoWm (2026-09-23) | the_culinary_uae | `images/chicken-quesadillas.webp` | 640×853 |
| DdhK2QfgqTW (2026-09-20) | the_culinary_uae | `images/lebanese-cooking.webp` | 640×847 |
| Dc1ZVJICSXc (2026-09-03) | the_culinary_uae | `images/chef-plating.webp` | 640×853 |
| DctyJkkkzsW (2026-08-31) | the_culinary_uae | `images/chef-at-home.webp` | 640×853 |

No shortfall in harvest. Total images folder: 8 WebP files, ~396 KB combined.

## Responsiveness — CSS audit (not a live browser pass)
Mobile-first CSS with breakpoints at 860px and 520px: hero/band/services/steps stack to one column, dish/gallery grids go 4→2→1 and 3→2→1 columns, nav wraps, no fixed widths that overflow. Verified by CSS audit only — this VM has no live Chromium pass, so a live visual check at ~390px / ~768px / ~1440px is still recommended before the link is sent.

## (e) Personalized DM draft (for parent to send — NOT sent by this task)
> Hi! I came across The Culinary by Chef Fady and loved how wide the cooking goes — handmade Pasta Fresca one day, handcrafted Japanese chicken gyoza the next, and Lebanese dishes cooked with intention, all in people's own homes in Dubai. Right now booking lives entirely in your DMs, since there's no website in your bio, so I put together a one-page preview to show how it could look as a proper home for the service — menus, private dinners and daily cooking, all leading back to your DM: https://jackmax1233-ship-it.github.io/devflix-demos/culinary-chef-fady-dubai/
>
> Would you like to see a version with your own menu details added?
