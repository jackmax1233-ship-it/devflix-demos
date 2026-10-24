# SOFA Vet Care — Preview Site Build Notes
Built 2026-10-22 (morning batch, PK/Gulf). Deploy-ready: `index.html` + `assets/*.webp`.

## Design identity
Warm, trustworthy vet clinic. Palette: warm white paper (#FDFBF6), deep green (#16402C / footer #12291D), coral accent (#B4431F text / #A83D1B buttons) on a warm tint section (#EAF1EC). Fonts: Fraunces (display serif) + Inter (body). Editorial asymmetric layout: portrait photos paired with text blocks, staggered left/right rows — photo-led, not a card grid. Restrained reveal animation via IntersectionObserver gated behind `.js` (content fully visible without JS), `prefers-reduced-motion` respected, hover states on buttons/links.

## Contrast table (WCAG AA — computed, all pass)
| Pair | Ratio | Gate |
|---|---|---|
| Ink #1F2A24 on paper #FDFBF6 (body) | 14.35:1 | AA pass |
| White on green button #16402C | 11.64:1 | AA pass |
| Green #16402C text on paper (nav brand, links, h3) | 11.26:1 | AA pass |
| Coral #B4431F accent text on paper (eyebrow, kickers, tags) | 5.40:1 | AA pass (4.5+) |
| White on coral button #A83D1B | 6.27:1 | AA pass |
| Ink on tint #EAF1EC (why section body) | 12.93:1 | AA pass |
| Paper text on footer #12291D | 14.92:1 | AA pass |
| Muted #4C5A52 on paper (secondary text) | 7.02:1 | AA pass |
No text sits over images (all photos caption-free or captioned below). No failures — no fixes needed.

## Image-fit audit (FULL-VIEW gate)
All 5 photos are the clinic's OWN Instagram post graphics (harvested 22 Oct 2026 via live browser from @sofavetcare_qa's posts), converted to WebP quality 78 — NO stock, NO faces/paws cut. Frames match each photo's natural ratio exactly with object-fit:contain on a soft tint background, so every image shows in full with zero cropping:
- `hero.webp` 1440×1728 (natural 5:6): clinic's winter-care post — golden retriever + tabby in knitted clothes holding SOFA shopping bags (source: sofavet-1.jpeg). Frame aspect 5/6, desktop max-height 600px (within discipline), mobile 70vh cap. Full view.
- `checkup.webp` 1080×1350 (natural 1440×1800 = 4:5): clinic's vaccination post — vet with syringe beside a beagle (source: sofavet-2.jpeg). Frame 4/5, ≤480px. Full view.
- `diagnostics.webp` 1080×1350 (natural 4:5): clinic's behaviour post — golden retriever resting under a sofa, "Yes, Behaviour Can Tell You" (source: sofavet-3.jpeg). Frame 4/5, ≤480px. Full view.
- `grooming.webp` 1080×1350 (natural 4:5): clinic's winter-groom post — golden retriever in a towel with pet shampoo/conditioner/tools (source: sofavet-5.jpeg). Frame 4/5, ≤480px. Full view.
- `hotel.webp` 640×1136 (natural ≈9:16): clinic's vet in teal scrubs with SOFA logo (source: sofavet-4.jpg) — placed in the final "one call covers it all" row. Frame 9/16, ≤480px. Full view.
No base64, all WebP quality 78, separate files, lazy-load below fold (hero eager + fetchpriority), width/height attrs set to shipped sizes. No cover-cropping anywhere.
Note: the graphics carry the clinic's own branding and phone numbers baked in (4411 0178 / 3078 3337) — consistent with the site's verified facts. Site copy describes them via alt text only; nothing invented.

**Photo honesty note (resolved 22 Oct 2026, photo swap):** the initial build used stock stand-ins because IG media URLs were behind the login wall. The 22 Oct photo swap replaced them with the clinic's own IG post images — the site now uses real business photos, and the DM "website concept" framing no longer needs the stand-in disclaimer.

## Fact sources (all from the verified research + live IG reads 22 Oct 2026)
- Name, city, handle, follower count: SOFA Vet Care, Doha, Qatar, @sofavetcare_qa, ~2,720 (instagram-cli `post` read, 2026-10-22).
- Services list: IG bio verbatim — "All facilities under one Roof / Checkup & Surgeries / Ultrasound & Xrays / Vaccination & Deworming / Grooming / Pet Hotel / Pick & Drop Service".
- Phones: 4411 0178 and 3078 3337 — caption of Oct 13 post (instagram-cli read: "📞 4411 0178 / 📞 3078 3337"); Oct 7 post specifies 4411 0178 = call, 3078 3337 = WhatsApp. tel: links use +974 country code (Qatar).
- Instagram URL: https://www.instagram.com/sofavetcare_qa/ (profile in CLI result).
- Vaccination copy line mirrors their Oct 13 caption wording; grooming copy mirrors their Oct 7 caption ("clean, healthy, and comfortable coat").
- NO address, NO hours, NO prices published by the business — marked absent on the contact section ("call for directions — street address isn't published online"). Nothing invented: no reviews, ratings, stats, medical claims, or made-up amenities.

## DM draft (for instagram-messages-cli to author_id 17841413257102054)
> Hi! I noticed SOFA Vet Care offers so much under one roof — pet hotel, grooming, pick & drop — but it's all listed only in your Instagram bio, so pet owners searching on Google never find it. I put together a small website concept for you so people can see your services and call you in one tap: [PREVIEW LINK]. Would you like me to share it here so you can take a look?

(Short, one genuine observation, why a site helps them, real link, one low-pressure question. No fake compliments, no invented stats.)
