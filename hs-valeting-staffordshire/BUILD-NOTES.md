# BUILD NOTES — HS Valeting (Staffordshire)

- Slug / preview URL (parent deploys): https://jackmax1233-ship-it.github.io/devflix-demos/hs-valeting-staffordshire/
- Instagram: @hs.valeting1 (author_id 17841427223984026, 88 followers per research file)
- Design: white + near-black #111111 panels + detailing red #A61E22 accent. Fonts: Oswald (display) + Source Sans 3 (body), Google Fonts display=swap. Deliberately distinct from JD's Dublin site (different palette, fonts, accent) — the two valeting businesses are not templated alike.
- Structure: header nav, hero, What they do, Recent work gallery, Named in recent captions, Enquire panel, preview-concept note. No booking form, no testimonials, no prices (none published).

## Contrast table (WCAG AA, computed from hex values)
| Text | Background | Ratio | Result |
|---|---|---|---|
| #171717 body/headings | #FFFFFF | 17.93:1 | PASS (4.5:1) |
| #555555 muted/lead/captions | #FFFFFF | 7.46:1 | PASS |
| #FFFFFF enquire text | #111111 dark panel | 18.88:1 | PASS |
| #FFFFFF button label | #A61E22 red button | 7.42:1 | PASS |
| #A61E22 accent links | #FFFFFF | 7.42:1 | PASS |

## Image-fit audit (all object-fit: contain, nothing cropped)
| File | Source post | Natural size | Frame | Fit |
|---|---|---|---|---|
| images/hero.webp | instagram.com/p/De7W_7KjUhO/ (25 Oct 2026) | 640x853 portrait | hero panel, max-height 540px | contain, full car in frame |
| images/work1.webp | instagram.com/p/De37_mvjSYv/ (24 Oct 2026) | 640x853 portrait | 3/4 frame, max-height 330px | contain, full subject |
| images/work2.webp | instagram.com/p/Dez_U3ajVE4/ (22 Oct 2026) | 640x853 portrait | 3/4 frame, max-height 330px | contain, full subject |
| images/work3.webp | instagram.com/p/DeuF9FjjRsE/ (20 Oct 2026) | 640x853 portrait | 3/4 frame, max-height 330px | contain, full subject |
| images/work4.webp | instagram.com/p/Dergz3CDWYG/ (19 Oct 2026) | 640x853 portrait | 3/4 frame, max-height 330px | contain, full subject |
- All 5 photos: oEmbed author_name verified = hs.valeting1 (match). No photo dropped. No base64; all separate WebP (quality 78), width/height attributes set, gallery lazy-loaded.
- Verified locally (Playwright/Chromium, file://): 390px / 768px / 1440px — scrollWidth == innerWidth at all widths, 0 broken images after scroll, hero 440px @390 / 540px @768-1440, gallery <=330px tall.

## Fact sources (research file batch-afternoon-31oct-UKIE-EU.json, published_facts only)
- "Staffordshire and surrounding areas" — bio/location in research file.
- "Clean - Protect - Shine" and "Premium Car Detailing" — business's own wording in research file.
- "Mini detail" — service named across recent posts in research file.
- "Bookings via DM" — every post ends with DM booking CTA in research file; enquiry links to Instagram.
- Cars (BMW M3 Competition, Golf R, Seat Leon Cupra, Mercedes A35 AMG, Mercedes A-Class) — recent jobs named in captions, each described as a mini detail. Car names are NOT mapped to specific photos (no per-post mapping in the research file).
- Gap: bio website field empty, no bio link (research file gap_evidence).
- NOT claimed: no prices, hours, phone number, extra packages, testimonials, ratings.

## DM draft (for parent to send; NOT sent by builder)
> Hi HS team — your recent mini details around Staffordshire caught my eye, especially the BMW M3 Competition and the A35 AMG work, and I noticed bookings run through DM with no website of your own yet. I made a short preview site for HS Valeting so your detailing work and how to book are in one place: https://jackmax1233-ship-it.github.io/devflix-demos/hs-valeting-staffordshire/ — would you like a quick look to see if that would be useful?
