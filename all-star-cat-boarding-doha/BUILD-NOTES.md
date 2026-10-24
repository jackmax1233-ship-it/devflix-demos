# BUILD NOTES — All Star Cat Boarding, Doha (all-star-cat-boarding-doha)

## Business facts (verified 22 Oct 2026 via research file batch-morning-22oct-PKGULF.json)
- **Business:** All Star Cat Boarding — IG @allstarcatboarding, author_id 17841469202436775
- **Location:** Doha, Qatar — a post lists Muntazah, Doha. (No phone / street address / hours / prices published.)
- **Since:** 2019, home-based cat boarding (per bio)
- **Bio (verbatim):** "home based Cat Boarding in Doha since 2019. Cat Boarding. Cage Free - Roam Free. Cat expert in handling different cat behavior. Vaccinated only"
- **Captions (verbatim):** "Clean & cozy rooms, Quality food, Daily care & attention, Safe & secure environment"
- **Boarding requirements (published):** cats must be VACCINATED, SPAYED, DEWORMED
- **Followers:** ~174; active Oct 2026 (posts 10-02/07/18; 2026-09-09 post: 23 likes / 4 comments)
- **Gap:** no website, no bio link — bookings via Instagram DM only; invisible to web searchers
- **NOT published (never invented in site copy):** street address / hours / prices / capacity / reviews. Note: their own promo graphic (used as hero) publishes WhatsApp 7060 7678 and "Muntazah" — site copy does not repeat the number.

## Gap evidence
- IG bio website field: EMPTY (verified via instagram-cli). Web search "All Star Cat Boarding Doha website": no own site — only competitors/directories (Parkview, Catari Cat Hotel, PetBacker).

## Photos used — BUSINESS'S OWN (swapped 22 Oct 2026 ~15:30 PKT)
All 6 Pexels stock WebPs were replaced with the business's own Instagram post graphics, harvested via live browser on 22 Oct 2026 from ~/workspace/browser_downloads/sess-2915682410/harvest/catboarding-1..5.jpg. Separate WebP files (quality 78), hero eager, rest lazy, width/height attrs set. No base64 anywhere.
| File | Source | Natural | Shipped | Fit decision (verified by viewing) |
|---|---|---|---|---|
| hero.webp | catboarding-1.jpg — their branded promo graphic (business name, "cage free roam free", requirements, WhatsApp 7060 7678, Muntazah) | 1254×1254 (1.00) | 1100×1100 | object-fit:contain in 1/1 frame on white — text/logos never cropped; hero capped 520px tall |
| cage.webp | catboarding-4.jpg — their photo: long-haired guest cat (sticker "Memories of Tommy") lounging in the boarding home | 1490×1987 (0.75) | 1100×1467 | cover in portrait 3/4 frame — exact ratio, object-position 50% 35%, face fully in frame |
| care.webp | catboarding-3.jpg — their 7-panel carousel graphic ("All Star Cat Boarding": why choose, what to prepare, what to bring, facilities, a typical day, plan ahead) | 1526×1024 (1.49) | 1100×738 | cover in landscape 3/2 frame — ratio match, all panel text fully readable |
| guest-doorway.webp | catboarding-2.jpg — their photo: guest cat hand-fed a treat (sticker @allstarcatboarding) | 640×1136 (0.563) | 640×1136 | cover in 4/5 frame, object-position 50% 30% — face, treat and sticker fully in frame; laptop/phone edges incidental |
| guest-window.webp | catboarding-5.jpg — their photo: guest cat in a crocheted pumpkin hat | 1215×2160 (0.5625) | 1215×2160 | cover in 4/5 frame, object-position 50% 30% — cat, face and hat fully in frame |
| guest-cuddle.webp | catboarding-4.jpg — same Tommy photo, reused in gallery with different caption (as the original layout did) | 1490×1987 (0.75) | 1100×1467 | cover in 4/5 frame, object-position 50% 40% — near-exact ratio, face fully in frame |
No invented photos remain. The phone number 7060 7678 visible in the hero graphic is the business's own published number (their IG post graphic), not invented. 6th gallery card reuses care.webp with object-fit:contain in its 4/5 frame so the carousel stays fully readable (white letterbox, no cropping).

## Palette & type
Warm cream ground + deep forest-teal + amber accents — cosy home-boarding identity. Fraunces (display serif) + Inter (body), Google Fonts display=swap. No gradients, no glassmorphism, no glow — flat editorial style.

## Contrast audit (computed, WCAG AA)
| Pair | Ratio | AA |
|---|---|---|
| Ink #1F3A34 on cream #FAF5EC (body/headings) | 11.29 | ✅ |
| Soft ink #57645E on cream (secondary) | 5.70 | ✅ |
| Teal #16655A on cream (kicker, links, ghost btn) | 6.35 | ✅ |
| Amber #8A4515 on cream (section labels) | 6.57 | ✅ |
| Cream #FAF5EC on teal #16655A (primary buttons) | 6.35 | ✅ |
| Cream #FAF5EC on deep teal #14332D (rules section) | 12.55 | ✅ |
| Muted #C9D4C9 on deep teal (rules body) | 8.92 | ✅ |
| Amber-deep #D9A441 on deep teal (rules labels) | 7.59 | ✅ |
| Ink on sand #F1E6D2 (gallery) | 9.92 | ✅ |
One draft amber (#B4601F on cream = 4.17) FAILED and was replaced with #8A4515 before shipping. No text over photos anywhere.

## Responsiveness
Mobile-first; single-column stacks under 820–900px; tested breakpoints 390 / 768 / 1440. Nav links hide on mobile, CTA remains. No fixed heights except hero max-height; images use aspect-ratio frames. Sticky nav with backdrop blur.

## Motion
IntersectionObserver reveal gated behind `.js` (content visible without JS); prefers-reduced-motion disables transitions; hover states on buttons/links.

## Facts sources
- Bio, captions, requirements, followers, location: ~/workspace/instagram/lead-campaign/research/batch-morning-22oct-PKGULF.json (qualified[1])
- Photos: the business's own Instagram post graphics (harvested 22 Oct 2026 via live browser; swap date logged above)
- CTA: https://www.instagram.com/allstarcatboarding/ (their own handle — bookings currently run here)

## DM DRAFT (Instagram — @allstarcatboarding; author_id 17841469202436775)
> Hi! I came across All Star Cat Boarding — I love that it's a real home setup in Doha and cage free since 2019. One thing I noticed: when pet owners in Doha search Google for cat boarding, there's no website to find you — everything runs through DMs. I built a one-page site concept for you using your own Instagram photos: [PREVIEW LINK]. Would you be open to a proper version with your own photos and a booking form?

Honest, no invented claims, one question, no spam wording. Photos swapped for the business's own on 22 Oct 2026 — ready to send.
