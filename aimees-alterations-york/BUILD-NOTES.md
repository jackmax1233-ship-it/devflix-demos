# BUILD NOTES — Aimée's Alterations (aimees-alterations-york)

Business: Aimée's Alterations · IG @aimees.alterations (author_id 17841451725568077)
Location: Sutton-on-the-Forest, York, England, UK — bridal seamstress, home studio
Built: 22 Oct 2026 (morning batch, site 1 of 3 — UK)

## 1. FACT SOURCES (all business-published, nothing invented)

| Fact | Value | Source |
|---|---|---|
| Name / handle | Aimée's Alterations / @aimees.alterations | IG profile |
| Bio (exact) | "Bridal Seamstress Aimée's alterations", "Bookings & Enquiries" | research brief, 22 Oct 2026 |
| Location | Home studio in the village of Sutton-on-the-Forest, York | research brief; confirmed non-India |
| Recognition | TWIA Regional Finalist 2025 & 2026 (The Wedding Industry Awards) | research brief |
| Education | York College national diploma + BA (Hons) in Fashion & Clothing; PGDIP in Garment Technology at London College of Fashion — 6 years studying | her Aug 7 intro post (research brief) |
| Services | Bridal dress alterations: fitting, pinning, reshaping, structural bodice work; wedding dress bustles; before/after gown transformations | research brief (facts_for_site) |
| Also works with | The Bridal Factory Outlet, Northallerton | Sep 27 caption (research brief) |
| Activity | Posts 2026-10-07 (39 likes/10 comments), 09-27 (40/7), 09-12 (69/15), 08-09 (87/8) — real engagement | research brief |
| Booking channel | Instagram DM (https://www.instagram.com/aimees.alterations/) | bio "Bookings & Enquiries" |
| Gap | No website — bio link is only a third-party LaceLink directory listing; web search found no official site | research brief |

Deliberately NOT on the site: phone, opening hours, prices, turnaround times (all
unpublished). No reviews/testimonials (none published). No permission claims on photos.

PHOTO NOTE: the site's 5th downloaded photo (aimee_0, showroom shot) carries an
on-image badge reading "REGIONAL FINALIST THE 2027 WEDDING INDUSTRY AWARDS", which
conflicts with the verified 2025 & 2026 fact. That photo was NOT used on the site.
Site uses only photos 1, 3, 4, 5 (bodice before/after, at-the-machine, garment bags,
bustle before/after). The 6th research post (reel DdKBJflIauV, bodice-pinning) 403'd
on CDN download; browser.open of the post returned no fresh image URL — 5 photos
were sufficient, so it was skipped.

## 2. CONTRAST TABLE (WCAG AA — standard relative-luminance formula)

| # | Element | Foreground | Background | Ratio | Result |
|---|---|---|---|---|---|
| 1 | Body text | #2E2A25 | #FBF7F0 (ivory) | 13.34:1 | PASS |
| 2 | Secondary body (.lede, figcaption, svc p) | #57504A | #FBF7F0 / #F3EAD9 | 7.42 / 6.63:1 | PASS |
| 3 | Eyebrow/kicker | #8A6A1F (gold) | #FBF7F0 | 4.72:1 | PASS |
| 4 | H1 accent + links | #7D444B (rose-deep) | #FBF7F0 | 7.02:1 | PASS |
| 5 | Primary button label | #FBF7F0 | #7D444B | 7.02:1 | PASS |
| 6 | Primary button hover label | #FBF7F0 | #2E2A25 | 13.34:1 | PASS |
| 7 | Outline button label | #7D444B | #FBF7F0 | 7.02:1 | PASS |
| 8 | Trust-band body text | #FBF7F0 | #2E2A25 (ink) | 13.34:1 | PASS |
| 9 | Trust-band kicker | #D9B36C (gold-light) | #2E2A25 | 7.20:1 | PASS |
| 10 | Trust-band small print | #CFC4B4 | #2E2A25 | 8.28:1 | PASS |
| 11 | Fact-row kickers | #5C6B52 (sage) | #FBF7F0 (visit card) | 5.34:1 | PASS |
| 12 | Contact-band body | #F0DDD9 | #7D444B | 5.73:1 | PASS |
| 13 | Contact-band eyebrow | #F3EAD9 (champagne) | #7D444B | 6.28:1 | PASS — was #D9B36C (3.79:1), fixed |
| 14 | Contact-band button label | #7D444B | #FBF7F0 | 7.02:1 | PASS |
| 15 | Footer text | #CFC4B4 | #2E2A25 | 8.28:1 | PASS |
| 16 | Footer links | #D9B36C | #2E2A25 | 7.20:1 | PASS |
| 17 | Footer devflix note | #9C937F | #2E2A25 | 4.68:1 | PASS |

No text sits over photographs — all copy is on solid ivory/champagne/ink/rose grounds.
ALL PASS after one fix (#13).

## 3. IMAGE-FIT AUDIT (per-image, full-view hard gate)

All 4 photos are her own Instagram work, portrait. Every frame uses `object-fit:
contain` on a solid card — ZERO cropping; whole subject (gown, bodice, face, hands)
visible on desktop and mobile. No cover crops anywhere.

| File (assets/) | Source | Natural | Displayed | Fit check |
|---|---|---|---|---|
| hero-bodice.webp (720×1280) | Bodice before/after transformation reel | 9:16 | Hero, 4:5 frame contain, max-height 540px desktop | Full view: both before & after panels + her hands fully visible |
| gallery-bustle.webp (880×1561) | Bustle before/after | 9:16 | Work section, 4:5 frame contain, max-height 560px | Full view: full skirt + bustle detail, nothing cut |
| about-atelier.webp (880×1173) | Aimée at her sewing machine | 3:4 | About, 3:4 frame contain, max-height 520px | Full view: face, hands, machine, dress form all visible |
| studio-personality.webp (720×1280) | Aimée carrying garment bags (fitting day) | 9:16 | Visit, 4:5 frame contain, max-height 480px | Full view: head to knees + all 3 garment bags in frame |

All WebP quality 78, separate files (no base64), width/height attrs set, lazy-load
below the fold, hero fetchpriority=high. Total image weight ~279 KB. `object-position:
center top` keeps heads/subjects anchored.

## 4. RESPONSIVE NOTES (mobile-first, code-verified)

- 390px: single column everywhere; nav shows brand + CTA button only (links hidden
  ≤639px, anchors reachable via footer); hero copy → CTA → photo; services stack;
  band items stack; contact band centered. Photo frames are width:100% contain —
  390px frame height ≤ ~487px, under the 70vh mobile guidance.
- 800/860px: hero becomes 2-col (copy | photo); services 2-col; trust band 3-col;
  about/visit become 2-col (image | text).
- 1440px: max-width 1120px container; no stretch.
- No horizontal overflow: grids use minmax auto / explicit 2-col with gap; all images
  max-width:100%; no vw units; body has no fixed widths.
- Motion: IntersectionObserver reveal gated behind `.js` (content fully visible
  without JS); `prefers-reduced-motion` kills reveals + smooth scroll.
- NOT verified in a live browser (subagent has no browser control) — the parent
  batch runner should do the live 390/768/1440 check before deploy.

## 5. DESIGN IDENTITY

Bridal-atelier editorial: ivory (#FBF7F0) + champagne (#F3EAD9) grounds, warm
charcoal ink (#2E2A25) text, dusty-rose (#7D444B) accents, sage (#5C6B52) and gold
(#8A6A1F) kickers. Cormorant Garamond (display serif) + Inter (body), Google Fonts
display=swap. Flat grounds, thin rules, numbered service list — no gradients, no
glassmorphism, no floating cards, no giant meaningless heading.

## 6. DM DRAFT (Instagram — to @aimees.alterations, author_id 17841451725568077)

> Hi Aimée! I've been looking at your fitting posts — the bodice reshaping
> before-and-after and the bustle transformation really show what goes into the
> work (not just taking up a hem).
>
> One thing I noticed: everything runs through Instagram DMs, and there's no
> website for brides to find you on Google — so anyone searching "bridal
> seamstress York" lands on a directory listing instead of your actual work.
>
> I put together a quick concept of how a simple one-page site could look for
> you — your services, your transformations, the TWIA finalist recognition, and
> a clear path to DM you: [PREVIEW LINK]
>
> Would a proper little home for your work be useful, or is Instagram handling
> bookings fine for you as is?

(Short; one genuine observation — the bodice/bustle posts showing real craft; why a
site helps HER — Google searches land on the directory listing, not her work;
preview placeholder; one low-pressure question. No fake compliments, no invented
stats, no spam wording. Name used because she publishes it.)
