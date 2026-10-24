# BUILD NOTES — E Minor DJ Services (e-minor-dj-services)

Built Fri 23 Oct 2026 · Devflix outreach afternoon batch · build-only (no DMs, no deploys, no contact with the business)
Preview placeholder: https://the-cut-co.pages.dev/e-minor-dj-services/

## (a) Contrast table (computed WCAG ratios — all ≥ 4.5:1, no large-text exceptions needed)

Palette: bg `#15120e` (deep warm charcoal) · surface `#211b14` · ink `#f6efe0` (warm off-white) · muted `#c9b591` · gold `#d9a03c` · gold-soft `#e8b95a`.

| Text | Background | Ratio | Pass |
|---|---|---|---|
| `#f6efe0` body/headings | `#15120e` page bg | 16.31 | ✅ |
| `#c9b591` muted body/captions | `#15120e` page bg | 9.34 | ✅ |
| `#d9a03c` gold eyebrow/links-accents | `#15120e` page bg | 8.04 | ✅ |
| `#e8b95a` gold-soft links/pull-quote/stars | `#15120e` page bg | 10.24 | ✅ |
| `#f6efe0` headings/body | `#211b14` surface (strip, cards, footer band) | 14.89 | ✅ |
| `#c9b591` muted text | `#211b14` surface | 8.53 | ✅ |
| `#d9a03c` gold accents | `#211b14` surface | 7.34 | ✅ |
| `#15120e` dark text on `#d9a03c` gold (availability band, gold buttons) | gold `#d9a03c` | 8.04 | ✅ |

Hover states: gold buttons darken to `#e8b95a` (ratio rises); ghost buttons keep gold-soft text. All states pass AA.

## (b) Image-fit audit (per image — frame ratio matches natural ratio, so `cover` crops nothing)

All thumbnails are Instagram's 640px CDN ceiling; displayed at/below native size (never upscaled).

| File | Natural size/ratio | Frame ratio | Fit | object-position | Full-view note |
|---|---|---|---|---|---|
| `img/hero-dancefloor.webp` | 640×360, 1.78 (16:9) | 16/9 | cover | center | Packed dance floor fully visible; no crop (ratios match) |
| `img/emmett-decks.webp` | 640×427, 1.50 (3:2) | 3/2 | cover | center | Emmett at decks fully visible, head/hands in frame |
| `img/gear-closeup.webp` | 480×480, 1.00 (1:1) | 1/1 | cover | center | Speaker/laptop/mixer fully visible |
| `img/booth-window.webp` | 640×480, 1.33 (4:3) | 4/3 | cover | center | Full booth setup visible |
| `img/barn-ecotay.webp` | 640×480, 1.33 (4:3) | 4/3 | cover | center | Full barn setup, string lights intact |
| `img/elegant-room.webp` | 640×361, 1.77 (16:9) | 16/9 | cover | center | Full room setup visible |
| `img/head-table.webp` | 640×361, 1.77 (16:9) | 16/9 | cover | center | Head table fully visible |
| `img/tent-mississippi.webp` | 640×480, 1.33 (4:3) | 4/3 | cover | center | Full tent/booth/dance-floor visible |
| `img/gazebo-sunset.webp` | 640×427, 1.50 (3:2) | 3/2 | cover | center | Gazebo + full reflection visible |
| `img/oakfield-party.webp` | 640×480, 1.33 (4:3) | 4/3 | cover | center | Full setup + decorated table visible |

Rule applied: since every frame ratio equals the photo's natural ratio, `object-fit: cover` never crops — full subject visible by construction. No image uses `contain`; no decorative-background cropping anywhere.

## (c) Fact sources — every claim traced (nothing invented)

- Business name / IG handle / location / bio quote: his own IG bio, via research JSON `bio_facts` ("Located on the outskirts of the beautiful Ottawa region in Carleton Place. | I am an experienced and professional DJ for all your event needs.").
- Owner-operator **Emmett Minor**: research JSON ("owner-operator Emmett Minor"; reviewers name him).
- **5.0 from 18 reviews on WeddingWire**: research JSON `activity_evidence` + `bio_facts` (WeddingWire.ca directory, named reviewers; named examples **April (Apr 2022)** and **Tori (Jun 2025)** from activity_evidence). Always attributed as WeddingWire; explicit note that reviews are not collected on this site.
- Reviewers mention **wedding DJ + photo booth services**: research JSON `bio_facts` — phrased on site as "Couples on WeddingWire … mention his wedding DJ and photo booth services."
- **Booking 2027–2028 weddings & private events / some holiday party dates still available**: his caption on https://www.instagram.com/p/DeHUgFlmsss/ (Oct 5, 2026 post).
- **Service names + taglines** ("Weddings & Receptions — Your Day, Our Sound", "Holiday Parties — Office Parties, Family Gatherings & More", "Corporate Events — Team Building, Product Launches & Awards", "Birthdays & Anniversaries — Celebrate Life's Special Moments", "Private Gatherings — Reunions, Graduations, & Special Events", "Custom Playlists & Lighting — Set the Perfect Mood") and the H1 tagline **"Your day. Our sound."**: his own promo graphic in the DeHUgFlmsss post (verified visually in the harvested thumbnail).
- **No own website; Facebook page is the real link**: research JSON `bio_facts` (IG website field = facebook.com/pg/eminordjservices/) → used as the site's Facebook link.
- **Venue names** (locks in Perth, Ecotay, Orchard View, Oakfield rugby park, Almonte Old Town Hall, Science and Technology Museum/Ottawa, Timber Run Golf, Maberly Riverhouse): his IG captions (posts CyG1Gc7OqyD, Cw_iP9ZO_gf, CwDewm6uk2Z, C07hGS-uiJG, Cwa_VzbNG4v, Cws4Y1EOnQR, DRm0Ydij59C, Dd1hBqqAQzs).
- **Service-area towns** (Carleton Place, Smiths Falls, Perth, Almonte, Manotick, Ottawa, Lanark County): his hashtags #lanarkweddings #smithsfallsweddings #ottawadj #manotickwedding + captions naming those towns.
- **Gallery captions** (Sarah & Jason / locks in Perth; Teleka & Jonathan; Bridget & Tyler; outdoor wedding on the Mississippi; Marie & Calvin / Orchard View; Oakfield holiday party): his captions on posts CyG1Gc7OqyD, CuaAm6BPW4l, CswssDQvJke, CwYYBdfMi4w, CwDewm6uk2Z, C07hGS-uiJG.
- CTA links: `https://ig.me/m/eminordjservices` (standard IG DM deep link for the handle) and his real Facebook page URL. No booking form (nothing invented to submit to).

## (d) Photo harvest log (all oEmbed-verified `author_name: eminordjservices`)

| # | Post URL | Caption evidence | Used as |
|---|---|---|---|
| 1 | https://www.instagram.com/p/DeHUgFlmsss/ | "Some holiday party dates still available and booking 2027-2028 weddings and private events!" | NOT used as image (text collage) — caption + services facts used |
| 2 | https://www.instagram.com/reel/CoI4ExjMtgB/ | Dance-floor reel (his own @eminordjservices TikTok watermark) | `hero-dancefloor.webp` |
| 3 | https://www.instagram.com/p/CpiA9XVLCa6/ | "Live shot of cueing a 1st dance" | `emmett-decks.webp` |
| 4 | https://www.instagram.com/p/CyG1Gc7OqyD/ | "Ready to go for Sarah and Jason's wedding at the locks in Perth!" | `gear-closeup.webp` |
| 5 | https://www.instagram.com/p/CybvDuFvesT/ | "Looking forward to celebrating with Ariane and Dylan" | `booth-window.webp` |
| 6 | https://www.instagram.com/p/Cw_iP9ZO_gf/ | "Away we go at Ecotay!" | `barn-ecotay.webp` |
| 7 | https://www.instagram.com/p/CuaAm6BPW4l/ | "Ready to go for Teleka and Jonathan's wedding!" | `elegant-room.webp` |
| 8 | https://www.instagram.com/p/CswssDQvJke/ | "Ready to go for Bridget and Tyler!" | `head-table.webp` |
| 9 | https://www.instagram.com/p/CwYYBdfMi4w/ | "What a nice day for an outdoor wedding on the Mississippi!" | `tent-mississippi.webp` |
| 10 | https://www.instagram.com/p/CwDewm6uk2Z/ | "Here at Orchard view ready for Marie and Calvin's wedding!" | `gazebo-sunset.webp` |
| 11 | https://www.instagram.com/p/C07hGS-uiJG/ | "At the Oakfield rugby park ready for a holiday party!" | `oakfield-party.webp` |
| 12 | https://www.instagram.com/reel/Dd1hBqqAQzs/ | "Wonderful wedding at the new Maberly Riverhouse" | NOT used (letterboxed reel cover, 480w, heavy black bars) |

## (e) Personalized DM draft (Devflix outreach — for parent/DM step, not sent)

> Hi Emmett — came across your page and saw you're already booking 2027–2028 weddings with a 5.0 from 18 WeddingWire reviews. That's seriously impressive for an owner-operator.
>
> The gap I noticed: couples searching for a wedding DJ around Ottawa/Lanark find the directory listing, not you — there's no site showing your setups, your services, or which dates are open. I put together a concept preview from your own photos so you can see what that could look like: https://the-cut-co.pages.dev/e-minor-dj-services/
>
> It covers your services, real event photos, the WeddingWire reviews, and a simple "check your date" route into your DMs. Would something like this be useful heading into the 2027–2028 season?
>
> — Mudassar, Devflix

Notes: one genuine observation (booking 2027–2028 + strong reviews yet invisible on Google beyond the directory); why a site helps (services + availability + enquiry route converting wedding demand); preview link placeholder; one low-pressure question. No fake compliments, no invented stats.

## (f) Honest shortfalls

1. **10 of 12 harvested photos used.** Skipped DeHUgFlmsss (text-heavy promo collage — tiny subjects, poor hero material; its *facts* were used) and Dd1hBqqAQzs (reel cover letterboxed with black bars at 480w).
2. **640px CDN ceiling.** oEmbed thumbnails max out at 640w, so the "hero ≤1600w" per-section standard can't be reached; images are displayed at/below native size and never upscaled. Hero shows at ~540px wide max.
3. **Email/domain on his graphic not used.** His Oct 5 promo graphic displays `info@eminordjservices.com` and `eminordjservices.com`, but the brief said no email is published and the domain has no verified live site — left the email off per instructions. Recommend verifying the domain resolves before adding it.
4. **No live visual pass.** No Chromium on this VM: verification was a careful CSS audit (breakpoints 390/768/1024, `overflow-x:hidden` on body, nav collapses to brand+CTA on mobile, sections stack single-column, hero ≈ 420px tall on desktop ≤ 560px cap, all images have width/height + lazy-load below fold, reveal gated behind `.js` so content is fully visible without JS, `prefers-reduced-motion` respected). **Recommend a live check at 390/768/1440px before any DM goes out.**
5. **Crowd energy is thin.** Only the hero shows a real dance floor (from his TikTok repost, carrying his own @eminordjservices watermark); the gallery is setups/venues — that's what his grid offers, so the site is honest about it.
6. Reviews section shows the aggregate + two named reviewers only — no invented review quotes, per the facts-only rule.
