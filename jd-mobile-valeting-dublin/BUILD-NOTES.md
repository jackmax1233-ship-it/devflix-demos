# BUILD NOTES — JD's Mobile Valeting (Dublin)

- Slug / preview URL (parent deploys): https://jackmax1233-ship-it.github.io/devflix-demos/jd-mobile-valeting-dublin/
- Instagram: @jd_mobile_valeting (author_id 17841421990695599, 519 followers per research file)
- Design: charcoal #16191C + amber-dark #8A5A00 on white / warm off-white #F2F0EB panels. Fonts: Barlow Condensed (display) + Inter (body), Google Fonts display=swap. No gradients, no glassmorphism.
- Structure: header nav, hero (text + photo), What they do, Recent work gallery, Named in recent captions, Enquire panel, preview-concept note. No booking form, no testimonials, no prices (none published).

## Contrast table (WCAG AA, computed from hex values)
| Text | Background | Ratio | Result |
|---|---|---|---|
| #16191C body/headings | #FFFFFF | 17.65:1 | PASS (4.5:1) |
| #4A5258 muted/lead/captions | #FFFFFF | 7.96:1 | PASS |
| #FFFFFF enquire text + button label | #16191C dark panel/button | 17.65:1 | PASS |
| #FFFFFF button label | #8A5A00 amber button | 5.93:1 | PASS |
| #8A5A00 accent links | #FFFFFF | 5.93:1 | PASS |

## Image-fit audit (all object-fit: contain, nothing cropped)
| File | Source post | Natural size | Frame | Fit |
|---|---|---|---|---|
| images/hero.webp | instagram.com/p/DfDQoOSkpWb/ (28 Oct 2026) | 640x853 portrait | hero panel, max-height 540px | contain, full car in frame |
| images/work1.webp | instagram.com/p/DepfTLQEeGi/ (18 Oct 2026) | 640x853 portrait | 3/4 frame, max-height 330px | contain, full subject |
| images/work2.webp | instagram.com/p/DeaCyXSkZOB/ (12 Oct 2026) | 640x853 portrait | 3/4 frame, max-height 330px | contain, full subject |
| images/work3.webp | instagram.com/p/DeNK2mIFZ1C/ (7 Oct 2026) | 640x853 portrait | 3/4 frame, max-height 330px | contain, full subject |
| images/work4.webp | instagram.com/p/Dd9vyo7lTjD/ (1 Oct 2026) | 640x853 portrait | 3/4 frame, max-height 330px | contain, full subject |
- All 5 photos: oEmbed author_name verified = jd_mobile_valeting (match). No photo dropped. No base64; all separate WebP (quality 78), width/height attributes set, gallery lazy-loaded.
- Verified locally (Playwright/Chromium, file://): 390px / 768px / 1440px — scrollWidth == innerWidth at all widths (no overflow), 0 broken images after scroll, hero rendered height 440px @390 / 540px @768-1440 (cap ~560px), gallery images <=330px tall. Mobile screenshot spot-checked: no overlap, full cars visible.

## Fact sources (research file batch-afternoon-31oct-UKIE-EU.json, published_facts only)
- "Mobile valeting in Dublin & surrounding areas" — bio/location in research file.
- "DM or WhatsApp to book" — bio booking instruction in research file. No phone number published, so none shown; enquiry links to Instagram.
- "Full Premium Valet" — service named in captions in research file.
- Cars (Audi Q7, Ford Ranger Wildtrak, Golf R, GTI, Audi A6, Audi A3) — recent jobs named in captions in research file. Car names are NOT mapped to specific photos (the research file does not give a per-post car mapping), so gallery captions stay neutral ("Recent work").
- Gap: bio website field empty, no bio link; booking DM/WhatsApp only (research file gap_evidence).
- NOT claimed: no prices, hours, phone number, service packages beyond the one named service, no testimonials, no ratings.

## DM draft (for parent to send; NOT sent by builder)
> Hi JD's team — I came across your recent valets around Dublin, including the Audi Q7 and Ford Ranger Wildtrak work you posted, and noticed booking is DM or WhatsApp only with no website of your own yet. I put together a short preview site for JD's Mobile Valeting so customers can see your work and how to book in one place: https://jackmax1233-ship-it.github.io/devflix-demos/jd-mobile-valeting-dublin/ — would it be worth a quick look to see if something like that would help?
