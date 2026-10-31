# BUILD NOTES — Munro Garden Maintenance (Glasgow)

- Slug / preview URL (parent deploys): https://jackmax1233-ship-it.github.io/devflix-demos/munro-garden-maintenance-glasgow/
- Instagram: @munro_gardenmaintenance1 (author_id 17841460183726260, 345 followers per research file)
- Design: warm cream #F7F3E9 + deep garden green #1E4634 panels + soft parchment #EDE7D6. Fonts: Fraunces (display serif) + Public Sans (body), Google Fonts display=swap.
- Structure: header nav, hero, What they do, Recent work gallery, Enquire panel, preview-concept note. No booking form, no testimonials, no prices (none published). No "named in captions" chip list — the research file names work types, not client names, and none were invented.

## Contrast table (WCAG AA, computed from hex values)
| Text | Background | Ratio | Result |
|---|---|---|---|
| #1F2A22 body/headings | #F7F3E9 | 13.42:1 | PASS (4.5:1) |
| #4E5A51 muted/lead/captions | #F7F3E9 | 6.52:1 | PASS |
| #FFFFFF enquire text + button label | #1E4634 green panel/button | 10.60:1 | PASS |
| #1E4634 green accent text | #F7F3E9 | 9.57:1 | PASS |

## Image-fit audit (all object-fit: contain, nothing cropped)
| File | Source post | Natural size | Frame | Fit |
|---|---|---|---|---|
| images/hero.webp | instagram.com/p/Det2DGxDlvy/ (20 Oct 2026, driveway tidy) | 640x853 portrait | hero panel, max-height 540px | contain, full garden in frame |
| images/work1.webp | instagram.com/p/DasF9wFDkOd/ (12 Jul 2026) | 640x853 portrait | 3/4 frame, max-height 330px | contain, full subject |
| images/work2.webp | instagram.com/p/DanPe9filD1/ (10 Jul 2026) | 640x853 portrait | 3/4 frame, max-height 330px | contain, full subject |
| images/work3.webp | instagram.com/p/DanLiDMjmWn/ (10 Jul 2026) | 640x853 portrait | 3/4 frame, max-height 330px | contain, full subject |
| images/work4.webp | instagram.com/p/DXMKCOLDGNN/ (16 Apr 2026) | 640x853 portrait | 3/4 frame, max-height 330px | contain, full subject |
- All 5 photos: oEmbed author_name verified = munro_gardenmaintenance1 (match). No photo dropped. No base64; all separate WebP (quality 78), width/height attributes set, gallery lazy-loaded.
- Verified locally (Playwright/Chromium, file://): 390px / 768px / 1440px — scrollWidth == innerWidth at all widths, 0 broken images after scroll, hero 440px @390 / 540px @768-1440, gallery <=330px tall.
- Flag: gallery photos are Jul/Apr 2026 (the most recent posts after the 20 Oct hero in the research file's photo list); the business's latest post is 20 Oct 2026, so the site is still current, but the gallery is not all-October work. Nothing is misdated on the site (no dates shown on gallery images).

## Fact sources (research file batch-afternoon-31oct-UKIE-EU.json, published_facts only)
- "Glasgow-based gardeners" and "free quotes" — captions in research file.
- Work types (driveway tidy-ups, garden clear-outs, regular maintenance, grass cutting, edging, hedge reduction) — captions in research file.
- "Regular maintenance customers and property work referenced" — captions in research file; phrased generically on the site, no client names invented.
- Gap: bio website field empty, no bio link; posts end "Get in touch for a free quote" (research file gap_evidence); enquiry links to Instagram.
- NOT claimed: no prices, coverage areas beyond Glasgow, hours, phone number, testimonials, ratings.

## DM draft (for parent to send; NOT sent by builder)
> Hi Munro team — your recent driveway tidy and regular maintenance work around Glasgow stood out, and I noticed there's no website of your own yet, just Instagram with a free-quote offer. I made a short preview site for Munro Garden Maintenance so local customers can see your work and how to get a quote in one place: https://jackmax1233-ship-it.github.io/devflix-demos/munro-garden-maintenance-glasgow/ — would you like a quick look to see if that would be useful?
