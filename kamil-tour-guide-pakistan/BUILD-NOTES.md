# BUILD NOTES — Kamil Tour Guide (kamil-tour-guide-pakistan)

## Business (all facts from the business's own Instagram)
- Business: Kamil Tour Guide / Tour Operator — @kamil_tour_guide, Pakistan (Hunza / Nagar Valley).
- Followers: 379 (verified via instagram-cli profile, 26 Oct 2026). 144 posts.
- Positioning: individual tour guide / tour operator, "Explore Pakistan With Me".
- Gap evidence: NO website and NO bio links at all. Bookings only via Instagram DM / WhatsApp mentioned in captions. Nothing searchable to land on.
- Latest post checked: 2026-10-19 (Winter Tour 2026–2027, bookings open) — 7 days before this batch.

## Design
- Identity: mountain editorial. Deep pine #1E3A2F + parchment #F5F0E6 + muted gold #7A5B21 (accents only).
- Fonts (2, Google Fonts, display=swap): Fraunces (display serif) + Public Sans (body).
- Layout: split hero (text + portrait photo), trek cards, photo gallery, dark "guided by a local" band, booking section. No gradients, no glassmorphism, no floating cards.
- No prices on the site: the business publishes no prices in the checked posts; the site says to ask for a customized itinerary and quotation.

## Contrast table (WCAG AA, computed)
| Pair | Ratio | Pass |
|---|---|---|
| White on #1E3A2F (buttons, dark band) | 12.34:1 | AA normal |
| #1E3A2F on #F5F0E6 (body/headings) | 10.87:1 | AA normal |
| #7A5B21 on #F5F0E6 (eyebrow accent) | 5.53:1 | AA normal |
| #4A4A42 on #F5F0E6 (captions/footer) | 7.87:1 | AA normal |
| #E8E0D2 on #1E3A2F (dark-band muted text) | 9.42:1 | AA normal |

## Image-fit audit (FULL VIEW gate)
- All 6 photos are the business's own Instagram photos, harvested via public oEmbed (640px ceiling).
- Natural size: 640×850/853 (portrait, ~3:4). Containers use aspect-ratio 3/4 with object-fit: contain, so nothing is cropped.
- Hero max height 540px (CSS max-height) — under the 560px cap. Gallery frames max 340px tall.
- Files are separate WebP (quality 78) in images/. No base64. No stock/AI imagery. No other business's photos.
- NOTE: two harvested thumbnails came from the oEmbed endpoint's t39 CDN variant rather than t51; both are the business's own post thumbnails, verified by author_name match (kamil_tour_guide) before download.

## Fact sources (post links / IDs)
- Profile: @kamil_tour_guide, user_id 17841459092105427, country PK, bio "Explore Pakistan With Me", bio_links [].
- https://www.instagram.com/p/DesCtFHh-Pg/ — 2026-10-19, Winter Tour 2026–2027, destinations Islamabad / Skardu / Hunza / Rakaposhi / Fairy Meadow; customized packages, transport, hotels, guidance.
- https://www.instagram.com/p/DeKJ2TpDOxR/ — 2026-10-06, guests from Belgium and Spain incl. YouTuber Enric Luzan at Pissan's Natural Cricket Ground, Rakaposhi Base Camp Trek next.
- https://www.instagram.com/p/DdswQKsjPZw/ — 4 days / 3 nights Rakaposhi & Diran Base Camp Trek from Minapin Village, Nagar Valley.
- Gallery posts: DeOqE_VMKmj, DcDS4yJDnYW, DbwGhzMjttN, DbT5-VijjbL (all author-verified via oEmbed author_name = kamil_tour_guide).

## Photo-harvest log
- Method: curl iPhone UA to instagram.com/api/v1/oembed/?url=<post URL>; author_name checked = kamil_tour_guide for every image used; CDN thumbnail downloaded with browser Referer + iPhone UA; converted to WebP q78 with PIL (no upscaling — native 640px).
- Dropped: none for this business (all 6 harvested images used). Reel-only posts were not used as stills.

## DM draft
> Hi Kamil — I came across your Winter Tour 2026–2027 post and the Rakaposhi Base Camp treks from Minapin, and noticed there's nowhere besides Instagram for someone to land and plan a trip with you. I made you a simple preview site with your treks, destinations and photos in one place: https://jackmax1233-ship-it.github.io/devflix-demos/kamil-tour-guide-pakistan/ — would something like that be useful for your bookings?

## Honest flags
- Small account (379 followers) with modest likes (14 on the latest post, up to 101 on guest posts) — real but small; the guide story (local guide, international guests) is the strength, not reach.
- No city beyond "northern Pakistan / Nagar Valley" is claimed on the site; no phone number is printed (booking goes via the Instagram bio links, as the business itself routes it).
- Responsive audit is CSS-based (mobile-first, stacks at 768px/480px, no fixed widths). A live visual pass at 390/768/1440px is still needed before sending — this subagent has no live browser.
