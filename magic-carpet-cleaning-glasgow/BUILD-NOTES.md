# BUILD NOTES — Magic Carpet Cleaning, Glasgow

## Business
- **Business:** Magic Carpet Cleaning Scotland — Glasgow, Scotland, UK
- **Instagram:** [@magiccarpetcleaningscotland](https://www.instagram.com/magiccarpetcleaningscotland/) (author_id supplied in brief: 17841458424875605; oEmbed returned author_id 58524843495 for the posts — author_name matched in all 4 cases, which is the check that matters)
- **Followers:** 1,388 (per brief)
- **Gap (per brief):** empty bio, no website, no bio links — booking demand lands only on Instagram. This site therefore has Instagram DM as its only contact route.

## Design
- Palette (trade, not template): deep pine green `#1E3A2F` / darker footer green `#14352A`, warm cream `#F7F3EA`, white cards `#FFFFFF`, warm neutral image backing `#EDE8DB`, brass rule `#C19A3D` used as a decorative border only (never as text).
- Type: Fraunces (display serif, headings) + Inter (body), Google Fonts with `display=swap`. Max 2 families.
- No purple/blue/pink gradients, no glassmorphism, no decorative icon clutter.

## Contrast table (WCAG AA: 4.5:1 normal text, 3:1 large — all pairs pass AA for normal text)
| Text | Background | Ratio | Result |
|---|---|---|---|
| `#F7F3EA` cream on `#1E3A2F` pine (header, nav, dark-section headings/intro, dark buttons) | `#1E3A2F` | 11.15:1 | PASS |
| `#1E3A2F` pine on `#F7F3EA` cream (headings, eyebrow, body headings) | `#F7F3EA` | 11.15:1 | PASS |
| `#1F2421` near-black on `#F7F3EA` cream (body text) | `#F7F3EA` | 14.23:1 | PASS |
| `#3D4A42` muted green-grey on `#F7F3EA` cream (captions, sub-notes) | `#F7F3EA` | 8.40:1 | PASS |
| `#1F2421` on `#FFFFFF` white (service-card text) | `#FFFFFF` | 15.76:1 | PASS |
| `#1E3A2F` on `#FFFFFF` white (service-card headings, prices) | `#FFFFFF` | 12.34:1 | PASS |
| `#F7F3EA` cream on `#14352A` footer green | `#14352A` | 12.06:1 | PASS |
| `#3D4A42` on `#FFFFFF` white (price qualifier "as posted") | `#FFFFFF` | 9.31:1 | PASS |

Ratios computed programmatically from hex values during build. No text is set in brass `#C19A3D`; it is a left-border accent only.

## Image-fit audit (FULL VIEW — no subject cut)
All 4 source photos are portrait. Containers match that orientation instead of forcing a uniform landscape crop:
| File | Source size | Container | Fit | Height check |
|---|---|---|---|---|
| `images/before-after-hero.webp` (hero + gallery) | 640 × 853 (3:4) | aspect-ratio 3/4, `object-fit: contain` on `#EDE8DB` | Full image visible, no crop | ≤ 560 px desktop (hero cap); ≤ 340 px in gallery |
| `images/october-deals.webp` | 640 × 853 (3:4) | aspect-ratio 3/4, `object-fit: contain` | Full image visible, no crop | ≤ 340 px gallery |
| `images/rug-cleaning.webp` | 640 × 853 (3/4) | aspect-ratio 3/4, `object-fit: contain` | Full image visible, no crop | ≤ 340 px gallery |
| `images/before-after-2.webp` | 640 × 816 (~0.78) | aspect-ratio 3/4, `object-fit: contain` | Full image visible; slight neutral letterbox because its ratio is marginally wider than 3:4 — nothing cut | ≤ 340 px gallery |

- `object-fit: cover` is used nowhere. No image is stretched or distorted.
- All images are separate WebP files (quality 78, ≤ 640 px wide — the oEmbed ceiling), relative paths only, `width`/`height` attributes set, below-the-fold images `loading="lazy"`, hero `fetchpriority="high"`.
- Responsive CSS audit: mobile-first, fluid widths, `max-width: 100%` on images, grid collapses 4 → 2 → 1 column (gallery), 3 → 2 → 1 (services), hero stacks on mobile, buttons go full-width ≤ 400 px, media queries at 640 px and 860 px. No fixed pixel widths that could overflow at ~390 px. (Live-browser check at 390/768/1440 px is for the parent to run — this subagent has no live browser.)

## Fact sources (nothing beyond these was used)
- **Glasgow identity, carpet-cleaning trade, 1,388 followers, 417 posts, empty bio / no website:** per the parent brief (verified facts supplied with the task).
- **Latest post, 6 Oct 2026:** https://www.instagram.com/p/DeKtpC1CAYu/ — "Swipe to check out the results … Let's get your carpet in for a freshen up now … October availability ✅". Availability on the site is phrased as "noted in their 6 October post", NOT as current availability.
- **October deals / services + starting prices:** https://www.instagram.com/p/DeFWtNAiuLh/ — "October deals … Carpet cleans from £30 / Sofa cleans from £50 / Mattress cleans from £30 / Hall and stairs cleans from £45 / Availability from Tuesday". Prices on the site are labelled "as posted" and "starting prices … confirm on booking".
- **Rug cleaning:** https://www.instagram.com/p/DdmlJtwCrD5/ — "Some rug cleaning done for Gucci … #glasgow #edinburgh #carpetcleaning #rugcleaning". No rug price was stated, so none is shown — "Price on enquiry".
- **September deals post (gallery only):** https://www.instagram.com/p/DdKN6vgijdt/ — same price list as October; used only as a gallery photo, not as a price source, to avoid presenting superseded deals as current.
- **Account display name from oEmbed:** "Magic professional carpet & upholstery cleaning" — this is what justifies "carpet & upholstery" wording alongside carpet cleaning; sofa/upholstery, mattress, hall & stairs and rug services are all evidenced by the posts above, not invented.
- **NOT included:** no phone number, no street address, no website, no reviews, no ratings, no invented claims — none is published by this account.

## Photo harvest log
- Method: public Instagram oEmbed, `curl`/Python with iPhone UA, per `~/TOOLS.md` note. `author_name` verified as `magiccarpetcleaningscotland` for all 4 posts before download.
- Thumbnails downloaded with browser Referer/UA (640 px ceiling), converted to WebP quality 78 with Pillow.
- **Shortfall: NONE — 4 of 4 posts yielded a usable photo.** No stock or AI photos used.

| Post | File | oEmbed title (abridged) |
|---|---|---|
| DeKtpC1CAYu | before-after-hero.webp | October availability / freshen up |
| DeFWtNAiuLh | october-deals.webp | October deals price list |
| DdmlJtwCrD5 | rug-cleaning.webp | Rug cleaning |
| DdKN6vgijdt | before-after-2.webp | September deals price list |

## Name-collision note
Other UK businesses use a similar name (the brief flags an Aberdeen business and a London business). **None of their facts, prices or links were used or visited for this site.** The site is branded throughout as "Magic Carpet Cleaning — Glasgow", links only to @magiccarpetcleaningscotland, and the footer carries an explicit note that this preview is for the Glasgow Instagram business only.

## Verification (run before finishing)
- `index.html` present (13 KB); all 4 image references resolve to existing files; 0 base64 strings; 0 absolute/local paths (only relative `images/…`, `#…` anchors and `https://` links, including Google Fonts); `BUILD-NOTES.md` present.
- No DM sent. Tracker not edited. (Per task.)

## DM draft (for the parent to send — [PREVIEW LINK] to be filled in)
> Hi, I came across your page while looking at carpet cleaners in Glasgow — your before-and-after posts really show the difference a clean makes, and I noticed you don't currently have a website, so anyone wanting to book has to come through Instagram.
>
> I put together a simple preview website for Magic Carpet Cleaning Glasgow using your own photos and your October deals, so people searching for a carpet cleaner in Glasgow can find you and message you to book: [PREVIEW LINK]
>
> Would you be open to having a quick look and telling me what you'd change?
