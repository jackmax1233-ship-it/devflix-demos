# BUILD NOTES — Amjad Dry Fruit (amjad-dry-fruit-pakistan)

## Business (all facts from the business's own Instagram)
- Business: Amjad Dry Fruit — @amjad.dryfruit, Pakistan (no city stated in bio).
- Followers: 11,987 (verified via instagram-cli profile, 26 Oct 2026). 314 posts.
- Positioning (bio): "Advance payment only", WhatsApp ordering, TikTok link only. No website.
- Gap evidence: NO website. Orders only via WhatsApp/DM; delivery "all over Pakistan" per captions. Nothing searchable to land on.
- Latest post checked: 2026-10-17 (premium bid box) — 9 days before this batch.

## Design
- Identity: pantry warmth. Walnut #2E1B0E + cream #FAF3E7 + pistachio green #5B7040.
- Fonts (2, Google Fonts, display=swap): DM Serif Display (display) + DM Sans (body).
- Layout: split hero, product cards (dry fruits / bid boxes / occasion boxes), photo gallery, dark ordering band, booking section. No gradients, no glassmorphism, no floating cards.
- No prices on the site: deliberately. A June 2026 reel advertised a 10-item deal price, but that price is 4 months old and may have changed — listing it would risk inventing a current price.

## Contrast table (WCAG AA, computed)
| Pair | Ratio | Pass |
|---|---|---|
| White on #2E1B0E (buttons, dark band) | 16.42:1 | AA normal |
| #2E1B0E on #FAF3E7 (body/headings) | 14.88:1 | AA normal |
| #5B7040 on #FAF3E7 (eyebrow accent) | 4.96:1 | AA normal |
| #5A4A3A on #FAF3E7 (captions/footer) | 7.69:1 | AA normal |
| #E8E0D2 on #2E1B0E (dark-band muted text) | 12.53:1 | AA normal |

## Image-fit audit (FULL VIEW gate)
- All 6 photos are the business's own Instagram photos, harvested via public oEmbed (640px ceiling).
- Natural size: 640×850/853 (portrait, ~3:4). Containers use aspect-ratio 3/4 with object-fit: contain — boxes and contents fully visible, nothing cropped.
- Hero max height 540px (under the 560px cap). Gallery frames max 340px tall.
- Files are separate WebP (quality 78) in images/. No base64. No stock/AI imagery.

## Fact sources (post links / IDs)
- Profile: @amjad.dryfruit, user_id 17841467563867773, country PK, bio "Advance payment only", WhatsApp + TikTok links, business website = none.
- https://www.instagram.com/p/DemcZH_DUBL/ — 2026-10-17, "Latest premium Bid Box", 17 likes, 2 comments.
- https://www.instagram.com/p/Dee8einE6tf/ — 2026-10-14, "New born baby Box".
- https://www.instagram.com/p/DeW99WSDdz6/ — 2026-10-11, order box post, 35 likes, 5 comments.
- Product range (from the business's own June 2026 shop reel + recent captions): almonds, pistachios, dried figs, dates, golden raisins, dried mango, walnuts, honey; bid boxes incl. luxury acrylic, latest-design, nikah and dholki boxes.
- Gallery posts: Dd8aw6VjbYT, Dcs1hrMDWyB, DcLOUVIDcTI — all author-verified via oEmbed author_name = amjad.dryfruit.

## Photo-harvest log
- Method: curl iPhone UA to oEmbed; author_name checked = amjad.dryfruit for every image used; CDN thumbnail downloaded with browser Referer + iPhone UA; converted to WebP q78 with PIL (native 640px, no upscaling).

## DM draft
> Hi — I saw your recent premium bid boxes and newborn boxes, and that orders run through WhatsApp with delivery all over Pakistan, but there's no page showing the fruit and boxes together. I built you a preview site with your dry fruits, bid boxes and occasion boxes in one place: https://jackmax1233-ship-it.github.io/devflix-demos/amjad-dry-fruit-pakistan/ — would a page like that make ordering easier for your customers?

## Honest flags
- No city is claimed: the bio gives no city, only Pakistan-wide delivery. The site says "delivered across Pakistan" and nothing more specific.
- No phone number is printed on the site (ordering goes via the WhatsApp number in the bio, as the business routes it); the bio's "advance payment only" line IS stated, since it is the business's own ordering term.
- No prices listed (see Design note — the June deal price was deliberately omitted as stale).
- Responsive audit is CSS-based (mobile-first, stacks at 768px/480px). A live visual pass at 390/768/1440px is still needed before sending — this subagent has no live browser.
