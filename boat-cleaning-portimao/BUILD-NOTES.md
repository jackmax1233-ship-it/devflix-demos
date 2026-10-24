# BUILD NOTES — boat-cleaning-portimao

Preview site for **Boat Cleaning** (@boat_cleaning_), Portimão – Algarve, Portugal.
Preview link placeholder: `https://the-cut-co.pages.dev/boat-cleaning-portimao/`
Built: Fri 23 Oct 2026 (afternoon batch). Build-only — no DMs, no deploy.

## (a) Contrast table (all computed, WCAG AA 4.5:1 normal text)

| Text | Background | Ratio | Pass |
|---|---|---|---|
| #102E2B body ink | #FAF6EC cream | 13.44 | ✓ |
| #43554F muted (lede, captions, section intros, footer) | #FAF6EC cream | 7.34 | ✓ |
| #A95A1A amber (eyebrows, service numbers, tier tags) | #FAF6EC cream | 4.67 | ✓ |
| #0E5B57 teal (ghost buttons, table figures, links) | #FAF6EC cream / #FFFFFF | 7.34 / 7.92 | ✓ |
| #FFFFFF | #0E5B57 teal button | 7.92 | ✓ |
| #FFFFFF | #0C3336 petrol (band, thead, hot tier, contact) | 13.61 | ✓ |
| #FFFFFF | #0F4145 petrol-2 (band cards) | 11.28 | ✓ |
| rgba(255,255,255,.78) (contact meta, hot-tier sub) | #0C3336 petrol | 8.86 | ✓ |
| #E8B44A gold (accents, plan %, phone, band highlight) | #0C3336 petrol | 7.17 | ✓ |
| #0C3336 petrol (gold button label) | #E8B44A gold | 7.17 | ✓ |
| #102E2B ink | #FFFFFF / #FBF8EF (tables) | 14.51 / 13.66 | ✓ |

No large-text-only exceptions used. Palette is solid (no gradients), petrol + sand/cream.

## (b) Image-fit audit

Source ceiling: IG oEmbed thumbnails are 640px wide max. All shown at/below native size.

| File | Natural | Frame | Fit | object-position | Full-view note |
|---|---|---|---|---|---|
| img/hero-catamaran.webp | 640×1138 (0.56, portrait) | portrait frame aspect 640/1138, max-height 520px | cover | center 30% | Full catamaran hull + dock visible in thumbnail; frame matches natural ratio so nothing meaningful is cut |
| img/graphic-ready-to-sail.webp | 640×853 (0.75, portrait) | 640/853 | contain | n/a | Whole poster visible |
| img/graphic-price-table.webp | 640×640 (1.00, square) | 1/1 | contain | n/a | Whole table visible; text legible (see price audit below) |
| img/graphic-boat-care-plans.webp | 640×853 (0.75, portrait) | 640/853 | contain | n/a | Whole plan comparison visible |
| img/work-motorboat-deck.webp | 640×1138 (0.56, portrait) | 640/1138 | cover | center 30% | Deck, bow and marina masts all in frame; frame matches natural ratio |
| img/detail-helm-console.webp | 640×852 (0.75, portrait) | 640/852 | cover | center 40% | Console detail fully visible |
| img/work-stern-marina.webp | 640×1136 (0.56, portrait) | 640/1136 | cover | center 45% | Stern, deck and pontoon fully visible; natural ratio matched |

Photo frames: all ≤ ~340px tall in gallery grid at desktop. Hero photo capped at 520px (≤560px rule). All `<img>` carry width/height attrs and `loading="lazy"` (hero uses `fetchpriority="high"`).

## (c) Fact sources

Every claim traced to the business's own Instagram or the research JSON entry.

- Business name "Boat Cleaning", bio "Professional Boat Cleaning & Maintenance — Portimão – Algarve — Monthly plans & one-off services", WhatsApp +351 927 311 006: IG bio (via instagram-cli `posts` author_bio, 23 Oct 2026) + research JSON bio_facts.
- Services (exterior/interior wash, polishing, wax, teak, upholstery, engine compartment; biodegradable products; monthly plans & one-off): research JSON bio_facts + IG post 2026-06-24 "OUR SERVICES" (https://www.instagram.com/p/DZ-GH7XN0fy/) — Exterior cleaning (hull, decks, windows, finishes); Interior cleaning (saloon, cabins, bathrooms, living areas); Treatment & protection; Dry wash & detailing; Regular maintenance.
- "We take care of your boat as if it were our own": paraphrase of that post's caption ("We take care of your boat as if it were our own").
- Included-in-every-cleaning list: their published price-table graphic (see price audit) — biodegradable nautical wash, glass cleaning, cockpit cleaning, microfibre drying, visual inspection.
- Travel included (Faro, Vilamoura, Albufeira, Portimão, Lagos; other areas on request): price-table graphic + 17 Jul 2026 post caption (https://www.instagram.com/p/Da5TEjcNZ8a/).
- Monthly plans 2×/month −10%, 4×/month −15%, annual weekly service on personalised quote: price-table graphic + caption.
- Boat Care tiers (Essential / Care / Premium) and all checklist items + extra services + "plans personalised by boat size & visits per month": their Boat Care graphic, 27 Sep 2026 post (https://www.instagram.com/p/DdzSiMoxoH6/) — transcription verified at zoom; caption adds photo report after each visit, mooring/equipment checks, small-maintenance coordination, arrival preparation.
- Fountaine Pajot 80 service job, Marina de Portimão: 4 Jun 2026 reel (https://www.instagram.com/reel/DZLkhVXNm_g/, caption "Mais um serviço feito, hoje num Fountaine Pajot 80", tagged Marina de Portimão).
- Gallery captions: satisfied-customer reel 29 Jul 2025 (https://www.instagram.com/reel/DMs4iMVtelV/); console detail from carousel 20 Jun 2025 (https://www.instagram.com/p/DLH_wKdttHY/, tagged Marina de Portimão); stern/marina from appointments reel 14 Feb 2026 (https://www.instagram.com/reel/DUwWtLijTrZ/).
- Follower count 239: research JSON (not displayed on site — irrelevant to customers).
- CTA: WhatsApp wa.me/351927311006 (their published channel — bio says "WhatsApp: +351 927311006"). No fake booking forms.
- NO website (bio link only Linktree): research JSON opportunity_observed — used in DM draft, not on site.

### Price figures — legibility audit (all from the price-table image, post 17 Jul 2026, https://www.instagram.com/p/Da5TEjcNZ8a/)

The 640px thumbnail was viewed at full size plus 2–3× zoomed crops. **Every figure below was clearly legible.** The zoomed extras crop confirmed "Desde" (from) under ALL eight extras rows.

Main services — Exterior wash / Complete wash (exterior + interior):
- Up to 5 m (16 ft): €65 / €105
- 5–7 m (17–23 ft): €85 / €145
- 7–9 m (24–30 ft): €105 / €185
- 9–12 m (31–40 ft): €135 / €245
- 12–15 m (41–50 ft): €185 / €335
- Over 15 m: On quote / On quote ("Sob orçamento")

Extras (all "from" prices):
- Upholstery cleaning from €65 · Teak cleaning from €95 · Stainless & chrome polishing from €55 · Vinyl treatment from €50 · Engine compartment cleaning from €105 · Stain removal from €45 · Protective wax application from €75 · Polishing from €135 · Other services on quote.

Monthly plans: 2 cleanings/month −10% · 4 cleanings/month −15% · Annual weekly service — personalised quote.

Note under table: "Indicative values — the final price may vary with the boat's condition, accessibility and marina." (their footnote, translated).

**No figures were illegible; none were invented.** Structure-only fallback was not needed.

## (d) Photo harvest log

Method: `instagram-cli posts --username boat_cleaning_` (8 posts returned; pagination cursor returned 0 further posts) → public oEmbed per shortcode → author_name verified = boat_cleaning_ on all 8 → CDN thumbnails downloaded with browser UA + Referer (all HTTP 200) → converted to WebP q78.

| Source post | Used as | Included |
|---|---|---|
| https://www.instagram.com/reel/DZLkhVXNm_g/ (Fountaine Pajot 80, 4 Jun 2026) | img/hero-catamaran.webp | yes |
| https://www.instagram.com/p/DZ-GH7XN0fy/ (services poster, 24 Jun 2026) | img/graphic-ready-to-sail.webp | yes |
| https://www.instagram.com/p/Da5TEjcNZ8a/ (price table, 17 Jul 2026) | img/graphic-price-table.webp | yes |
| https://www.instagram.com/p/DdzSiMoxoH6/ (Boat Care plans, 27 Sep 2026) | img/graphic-boat-care-plans.webp | yes |
| https://www.instagram.com/reel/DMs4iMVtelV/ (satisfied customer, 29 Jul 2025) | img/work-motorboat-deck.webp | yes |
| https://www.instagram.com/p/DLH_wKdttHY/ (carousel, 20 Jun 2025) | img/detail-helm-console.webp | yes |
| https://www.instagram.com/reel/DUwWtLijTrZ/ (appointments, 14 Feb 2026) | img/work-stern-marina.webp | yes |
| https://www.instagram.com/reel/DLlGhvYuxkm/ (ready to sail, 1 Jul 2025) | — | NO — thumbnail blurry (throttle-lever close-up, out of focus); excluded for quality |

7 of 8 harvested photos used. No stock, no AI images.

## (e) DM draft (Devflix outreach — NOT sent)

> Hi! Came across your page and your published price table really stood out — most boat cleaners in the Algarve make people DM just to find out what a wash costs, but you've got the full table by boat length right there. Also saw the Fountaine Pajot 80 job at Marina de Portimão — great work.
>
> One thing though: right now that price table lives inside an Instagram post, and all bookings run through WhatsApp/DMs. We built you a quick preview of what a simple website could look like — your services, the real prices, the Boat Care plans, and a WhatsApp quote button, all in one place: https://the-cut-co.pages.dev/boat-cleaning-portimao/
>
> Would you be open to me sending over the details? No pressure either way.

Why it fits: IG-only bookings (bio link is just Linktree, no website — research-verified); the price table is genuinely published but buried in a July post; everything on the preview is their own photos and their own prices.

## (f) Honest shortfalls

1. Thin photo pool (~14 estimated, 8 retrievable via API, 7 usable after excluding one blurry thumbnail). Gallery is 3 photos; hero relies on a reel thumbnail (640px, adequate at display size).
2. No live-browser visual verification — no Chromium on this VM. CSS was audit-checked (breakpoints at 960/860/760/560px, overflow-x hidden on body, tables in horizontal scroll wrappers at 390px, nav collapses to brand + CTA under 760px, hero stacks under 860px). **Recommend a live visual pass at 390/768/1440px before DMs go out.**
3. Copy is English; some of their posts are Portuguese. Boat Care tier names translated from their Portuguese graphic (Essential/Care/Premium are the literal tier names, sub-labels translated: "Inspeção e tranquilidade" → "Inspection & peace of mind" etc.).
4. "Most chosen" style social proof deliberately NOT used — no review/testimonial data exists on their IG.
