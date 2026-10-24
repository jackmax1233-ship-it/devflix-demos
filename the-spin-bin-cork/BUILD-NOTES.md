# BUILD NOTES — The Spin Bin (the-spin-bin-cork)

Preview concept for Devflix outreach, morning batch 23 Oct 2026.
Target final URL: https://the-cut-co.pages.dev/the-spin-bin-cork/

## Lead facts (ONLY source: `~/workspace/instagram/lead-campaign/research/batch-morning-23oct-UKIE.json`)
- Business: **The Spin Bin** — launderette, Cork / Bandon, Ireland. IG: `the.spinbin` (1,981 followers).
- Services (JSON): self-service / drop-off / home collections. Two locations: **Model Farm Rd, Cork** + **Bandon** store.
- No own-domain website. Bio link is only a third-party CleanCloud booking widget: `cleancloudapp.com/s3/39601`.
- Engagement: 2026-09-18 carousel announcing the new Bandon store — 103 likes, 9 comments; 2026-10-06 post "Book your collection here" CTA (13 likes); 2026-10-16 post (22 likes).
- JSON explicitly noted NO prices/hours in the research file — but photo-1 (their own published Instagram price-list poster, downloaded from their CDN) printed the full price list and was used as the verified source for the Prices section (see below). Nothing else was invented.

## Additional VERIFIED facts (from their own published Instagram post — photo-1 price poster)
These facts come from the business's own price-list poster (downloaded from their Instagram CDN), not from the JSON text — all copy on the site traces to this image:
- Tagline: "Fresh. Clean. Ready for you." / Service words: "Wash | Dry | Fold | Collection"
- Wash, Dry & Fold — Clothing: 0–6 kg €19 / 6–10 kg €28 / 10–14 kg €40 / 14–18 kg €50
- Wash, Dry & Fold — Mixed Bag: 0–6 kg €24 / 6–10 kg €35 / 10–14 kg €45 / 14–18 kg €54
- Dry & Fold Only: 0–6 kg €12 / 6–10 kg €15 / 10–14 kg €20 ("Bags weighed when dried")
- Bedding Duvet/Comforter: Single/Double €25 / King/Queen €30
- Collection & Delivery: 0–6 kg €24 / 6–10 kg €35 / 10–14 kg €45 / 14–18 kg €54
- Self-Service: Wash 10 kg (Small) €6, 14 kg (Medium) €9, 18 kg (Large) €12; Pet Machine wash €6; Dry 14 kg €3/15 min, €5/30 min; 18 kg €4/15 min, €6/30 min; Pet Machine dry €6/45 min
- "Separated loads. Each extra load is charged an additional €10."
- Collection steps: "Choose the date and time / Choose the address for collection / We collect, wash, dry and fold / We deliver back to you"
- Locations with Eircodes: **Model Farm Rd, Cork T12 AH79** / **Bandon P72 VW21**
- Contact from poster: "Book your collection in our Instagram bio or WhatsApp **085 7222283**" (wa.me link uses +353 85 — standard Irish mobile format for an 085 number)
- Photo-2 (their own post overlay): "Laundry Home Collection Service — **7 days per week, 9am–8pm**" (attributed on-site as the *collection service* hours, not store hours — store hours were never published, so none are claimed)

## Booking-link choice (documented per task)
- Primary "Book a collection" CTA → `https://cleancloudapp.com/s3/39601` — this is The Spin Bin's OWN public booking link (their only bio link, per the research JSON). A preview site that books through any other widget would be inventing their booking flow; using their own link keeps the demo honest. It is clearly their third-party widget, which is exactly the pain point the DM names.
- Secondary CTAs → `https://www.instagram.com/the.spinbin/` (DM to book) and `https://wa.me/353857222283` (their published WhatsApp number).

## Photos — download log (downloaded 23 Oct 2026 ~05:20 PKT, promptly — URLs are time-signed)
Command per task spec (iPhone UA + instagram.com referer). 8 URLs in JSON; **4 succeeded, 4 failed**:
| # | Result | Size | Content |
|---|--------|------|---------|
| photo-1 | ✅ 200 | 640×800 portrait | **Their published price-list poster** — used in Prices section |
| photo-2 | ✅ 200 | 640×480 landscape | Launderette interior + "Home Collection Service 7 days 9am–8pm" overlay — hero |
| photo-5 | ✅ 200 | 640×853 portrait | Spin Bin shopfront — Stores section |
| photo-8 | ✅ 200 | 640×790 portrait | Dog at the dedicated pet wash machine — Pet section |
| photo-3/4/6/7 | ❌ 403 ×2 attempts | 22-byte body: **"URL signature mismatch"** | CDN signatures expired — NOT retried further |

- Per instructions: NO stock/AI substitutions. The 4 failed photos are simply not used; the site is fully built from the 4 genuine photos. Failed 403 files deleted.
- All 4 converted to WebP q78 at native size (never upscaled), saved to `assets/`: `price-poster.webp` (79 KB), `store-interior.webp` (35 KB), `storefront.webp` (99 KB), `pet-wash.webp` (54 KB). No base64 anywhere.

## Contrast audit (WCAG AA — computed, all rows PASS at normal-text 4.5:1)
Palette: paper #FBFAF7 · ink #0B2A4A · teal #0B6B6B (buttons) · teal-deep #0A5E5D · mint #E7F4F3 · muted slate #44515F · footer-muted #C9D6E2
| Pair | Ratio | Result |
|------|-------|--------|
| Ink on paper (body, headings, nav, footer text) | 13.93:1 | PASS |
| White on ink (dark buttons, store cards, final CTA bg) | 14.54:1 | PASS |
| Muted slate on paper (secondary/lead text) | 7.77:1 | PASS |
| White on teal #0B6B6B (primary CTA buttons) | 6.31:1 | PASS |
| Teal-deep on paper (teal headings, h1 em, strip) | 7.26:1 | PASS |
| White on teal-deep (collection band text/buttons) | 7.58:1 | PASS |
| Teal-deep on mint (eyebrow chips, tags) | 6.72:1 | PASS |
| Ink on mint (price note text zone) | 12.90:1 | PASS |
| Footer-muted on ink (final-CTA paragraph, store eircodes) | 9.83:1 | PASS |
| Teal-deep price values on white cards | 7.58:1 | PASS |
| Muted slate on white cards | 8.11:1 | PASS |
| Muted slate on mint (price-note bar) | 7.20:1 | PASS |
| Band sub-text (white 92% opacity, blended → #ebf2f2 on #0A5E5D) | 6.68:1 | PASS |
| Step text (white on blended #226e6d tile bg) | 5.97:1 | PASS |
| Band eyebrow (white on blended #317877 chip) | 5.14:1 | PASS |
All opacity-blended pairs were computed against their effective blended colours, not assumed.

## Image-fit audit (FULL VIEW — nothing cropped)
- All 4 images displayed at or below native 640px width, `height:auto` (natural aspect preserved), `width`+`height` attributes set, `loading="lazy"` below the fold (hero eager).
- **No `object-fit: cover` crops anywhere.** Hero uses `object-fit: contain` at the image's exact native 4:3 ratio — zero letterboxing, zero cropping. Subjects (machines, shopfront sign, dog, price poster) fully visible.
- Portrait images are width-capped so heights stay within the 480px content-image limit: storefront figure max-width 360px → 480px tall; pet figure max-width 390px → 480px tall; price poster column 340px → 425px tall. Hero (landscape) ≈ 350px tall at desktop ≤ 560px cap. Full view wins; no image is cut at any breakpoint.

## Responsive check (CSS audit at 390 / 768 / 1440px — no headless Chromium on this VM)
- 1440: two-column hero (text/photo), 3-col services, 4-col steps, 2-col price cards — all within 1180px wrap, no fixed widths > container, `overflow-x:hidden` on body, `img{max-width:100%}`.
- 960 breakpoint: hero stacks to 1 col; services 1 col; steps 2 col; price cards 1 col; store/pet/poster rows stack; figures centred with their width caps intact.
- 700 breakpoint: nav links hidden (CTAs remain, one ghost CTA hidden to fit), steps 1 col, section padding reduced.
- 390: tables are simple two-column label/value rows that fit 342px content width; buttons wrap (`flex-wrap`) and are inline-block (no fixed width); header brand + one CTA fit via flex with gap; no horizontal scroll triggers found in audit. **Honest caveat:** verified by careful CSS audit only, not a live browser render — parent should eyeball at 390px on deploy.

## Other notes
- Fonts: Fraunces (display) + Inter (body), 2 families, `display=swap`.
- Reveal animations gated behind `.js` (content fully visible without JS); `prefers-reduced-motion` disables all motion.
- Single self-contained `index.html`, relative `assets/` paths only. Footer carries a "Concept preview crafted by Devflix" credit.
- No prices, hours, reviews, ratings or services invented — every fact traces to the JSON or the business's own published price-poster image.

## DM DRAFT (for @the.spinbin)
> Hi! Saw the buzz around your new Bandon store — 100+ likes on the announcement, that's some launch 👏
>
> One thing I noticed: right now the only way to book a home collection is through the CleanCloud widget link in your bio. It works, but it's someone else's page — no services info, no price list, nothing about the two stores.
>
> I mocked up what a proper site for The Spin Bin could look like — services, your full price list, both locations and a direct booking button, all in one place: https://the-cut-co.pages.dev/the-spin-bin-cork/
>
> Built it from your own Instagram photos and price list. If you ever want something like this for real, would you be open to a quick chat about it?
