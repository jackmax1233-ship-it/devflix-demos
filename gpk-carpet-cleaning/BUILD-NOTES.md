# BUILD-NOTES — GPK Carpet Cleaning preview site

Folder: `~/workspace/instagram/lead-campaign/sites/gpk-carpet-cleaning/`
Built: Sun 25 Oct 2026 (afternoon outreach batch). No DM sent. Tracker not edited.

## Design
Trade-business palette, no gradients/glassmorphism: deep navy `#122B3A`, warm cream `#F7F3EA`, dark clean-green `#14532D` for buttons/accents, pale gold `#FBEED3` for the secondary button. Serif display + system sans body. Mobile-first: single column under 768px, cards 3→2→1 columns, nav wraps, all widths fluid with `max-width:100%` behaviour via the `.wrap` container; hero image capped at 560px tall on desktop (480px under 480px width), gallery images capped at 340px tall.

## Contrast table (WCAG AA: 4.5:1 normal text, 3:1 large text — all pairs pass)
Ratios computed from relative luminance of the exact hex values used.

| Text / element | Foreground | Background | Ratio | Pass |
|---|---|---|---|---|
| Body text | `#1E2A32` | `#F7F3EA` cream | 13.24:1 | Yes |
| Headings | `#122B3A` | `#F7F3EA` cream | 13.24:1 | Yes |
| Header brand/nav | `#FFFFFF` | `#122B3A` navy | 14.66:1 | Yes |
| Header subtitle | `#D9E8DD` | `#122B3A` navy | 11.55:1 | Yes |
| Primary button label | `#FFFFFF` | `#14532D` green | 9.11:1 | Yes |
| Secondary button label | `#122B3A` | `#FBEED3` pale gold | 12.76:1 | Yes |
| Green accent text (eyebrow, price) | `#14532D` | `#F7F3EA` / `#FFFFFF` | 8.23:1 / 9.11:1 | Yes |
| Captions | `#3D4A53` | `#FFFFFF` | 9.12:1 | Yes |
| Price-band text/headings | `#FFFFFF` | `#14532D` green | 9.11:1 | Yes |
| Contact panel text/links | `#FFFFFF` | `#122B3A` navy | 14.66:1 | Yes |
| Footer text | `#3D4A53` | `#F7F3EA` cream | 8.23:1 | Yes |
| Strip check marks (decorative) | `#8FC7A3` | `#122B3A` navy | 7.59:1 | Yes (decorative only) |

## Image-fit audit (full view — no cropping)
All photos are shown with `object-fit: contain` on a white card background, at their natural portrait ratio, so nothing is cut. No `object-fit: cover` is used anywhere.

| File (WebP, q78) | Source post | Natural size | Used as | Fit check |
|---|---|---|---|---|
| `images/De3oT9wCA2A.webp` (88 KB) | https://www.instagram.com/p/De3oT9wCA2A/ | 640×801 portrait | Hero | Contain, max-height 560px desktop; technician, van and rug all fully visible |
| `images/DeO-GL_iKQS.webp` (73 KB) | https://www.instagram.com/p/DeO-GL_iKQS/ | 640×801 portrait | Gallery — staircase | Contain, max-height 340px; full staircase in frame |
| `images/DeNjCcjCPW8.webp` (31 KB) | https://www.instagram.com/p/DeNjCcjCPW8/ | 640×801 portrait | Gallery — award graphic | Contain, max-height 340px; whole badge + caption text visible |

## Photo harvest log
Method: public oEmbed (`curl -A "Mozilla/5.0 (iPhone; CPU iPhone OS 17_0 like Mac OS X)" https://www.instagram.com/api/v1/oembed/?url=...`), thumbnail downloaded with browser Referer/UA, converted to WebP quality 78. `author_name` verified as `gpkcarpetcleaning` for all four posts.

| Post | Result |
|---|---|
| https://www.instagram.com/p/De3oT9wCA2A/ | Used (hero) |
| https://www.instagram.com/p/DernXvbCJ-B/ | NOT used — near-duplicate of the hero graphic (same van/technician illustration, minor crop difference). Using both would look like a mistake. No shortfall in quality: 3 distinct photos used. |
| https://www.instagram.com/p/DeO-GL_iKQS/ | Used (gallery) |
| https://www.instagram.com/p/DeNjCcjCPW8/ | Used (gallery) |

No stock or AI photos used. All images are the business's own Instagram photos.

## Fact sources — nothing beyond these was invented
- Business: GPK Carpet Cleaning, Instagram @gpkcarpetcleaning, 603 followers, South Wales / Gwent area (Cwmbran, Pontypool, Newport, Cardiff) — task brief.
- Prices/services: 24 Oct 2026 price-list carousel — 1–4 rooms £35–£80; Scotchgard, rugs, stairs, sofas, car interiors — task brief. Individual prices for rugs/stairs/sofas/cars/Scotchgard were NOT given, so the site lists them as "message for a quote" and does not invent figures.
- Bio: "DM to get a quote" — task brief; phone 07956173481 — task brief (also appears in the harvested post caption).
- 2,335 posts of before/after work; fully insured; domestic + commercial — task brief.
- Stain & odour treatments, carpet deep cleaning, sofa & upholstery — from the harvested caption of post De3oT9wCA2A itself.
- "700+ reviews on Facebook/Google" — phrased on the site as GPK's own claim ("GPK says they have…"), not as a verified rating. Source: their own posts per the task brief.
- No address, email or opening hours are shown — none were in the verified facts.

## Flags for the parent (do not silently "fix" in the site)
1. The hero graphic itself (their own post image) shows two extra phone numbers on the van (07512… and 01495…) besides the brief-verified 07956173481. The site's text lists ONLY 07956173481; the image is shown unedited as their own published photo. If the parent wants those numbers hidden, that needs a cropped/edited image decision, not a silent text change.
2. The award graphic itself carries the text "Caerphilly and Surrounding Areas, Caerphilly, UK CF83 1AD". The site text does NOT repeat this address/postcode (not in the verified brief); it captions the image only as an award graphic shared on their Instagram.
3. The 24 Oct price-list carousel itself was not among the four photo posts supplied; the £35–£80 range is used solely on the brief's authority.

## Verification (run before handover)
- `index.html` present; all 3 image references resolve to existing files in `images/`.
- 0 base64 strings in `index.html`; 0 absolute-path (`src="/…"` / `href="/…"`) references; all image paths relative (`images/…`).
- All images lazy-loaded below the fold (`loading="lazy"`); hero has `width`/`height` attributes and `fetchpriority="high"`.
- Responsive audit by CSS review only (subagent has no live browser): fluid grid, wrapping flex/nav, media queries at 768px and 480px, no fixed pixel widths on containers. Live-browser check at ~390px / ~768px / ~1440px is still needed before the link goes out in a DM.

## DM draft (for the parent to send — do not send from here)
> Hi GPK team — I came across your page and noticed your prices currently live as post graphics, with no website or link in bio for people to find them. I made you a quick concept site so customers can see your rooms pricing (£35–£80), your stairs, sofa, rug and car-interior services, and your work in one place, with a straight route to DM you for a quote: [PREVIEW LINK]
>
> It's just a concept — happy to change anything or hand it over if it's useful. Would a simple site like this help with the enquiries you get from Instagram?
