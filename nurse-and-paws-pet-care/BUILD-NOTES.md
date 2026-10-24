# BUILD NOTES — Nurse & Paws Pet Care preview site

- Business: Nurse & Paws Pet Care — Instagram @nurseandpawspetcare (author_id 17841421237877093), Brisbane QLD, Australia, 349 followers
- Deploy target: https://the-cut-co.pages.dev/nurse-and-paws-pet-care/ (relative asset paths only — no absolute paths anywhere except Google Fonts CDN + Instagram links)
- Design: warm trustworthy pet-care identity — cream #FFF9F0, sand #F4E8D3, deep teal #0E5F60, warm amber #8A5200; Fraunces (display serif) + Nunito (rounded sans), 2 families, display=swap
- Photos: 7 of THEIR OWN Instagram pet photos, harvested via hatch-zeitgeist thumbnail URLs from their 8 most recent posts (Oct 3–19, 2026). Resized ≤1100w, WebP q78, separate files in img/, never base64, lazy-loaded below the fold, width/height attributes on every img

## Photo inventory (all real client-pet photos; kruize.jpg EXCLUDED — AI-generated meme, not a real photo)

| File | From post | Shows | Natural size | Placement / fit |
|---|---|---|---|---|
| img/teddy-hero.webp | /p/DesNEFBk5QC/ (Oct 19) | Teddy (Border Collie X) getting a belly rub on the couch | 1100×1466 portrait | Hero, aspect-3/4 frame ≈ photo ratio, cover, object-position 50% 22% — full subject visible |
| img/calmiko-walk.webp | /p/DeQGiEYEzaz/ (Oct 8) | Calmiko the Husky mid-walk, harness + leash, tongue out | 1100×1466 portrait | Service card "Dog walking", contain on sand matte — full view |
| img/ollie-sitting.webp | /p/Dco6RJsE_Xq/ (Aug 29) | Ollie the Cockerspaniel in a paw-print blanket on couch | 1100×1466 portrait | Service card "Pet sitting" + gallery, contain on sand matte — full view |
| img/myah-noah.webp | /p/DeNXCQgk0gQ/ (Oct 7) | Myah (Rottie) close-up, Noah (Toy poodle) behind on couch | 1100×1466 portrait | Service card "Home visits" + gallery, contain on sand matte — full view |
| img/calmiko-closeup.webp | /p/DegOoXak94S/ (Oct 14) | Calmiko's face close-up (one blue, one brown eye) | 1100×1466 portrait | About section, contain on cream matte — full view |
| img/calmiko-park.webp | /p/DentfKhk-ma/ (Oct 17) | Calmiko walking a jacaranda-lined park path | 1100×1451 portrait | Gallery, contain on sand matte — full view |
| img/ollie-asleep.webp | /p/DeDDJsZk72R/ (Oct 3) | Ollie asleep on a bed — CROPPED (200,500)→(1080,1350) to remove the "REVIEW" banner + review-text region of the composite | 880×850 | Testimonial card, cover — full dog visible, no text artifacts |

## Contrast audit (WCAG AA, computed — all pass)

| Pair | Ratio | Gate |
|---|---|---|
| Body ink #23282B on cream #FFF9F0 | 14.23 | AA ✓ |
| Teal #0E5F60 on cream (accents, links, H1 em) | 7.10 | AA ✓ |
| White on teal button #0E5F60 / hover #0A4849 | 7.44 / 10.31 | AA ✓ |
| Eyebrow amber #8A5200 on cream | 6.10 | AA ✓ |
| Muted #4E5A57 on cream (captions, card text) | 6.86 | AA ✓ |
| Ink on sand #F4E8D3 (trust strip) | 12.29 | AA ✓ |
| Teal on sand (trust-strip icons) | 6.14 | AA ✓ |
| Booking body #F2EFE6 on teal | 6.47 | AA ✓ |
| Booking eyebrow #F4E8D3 on teal | 6.14 | AA ✓ |
| Footer meta #C9C2B0 on ink | 8.39 | AA ✓ |
| Footer fine print #9b9584 on ink | 4.98 | AA ✓ |
| Step numbers teal on white | 7.44 | AA ✓ |
| No text over images anywhere (all captions sit below photos) | — | ✓ |

## Image-fit audit

- All 7 photos are portrait; hero frame uses aspect-ratio 3/4 ≈ photo's natural 3/4 → cover crops essentially nothing, face fully framed at 390/768/1440.
- Service/about/gallery images use object-fit: contain on sand/cream mattes → zero cropping by construction, faces never cut.
- Verified visually in headless Chromium screenshots at 390, 768 and 1440: hero, cards, about, testimonial, gallery all show full animal subjects.

## Responsive verification (headless Chromium, Playwright)

- 390px: overflow 0px, no page errors, no failed requests; sections stack, nav wraps, CTAs full-width-friendly.
- 768px: overflow 0px; cards 3-col ≥700px, gallery 4-col; testimonial 2-col.
- 1440px: overflow 0px; editorial 2-col hero + about.
- Screenshots: ~/workspace/instagram/lead-campaign/verify-shots/nurse-and-paws-pet-care-{desktop,tablet,mobile}.png
- Motion: IntersectionObserver reveal gated behind .js (content visible without JS), prefers-reduced-motion disables all transitions. Hero image: eager + fetchpriority high.

## Fact sources (ONLY published facts used — nothing invented)

- Name/handle/location: @nurseandpawspetcare, "Nurse & Paws Pet Care", Brisbane (profile + post URLs), service area "Brisbane & Moreton Bay Areas, QLD, Australia" (post captions Oct 8/16)
- Credential: "Qualified Vet Nurse with 20 years' experience" (bio); "Professional, reliable & gold standard pet care" (bio)
- Services: "Dog walking • Pet sitting • Home visits • More" (bio)
- Walk length: "dog walks from 30 minutes to 2 hours, tailored to suit your pup's needs" (Oct 14 caption)
- Medical care: Teddy's weekend included twice-daily eye drops for an eye condition (Oct 19 caption)
- Birds: looked after Teddy plus Ingrid & Spud the cockatiels over a weekend (Oct 19 caption)
- Owner name "Jordan": from Ruth's review published on the business's own Instagram (Oct 3 post)
- Testimonial: paraphrase (not verbatim) of Ruth Anderson's published review; attributed, marked "paraphrased with thanks"
- NOT published and NOT on the site: prices, hours, phone, email, address. Booking channel = Instagram DM only (bio has no email/phone/links)

## DM draft (~80 words) — Instagram, to author_id 17841421237877093

Hi! I came across Nurse & Paws and loved the Teddy belly-rub post — a 20-year vet nurse doing pet care in Brisbane is such a strong story, but right now Google can't find any of it since there's no website. I built you a little preview of what one could look like, using your own photos: [PREVIEW LINK]. If you ever want a proper site where locals can find you and book directly, I'd love to help — worth a look?
