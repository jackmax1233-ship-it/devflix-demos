# BUILD NOTES — Skin and Smile Dental Clinic (Al Satwa, Dubai) preview site
Built 2026-10-22 ~10:30 PKT · site folder: ~/workspace/instagram/lead-campaign/sites/skin-and-smile-dental-dubai/

## Facts used (sources — nothing invented)
All facts from the business's own Instagram (@skinandsmiledentalclinic,
2,439 followers, author_id 17841455188669681) and the research handoff
(~/workspace/instagram/lead-campaign/research/batch-morning-22oct-PKGULF.json),
verified 2026-10-22:
- Name: Skin and Smile Dental Clinic · IG @skinandsmiledentalclinic
- Location: Al Satwa, Dubai, UAE — NOT India (geography gate passed)
- Bio: "SKIN AND DENTAL CLINIC IN SATWA DUBAI, UAE. For more info: 04 272 5458 / +971 56 423 3443"
- Address (Practo directory): ROSE HOUSE BLDG, ROOM 207, Al Hudaiba Rd, Al Badaa/Satwa, Dubai
- Hours (Practo): Mon–Thu & Sat–Sun 10:00–22:00. Friday hours not listed — site says "call ahead to confirm".
- Services (Practo): dental treatments incl. smile makeover/orthodontics, laser hair removal, Botox, PRP therapy
- Offer (IG caption, Oct 17 2026): teeth whitening 349 AED (was 499 AED) incl. FREE dental cleaning; valid Oct 17–29, 2026; Tabby & Tamara payments; call/WhatsApp 0564233443
- Braces/orthodontics also evidenced on their TikTok (@skinandsmile) — "braces" is a published term.
- Opportunity: no website — appointments by phone/WhatsApp only; real offers live only in IG captions; Google shows only Practo/Fresha directory pages.
- Nothing invented: no reviews, no ratings, no medical efficacy claims, no contact details beyond published phones.

## Images — FILLED with the clinic's real IG photos (2026-10-22 ~10:45 PKT)
Harvested by parent via live browser into
~/workspace/browser_downloads/sess-2915682410/harvest/. Converted to
optimized WebP (q78) with ffmpeg libwebp; no cropping, no edits — files
shipped at natural size (all ≤ max widths), object-fit:contain in the
wired frames so no text/logo/face is ever cut.

| Shipped file | Source photo | Content | Natural → shipped |
|---|---|---|---|
| assets/hero.webp | skinsmile-4.jpg | "BIGGEST OFFER! Veneers" promo graphic — confident smiling patient face + before/after veneers (Oct 17–29, 2026 dates) | 1136×1408 → 1136×1408 |
| assets/offer-whitening.webp | skinsmile-1.jpg | "BIGGEST OFFER! Teeth Whitening" graphic — 349 AED (was 499 AED) with FREE cleaning, Tabby & Tamara, phone 0564233443, Al Satwa Dubai | 1024×1360 → 1024×1360 |
| assets/clinic-interior.webp | skinsmile-2.jpg | "Dental X-Ray Services" graphic — IOPA 50 / OPG 120 / CBCT 300 AED; shows the modern treatment room with X-ray machine | 1248×1248 → 1100×1100 |

Skipped: skinsmile-3.jpg ("Zirconia Fixed Bridge" clinical mouth
close-up) — too graphic for a premium preview; not wired.
skinsmile-4 was chosen over skinsmile-1 for the hero so the hero and the
offer section show two different graphics; skinsmile-1 is the exact
349 AED offer graphic the DM references.

Fit decisions: all frames use object-fit:contain on tinted backgrounds
(#EAF6EF mint-soft for hero + duo photo, #0A2A28 dark for the offer
photo) — full-view always; object-position center (content is centered
in every graphic). Frames: hero 4:5 max-height 520px, offer 4:3
max-height 420px, duo 16:10 max-height 400px — all within the size
discipline (hero ≤560, content ≤480 desktop).
Contrast re-check: no CSS text overlaps any image (all captions/chips on
solid backgrounds) — the original contrast table stands unchanged. No
text was added on top of the clinic's graphics.

## Design
Modern-clinic identity: white + paper mint, deep teal #0E5B59, dark teal
sections, mint accent, terracotta/coral CTA (#A8441F buttons). Fonts: Sora
(display) + Inter (body), Google Fonts display=swap, 2 families. No
gradients, no glow, no glassmorphism, no floating cards, no giant
meaningless hero heading. Restrained motion: IntersectionObserver reveal
gated behind .js (content visible without JS), hover states,
prefers-reduced-motion respected.

## Contrast table (WCAG, computed — all ≥ 4.5:1 normal / 3:1 large)
| Pair | Ratio | Used for |
|---|---|---|
| #FFFFFF / #15211F ink | 16.55 | body text on white |
| #F7FAF9 paper / #15211F ink | 15.76 | headings/body on light section |
| #FFFFFF / #45514E body | 8.27 | secondary copy |
| #FFFFFF / #0E5B59 teal | 7.90 | kickers, links, brand sub-line, big tel numbers |
| #0E5B59 teal / #FFFFFF | 7.90 | primary buttons (white label), nav CTA |
| #07322F dark teal / #FFFFFF | 13.94 | offer + footer text |
| #07322F dark teal / #CDEEDD mint | 11.20 | offer kicker, price highlight, footer accents |
| #FFFFFF / #A8441F coral | 5.98 | WhatsApp buttons (white label) — same coral serves section kickers at 5.69 on paper |

No text over photos: all images sit in tinted contain-frames; chip labels
are on solid cards. No dark-text-on-dark anywhere.

## Responsive / full-view audit (static review — parent to verify live)
- Mobile-first; 2-col grids collapse to 1-col ≤940px; services 3→2→1; nav links hidden ≤760px (call button stays).
- Hero ≤560px desktop (hero figure max-height 520px); content images ≤480px.
- No fixed widths >100%; wrap max-width + padding; flex-wrap on CTAs/meta.
- Full-view: object-fit:contain everywhere → faces/smiles can never be cut.
- overflow-x:hidden on body; single-column flow at 390px.

## DM draft (for parent — DO NOT send myself; [PREVIEW LINK] placeholder)
> Hi — I came across Skin and Smile while looking at dental clinics in Satwa, and noticed your whitening offer (349 AED with free cleaning) lives only inside an Instagram caption — anyone Googling "teeth whitening Satwa" lands on directory pages, not on you.
>
> I mocked up what a simple site for the clinic could look like, using your own photos: [PREVIEW LINK]
>
> Would something like that be useful for turning searches into bookings, or are call and WhatsApp working fine for you as-is?

## Deliverables
- index.html + assets/ (3 real clinic photos, filled 2026-10-22 ~10:45 PKT) + PHOTOS-NEEDED.md (deleted — superseded by the fill above)
- ZIP: ~/workspace/instagram/lead-campaign/sites/skin-and-smile-dental-dubai.zip (rebuilt with photos, 2026-10-22 ~10:45 PKT)
- Parent handles: Cloudflare Pages deploy → DM send (author_id 17841455188669681) → tracker logging.
