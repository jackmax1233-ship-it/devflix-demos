# BUILD NOTES — Tours By Abrar (tours-by-abrar-pakistan)

## Business (all facts from the business's own Instagram)
- Business: Tours By Abrar Khawaja — @toursby_abrar, Pakistan.
- Followers: 3,986 (verified via instagram-cli profile, 26 Oct 2026). 238 posts.
- Positioning (bio): "Unique PREMIUM tours in PAKISTAN — Customized • Corporate • Honeymoon • Solo; Adventure • Hiking • Luxury Tours".
- Gap evidence: NO website. Bio links = WhatsApp only. Bookings via WhatsApp/DM; nothing searchable to land on.
- Latest post checked: 2026-10-25 (Autumn 2026 group trip) — 1 day before this batch.

## Design
- Identity: premium expedition. Dark slate-teal #16211F + sand #EFE7D8 + muted gold #7A5B21.
- Fonts (2, Google Fonts, display=swap): Marcellus (display) + Jost (body).
- Layout: split hero, three tour-type cards, photo gallery, dark premium band, booking section. No gradients, no glassmorphism, no floating cards.
- No prices on the site: the business publishes no package prices in the checked posts/captions.

## Contrast table (WCAG AA, computed)
| Pair | Ratio | Pass |
|---|---|---|
| White on #16211F (buttons, dark band) | 16.52:1 | AA normal |
| #1C2B2A on #EFE7D8 (body/headings) | 11.97:1 | AA normal |
| #7A5B21 on #EFE7D8 (eyebrow accent) | 5.11:1 | AA normal |
| #4A4A42 on #EFE7D8 (captions/footer) | 7.28:1 | AA normal |
| #E8E0D2 on #16211F (dark-band muted text) | 12.60:1 | AA normal |

## Image-fit audit (FULL VIEW gate)
- All 6 photos are the business's own Instagram photos, harvested via public oEmbed (640px ceiling).
- Natural size: 640×853 (portrait, ~3:4). Containers use aspect-ratio 3/4 with object-fit: contain — nothing cropped.
- Hero max height 540px (under the 560px cap). Gallery frames max 340px tall.
- Files are separate WebP (quality 78) in images/. No base64. No stock/AI imagery.
- DROPPED, deliberately: post DeuVhttjY2z (oEmbed returned no thumbnail/author — unusable) and post DekwbqBjLlS (oEmbed author_name = harisyousufzai, NOT toursby_abrar — another account's post, never used as Abrar's photo).

## Fact sources (post links / IDs)
- Profile: @toursby_abrar, user_id 17841474970605326, country PK, bio as above, bio_links = WhatsApp only, business website = none.
- https://www.instagram.com/p/De7YJpxCv2L/ — 2026-10-25, "Glimpse from ongoing Autumn 2026 Group Trip".
- https://www.instagram.com/p/DeygN1Liun1/ — 2026-10-22, "Ongoing Autumn 2026 Skardu/Hunza Group trip!".
- https://www.instagram.com/p/DertCAxK5II/ — horse riding at Sarfaranga desert.
- Gallery posts: De7M2cQCpuC, DePTKl0GLEM ("Explore North Pakistan with me!"), DeCr3WFCtkA ("Shigar nowadays") — all author-verified via oEmbed.

## Photo-harvest log
- Method: curl iPhone UA to oEmbed; author_name checked = toursby_abrar for every image used; CDN thumbnail downloaded with browser Referer + iPhone UA; converted to WebP q78 with PIL (native 640px, no upscaling).

## DM draft
> Hi Abrar — I saw your Autumn 2026 Skardu/Hunza group trip posts and that you run premium customized tours, and noticed bookings run through WhatsApp with no site to show the trips on. I built you a preview site with your tour types, destinations and trip photos in one place: https://jackmax1233-ship-it.github.io/devflix-demos/tours-by-abrar-pakistan/ — would a page like that help people choose and book a tour with you?

## Honest flags
- "Premium" is the business's own bio wording, kept as-is; no premium claim is invented by us.
- No prices, dates or inclusions are listed — none were published in the checked captions.
- Responsive audit is CSS-based (mobile-first, stacks at 768px/480px). A live visual pass at 390/768/1440px is still needed before sending — this subagent has no live browser.
