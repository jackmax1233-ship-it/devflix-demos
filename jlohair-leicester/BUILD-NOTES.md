# BUILD NOTES — JLOHair (Mobile Hairdresser, Leicester)

- Slug / preview URL (parent deploys): https://jackmax1233-ship-it.github.io/devflix-demos/jlohair-leicester/
- Instagram: @jennlohair (author_id 17841402239427972, 513 followers per research file)
- Design: warm cream #FBF6F1 + charcoal #241F1C panels + muted gold #7A5E2B accent. Fonts: Playfair Display (display serif) + Inter (body), Google Fonts display=swap. Elegant salon look, distinct from Siopa's romantic serif (different palette, fonts, layout tone).
- Structure: header nav, hero, What they do, Recent work gallery, Named in recent captions, Enquire panel, preview-concept note. No booking form, no testimonials, no prices (none published).

## Contrast table (WCAG AA, computed from hex values)
| Text | Background | Ratio | Result |
|---|---|---|---|
| #241F1C body/headings | #FBF6F1 | 15.18:1 | PASS (4.5:1) |
| #5A534C muted/lead/captions | #FBF6F1 | 7.04:1 | PASS |
| #FFFFFF enquire text | #241F1C charcoal panel | 16.31:1 | PASS |
| #FFFFFF button label | #7A5E2B gold button | 6.06:1 | PASS |
| #7A5E2B gold accent text | #FBF6F1 | 5.65:1 | PASS |

## Image-fit audit (all object-fit: contain, nothing cropped)
| File | Source post | Natural size | Frame | Fit |
|---|---|---|---|---|
| images/hero.webp | instagram.com/p/De3-XoZCMuM/ (24 Oct 2026) | 640x640 square | hero panel, max-height 540px | contain, full subject in frame |
| images/work1.webp | instagram.com/p/DezLM6BCOPE/ (22 Oct 2026) | 640x640 square | 1/1 frame, max-height 330px | contain, full subject |
| images/work2.webp | instagram.com/p/DewvksAiJ6y/ (21 Oct 2026) | 640x640 square | 1/1 frame, max-height 330px | contain, full subject |
| images/work3.webp | instagram.com/p/DeTm0sfCAd7/ (10 Oct 2026) | 640x640 square | 1/1 frame, max-height 330px | contain, full subject |
| images/work4.webp | instagram.com/p/DeJ4pFyCBZz/ (6 Oct 2026) | 640x640 square | 1/1 frame, max-height 330px | contain, full subject |
- All 5 photos: oEmbed author_name verified = jennlohair (match). No photo dropped. No base64; all separate WebP (quality 78), width/height attributes set, gallery lazy-loaded.
- Verified locally (Playwright/Chromium, file://): 390px / 768px / 1440px — scrollWidth == innerWidth at all widths, 0 broken images after scroll, hero 330px @390 / 540px @768 / 449px @1440, gallery <=330px tall.
- Flag: hair photos are close crops of finished styles by nature (the business's own posts). No faces are cut by the site: object-fit: contain shows each photo exactly as posted; any cropping in the source photo itself is the business's own framing, not the site's.

## Fact sources (research file batch-afternoon-31oct-UKIE-EU.json, published_facts only)
- "Mobile hair services in Leicester, in the client's home" — bio/location in research file.
- Services (colour, balayage, cut and style) — bio service list in research file.
- "DM for bookings" — bio instruction in research file; enquiry links to Instagram.
- Looks (iridescent pearl blonde, pixie cut, grey blending, champagne beige blonde) — recent work named in captions in research file. Looks are NOT mapped to specific photos (no per-post mapping in the research file).
- Gap: bio website field is only a Facebook page (facebook.com/JLOHair), not an own website (research file gap_evidence).
- NOT claimed: no prices, hours, phone number, testimonials, ratings, or stylist name (the research file gives the brand "JLOHair (Jennlo Hair)" — the site uses the brand name JLOHair only).

## DM draft (for parent to send; NOT sent by builder)
> Hi — your recent mobile work around Leicester caught my eye, from the pixie cuts to the grey blending you've posted, and I noticed bookings are DM-only with no website of your own yet. I put together a short preview site for JLOHair so clients can see your work and how to book in one place: https://jackmax1233-ship-it.github.io/devflix-demos/jlohair-leicester/ — would it be worth a quick look?
