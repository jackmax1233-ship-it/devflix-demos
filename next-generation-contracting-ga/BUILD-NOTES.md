# BUILD NOTES — Next Generation Contracting LLC (Winder, GA)

Preview site built Sun 25 Oct 2026 for the Devflix afternoon outreach batch.
Folder: `sites/next-generation-contracting-ga/` — `index.html` + `images/` (6 WebP files).

## Design
- Rugged roofing-trade palette: warm paper background, charcoal, rust-red accent, gold highlight. No gradients, no glassmorphism, no generic AI look.
- Fonts (2 families, Google Fonts, display=swap): **Bitter** (slab-serif display headings — trade/contractor feel) + **Inter** (body sans).
- Editorial split hero; photo-led sections, no card-grid clutter.

## Contrast table (WCAG AA: 4.5:1 normal text, 3:1 large text — all pairs PASS)
Computed from relative luminance; every pair below exceeds 4.5:1, so all text sizes pass.

| Text colour | Background | Ratio | Use |
|---|---|---|---|
| #FFFFFF | #1E2328 charcoal | 15.83:1 | Top bar, footer, gallery headings/body |
| #F7F4EE paper | #1E2328 charcoal | 14.42:1 | Gallery intro text |
| #23272B ink | #F7F4EE paper | 13.70:1 | Body text, nav links |
| #FFFFFF | #9C3319 rust | 7.24:1 | Primary buttons, contact section text |
| #F7F4EE paper | #9C3319 rust | 6.59:1 | Contact section body |
| #E8C15A gold | #1E2328 charcoal | 9.20:1 | Top-bar emphasis, footer links, gallery links |
| #FFFFFF | #6E2412 dark rust | 10.91:1 | Button hover state |
| #D8D2C4 sand | #1E2328 charcoal | 10.51:1 | Top-bar/footer secondary text |
| #5A5348 muted | #F7F4EE paper | 6.92:1 | Secondary body text, captions |
| #1E2328 charcoal | #E8C15A gold | 9.20:1 | Gold CTA button label |

## Image-fit audit (FULL-VIEW rule)
Every frame's aspect ratio matches its photo's natural ratio, so nothing is cropped — `object-fit: cover` at an identical ratio shows the full subject.

| File | Source post | Natural size | Frame | Fit result |
|---|---|---|---|---|
| hero-roof-1.webp | Dere0QCOGxA | 640×853 (3:4 portrait) | 3/4, max-height 560px | Full view, no crop |
| roof-2.webp | DczXAHeJXJ7 | 640×853 (3:4 portrait) | 3/4, max-height 340px | Full view, no crop |
| roof-3.webp | DcR3dWeJuoM | 640×640 (1:1 square) | 1/1, max-height 340px | Full view, no crop |
| roof-4.webp | DbHGkhFiYUh | 640×853 (3:4 portrait) | 3/4, max-height 340px | Full view, no crop |
| roof-5.webp | DZLiHbYCdbS | 640×640 (1:1 square) | 1/1, max-height 340px | Full view, no crop |
| roof-6.webp | DZGOvfLj0pb | 640×640 (1:1 square) | 1/1, max-height 340px | Full view, no crop |

- All images are the business's own Instagram photos (see harvest log). No stock/AI photos used.
- WebP, quality 78, converted from the 640px oEmbed thumbnails (Instagram's ceiling for this route).
- Hero image has `fetchpriority="high"`; all gallery images `loading="lazy"`; all images carry width/height attributes.
- Hero media capped at 560px tall on desktop; gallery frames capped at ~340px tall.

## Responsive audit (CSS)
- Mobile-first: fluid widths (`max-width:100%` on images, `width:100%` on `.wrap`), CSS grid with wrapping breakpoints at 900px (hero stacks, 3-col → 2-col) and 560px (all grids → 1 column, nav wraps, hero frame max 480px).
- No fixed pixel widths on layout containers; no horizontal overflow by construction (box-sizing: border-box throughout). Verified by CSS audit at ~390px / ~768px / ~1440px breakpoints (no live-browser check available to this builder — parent to confirm visually if desired).

## Fact sources (verified facts ONLY — nothing invented)
- Business: Next Generation Contracting LLC, Instagram @nextgenerationcontractingllc, 163 followers, Winder / Barrow County, Georgia, USA. Roofing contractor.
- Latest post 19 Oct 2026: completed home roof replacement (26 likes, 3 comments).
- Licensed & insured; BBB A-rated; free roof inspections; 45 posts of completed replacements; 13–30 likes + real comments per post at 163 followers.
- Phone in bio: (470) 385-8065. GAP: no website, zero bio links — enquiries only via phone or DM.
- Services shown are only those evidenced by the business's own posts: roof replacement, free roof inspections & estimates, storm damage inspections (all listed in the Dere0QCOGxA post caption).
- No prices, reviews, ratings beyond BBB A, or contact details beyond the verified facts above are claimed anywhere on the site.

## Photo harvest log (public Instagram oEmbed, 25 Oct 2026)
Method: `curl -A "Mozilla/5.0 (iPhone; CPU iPhone OS 17_0 like Mac OS X)" "https://www.instagram.com/api/v1/oembed/?url=https://www.instagram.com/p/<POST_ID>/"` — `author_name` verified as `nextgenerationcontractingllc` for all 6 posts; `thumbnail_url` downloaded with browser Referer/UA; converted to WebP quality 78.

| Post | Author verified | Result |
|---|---|---|
| https://www.instagram.com/p/Dere0QCOGxA/ | yes | hero-roof-1.webp (hero, latest post) |
| https://www.instagram.com/p/DczXAHeJXJ7/ | yes | roof-2.webp |
| https://www.instagram.com/p/DcR3dWeJuoM/ | yes | roof-3.webp |
| https://www.instagram.com/p/DbHGkhFiYUh/ | yes | roof-4.webp |
| https://www.instagram.com/p/DZLiHbYCdbS/ | yes | roof-5.webp |
| https://www.instagram.com/p/DZGOvfLj0pb/ | yes | roof-6.webp |

Photo shortfall: NONE — all 6 requested posts returned usable photos.

## Name-collision note
This site is for the Winder, Georgia firm ONLY. It is not affiliated with, and uses no facts or links from: nextgenerationcontracting.com (Santa Fe, NM), ngcontracting.net (Buffalo, NY), nextgenrestoration.net (Ohio / Kansas City). The Winder firm's BBB listing shows the same phone (470) 385-8065 and no website — consistent with the no-website gap. The collision note is also stated in the site footer.

## DM draft (natural, for parent to send — do NOT send from this build)
> Hi! I came across your page and your recent roof replacement post caught my eye — the finished roof looks great, and it's clear you take pride in the work. I did notice you don't have a website linked in your bio right now, so anyone finding you has to call or DM to get started. I put together a quick preview site for Next Generation Contracting using your own photos — it shows your completed replacements, your free inspections, and makes it easy for homeowners in Winder to reach you. Here's a look: [PREVIEW LINK]
>
> Would something like that be useful for your business?
