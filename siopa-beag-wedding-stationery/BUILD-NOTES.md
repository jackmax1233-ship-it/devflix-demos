# BUILD NOTES — Siopa Beag (Wedding Stationery by Claire, Ireland)

- Slug / preview URL (parent deploys): https://jackmax1233-ship-it.github.io/devflix-demos/siopa-beag-wedding-stationery/
- Instagram: @siopa.beag.iee (author_id 17841468244129909, 5,308 followers per research file)
- Design: ivory #FAF6EF + sage green #3E5145 panels + dusty rose #7E3B47 accent. Fonts: Cormorant Garamond (display serif) + Karla (body), Google Fonts display=swap. Editorial/romantic, distinct from all other batch sites.
- Structure: header nav, hero, What they do, Recent work gallery, Named in recent captions, Enquire panel, preview-concept note. No booking form, no testimonials, no prices (none published).

## Contrast table (WCAG AA, computed from hex values)
| Text | Background | Ratio | Result |
|---|---|---|---|
| #2E2A26 body/headings | #FAF6EF | 13.21:1 | PASS (4.5:1) |
| #5C554D muted/lead/captions | #FAF6EF | 6.81:1 | PASS |
| #FFFFFF enquire text + button label on sage panel | #3E5145 | 8.51:1 | PASS |
| #FFFFFF button label | #7E3B47 rose button | 7.49:1 | PASS |
| #3E5145 sage links/headings accents | #FAF6EF | 7.90:1 | PASS |
| #7E3B47 rose accent text | #FAF6EF | 7.49:1 | PASS |

## Image-fit audit (all object-fit: contain, nothing cropped; frames matched to each photo's orientation)
| File | Source post | Natural size | Frame | Fit |
|---|---|---|---|---|
| images/hero.webp | instagram.com/p/DfHIbyoonRS/ (30 Oct 2026, competition post) | 640x850 portrait | hero panel, max-height 540px | contain, full graphic in frame |
| images/work1.webp | instagram.com/p/De7F71QiIEw/ (25 Oct 2026) | 640x853 portrait | 3/4 frame, max-height 330px | contain, full subject |
| images/work2.webp | instagram.com/p/De7FF_wIYvK/ (25 Oct 2026) | 640x640 square | 1/1 frame, max-height 330px | contain, full subject |
| images/work3.webp | instagram.com/p/Dez3Kh7IbnS/ (22 Oct 2026) | 640x760 portrait | 3/4 frame, max-height 330px | contain, full subject |
| images/work4.webp | instagram.com/p/DesNA0hiE0q/ (19 Oct 2026) | 640x550 landscape | 3/2 frame, max-height 330px | contain, full subject |
- All 5 photos: oEmbed author_name verified = siopa.beag.iee (match). No photo dropped. No base64; all separate WebP (quality 78), width/height attributes set, gallery lazy-loaded.
- Verified locally (Playwright/Chromium, file://): 390px / 768px / 1440px — scrollWidth == innerWidth at all widths, 0 broken images after scroll, hero 438px @390 / 540px @768-1440, gallery <=330px tall. Mobile screenshot spot-checked: no overlap, stationery fully visible.
- Flag: the hero is the business's own 30 Oct competition graphic ("WIN 100 MASS BOOKLETS, 2026 & 2027 BRIDES" — its own published competition). It is used as a recent-work photo, not as an offer by Devflix; the site makes no competition claim of its own. If the parent prefers a suite photo as hero, swap hero.webp with work1.webp.

## Fact sources (research file batch-afternoon-31oct-UKIE-EU.json, published_facts only)
- "Wedding stationery by Claire, Ireland-wide" — bio in research file.
- Products (invitations, mass booklets, welcome signs, newspapers, venue illustrations, caricatures) — bio product list in research file.
- "DM to order" — bio instruction in research file; enquiry links to Instagram.
- Couples (Helena & Conor, Gabrielle & Anthony, Christina & Barry, Daniel & Niamh, Katie & Jason, Laura & Eoghan) — named-couple suites in October captions in research file. Couple names are NOT mapped to specific photos (no per-post mapping in the research file).
- Competition for 2026 & 2027 brides (30 Oct post) — research file; referenced only via the hero photo itself and the DM draft's "2026 & 2027 weddings" line.
- Gap: bio website field is only a third-party directory listing (letstalkweddings.ie), not an own website; bio says "DM to order" (research file gap_evidence).
- NOT claimed: no prices, turnaround times, testimonials, ratings. The WOL Awards finalist detail from the research narrative was deliberately NOT put on the site (it comes from a directory listing, not the business's own bio/captions in the file) — parent may add it only if verified on the business's own channels.

## DM draft (for parent to send; NOT sent by builder)
> Hi Claire — your recent suites for couples like Helena & Conor and Gabrielle & Anthony are lovely, and I noticed ordering is DM-only with no website of your own yet, just a directory listing. I put together a preview site for Siopa Beag so couples can browse your stationery and how to order in one place: https://jackmax1233-ship-it.github.io/devflix-demos/siopa-beag-wedding-stationery/ — would it be worth a quick look to see if that would help for 2026 & 2027 weddings?
