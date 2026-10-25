# BUILD-NOTES — The Plant Spot NZ (Auckland, New Zealand)

## Result
BUILT — one preview site. Not deployed, no tracker edited, nobody contacted (per task).

Folder: `~/workspace/instagram/lead-campaign/sites/the-plant-spot-nz-auckland/`
- `index.html`
- `images/retail-space.webp`, `images/orchids.webp`, `images/impatiens.webp`, `images/colourful-foliage.webp`
- `BUILD-NOTES.md` (this file)

Preview link for the DM (placeholder, to be live after parent deploys):
`https://jackmax1233-ship-it.github.io/devflix-demos/the-plant-spot-nz-auckland/`

## Facts used (only what the business published)
- Name: The Plant Spot NZ. Instagram: @theplantspot.nz. Location: Auckland, New Zealand (from the brief + post captions tagging #auckland / #aucklandnz).
- Type: indoor plant shop / nursery retail — lush retail displays of potted plants.
- Plants shown in the harvested photos: phalaenopsis orchids (pink/magenta), impatiens (pink/orange), colourful coleus foliage, ranunculus and other flowering potted plants.
- Contact route shown on the site: Instagram DM to @theplantspot.nz only.
- Engagement (from the brief, researcher-supplied): 26 followers; 2026-09-27 retail-space photo 13 likes/1 comment; 2026-09-27 plant showcase reel 9 likes/3 comments; 2026-09-28 orchid carousel 10 likes; 2026-10-03 impatiens reel 4 likes; latest post 2026-10-03.

## Deliberately NOT shown (unverified — never invented)
No street address, no opening hours, no phone number, no prices, no product catalogue with availability, no reviews, no ratings, no delivery/ordering route. The site says plainly that hours/address are not published there and to message on Instagram first. The "In the shop" copy is worded as "recently shared / as posted", not a live catalogue, so it cannot mislead about current stock.

## Gap re-verification (done 2026-10-25 by this builder)
1. **Web search re-run:** "The Plant Spot Auckland plant shop website", exact "theplantspot.nz Auckland plant shop", and "The Plant Spot Auckland indoor plant shop". Results were only DIFFERENT businesses: The Plant Market (permanently closed, theplantmarket.co.nz), The Plant People Ltd (commercial landscaping, theplantpeople.co.nz), Plant & Pot NZ (plantandpot.nz), The Plant Company (Napier), Kings Plant Barn, Church Street Garden Central, and a UK shop (The Plant Place). No website, shop or booking page for The Plant Spot NZ / theplantspot.nz appeared.
2. **Bio-link check — ATTEMPTED, INCONCLUSIVE (read this before DMing):** An unauthenticated fetch of `https://www.instagram.com/theplantspot.nz/` on 2026-10-25 returned a 690 KB generic Instagram shell containing ZERO `biography`, `external_url` or `bio_links` fields and no link-hub URL (no linktr.ee / lnk.bio / beacons / bit.ly). Instagram serves profile content only behind login, so the bio link could NOT be read this way — this is NOT proof that no bio link exists. No website/shop evidence was found anywhere else, so building proceeded, but the parent should eyeball the bio on a signed-in device before sending the DM; if the bio links to a website, shop, Linktree booking hub or booking system for this business, do not send the pitch as written.
3. **Graphics/domain check:** All four harvested thumbnails were inspected visually. None contains baked-in text, a URL, a domain name, a watermark or a logo. No domain to check arose from the graphics. No directory listing for this business was found in the searches above.
4. **India / age check:** Auckland, New Zealand — not India-based. Nothing in the posts indicates an operator under 18; no age is claimed anywhere on the site.

## Photo harvest log (oEmbed route, iPhone UA)
All four oEmbed calls returned `author_name: theplantspot.nz` (match verified) and `author_id: 10054635038`. Thumbnails downloaded with a browser Referer + iPhone UA; all HTTP 200.

| File | Source post | Type | Native size | WebP (q78) |
|---|---|---|---|---|
| retail-space.webp | https://www.instagram.com/p/DdxVOkyhC38/ | photo, 2026-09-27 | 640×853 (3:4) | 109,354 bytes |
| colourful-foliage.webp | https://www.instagram.com/reel/DdyIRrChw8P/ | reel poster, 2026-09-27 | 640×1138 (9:16) | 137,224 bytes |
| orchids.webp | https://www.instagram.com/p/Dd01eiqgRZ4/ | carousel photo, 2026-09-28 | 640×853 (3:4) | 56,620 bytes |
| impatiens.webp | https://www.instagram.com/reel/DeBxKHXBODX/ | reel poster, 2026-10-03 | 640×1138 (9:16) | 71,052 bytes |

- **Reel poster frames / play buttons:** DISCLOSURE — the two reel posters are clean still frames. Visually inspected: NO baked-in play button, no UI overlay, no text on any of the four images. They are used as still photos, not presented as videos.
- No stock or AI photos used. No photo faked or altered beyond WebP conversion at native resolution (sources are 640 px wide, so no upscaling; hero ≤1600 w and content ≤1100 w limits are met trivially).
- 4 usable photos ≥ 3 required — "too thin" threshold not triggered.

## Author ID notes (important for the DM)
- **oEmbed author ID for @theplantspot.nz: `10054635038`** — consistent across all four posts. **Use this one for DM targeting.**
- **instagram-cli numeric ID: NOT obtainable for this target.** `instagram-cli accounts` only returns the operator's own connected account (Devflix: @devfl_ix, fbid 17841415635149093, igid 15752745171). The CLI does not expose another account's numeric ID, and its fbid is Devflix's own — do NOT use it as the target. The two IDs differ because they belong to different accounts; the oEmbed ID is the target's.

## Design
Nursery-specific, not a template: cream paper background (#FAF7EF), deep leaf green (#1C3A28), sand band (#E9E2CF), terracotta accent (#8C3B1F). Fraunces display serif + DM Sans body (Google Fonts, display=swap). No gradients, no glassmorphism, no glowing borders, no decorative icons. Editorial split hero; "In the shop" gallery; "Find us" section that honestly omits hours/address; footer credits photos to @theplantspot.nz.

## Contrast table (WCAG AA, normal text needs ≥ 4.5:1; computed by relative luminance)
| Pair | Ratio | Verdict |
|---|---|---|
| Deep green #1C3A28 on cream #FAF7EF (headings, brand) | 11.64:1 | PASS |
| Body #2E3B26 on cream #FAF7EF | 11.08:1 | PASS |
| Muted #4A5A44 on cream #FAF7EF (captions, notes) | 6.91:1 | PASS |
| White #FFFFFF on deep green #1C3A28 (footer, visit box, ghost-button hover) | 12.46:1 | PASS |
| White #FFFFFF on terracotta #8C3B1F (primary buttons) | 7.61:1 | PASS |
| Deep green #1C3A28 on sand #E9E2CF (gallery section headings/intro) | 9.64:1 | PASS |
| Body #2E3B26 on sand #E9E2CF | 9.18:1 | PASS |
| White #FFFFFF on dark terracotta #5B2D16 (primary-button hover) | 11.46:1 | PASS |
| Terracotta #8C3B1F on cream #FAF7EF (eyebrow label) | 7.11:1 | PASS |

Note: every body-copy, button-label, nav-link, caption and footer pair in the table passes 4.5:1. No text sits over a photo.

## Image-fit audit (full view, no cropping)
- Hero (retail-space, 640×853, 3:4): frame `aspect-ratio: 3/4`, `object-fit: contain`, `max-height: 560px` — the whole shop display is visible; ratio matches the photo exactly, so nothing is cut at any width.
- Gallery cards (all three): `object-fit: contain` on a sand background, `max-height: 340px`, `width: 100%` — orchids, impatiens and foliage are shown whole; the tall 9:16 reel frames letterbox rather than crop. Full view wins over uniform height here by design.
- All images carry `width`/`height` attributes, `max-width: 100%`, `alt` text describing the actual photo content.

## Responsive audit — CSS AUDIT ONLY (no live viewport check possible for this subagent)
Mobile-first single column under 768 px; hero stacks; gallery 1 column → 2 at ≥768 px → 3 at ≥1100 px; `box-sizing: border-box` throughout; no fixed pixel width above 1100 px (wrap max-width 1100 px); all images `max-width: 100%`. No overflow, overlap or clipping is possible from the stylesheet at ~390/768/1440 px widths by construction. This was NOT verified in a live browser viewport — the parent should eyeball it at 390 px before calling it fully verified.

## Relative paths / no-invention check
- All internal links are anchors (`#in-the-shop`, `#find-us`) and all images are relative (`images/*.webp`). No pages.dev / Netlify / GitHub URLs inside the site. Only external links are the Instagram profile (the business's own contact route) and Google Fonts CDN.
- No base64 images in the HTML. No prices, hours, address, phone, reviews or ratings anywhere.

## Opportunity + why a good prospect
An Auckland buyer searching "The Plant Spot" finds only Instagram posts and unrelated similarly-named Auckland plant businesses — there is no page answering "what do they sell, where are they, how do I buy". A single page built from their own photos (the lush shop floor, orchids, impatiens) gives that buyer a reason to message instead of bouncing to Kings or Plant & Pot. Small and real: the shop floor photo shows a genuine stocked retail space, not a dropship page.

## Follower-count honesty note
26 followers is below the usual ~50 ideal — flagged honestly, not padded. What offsets it: the account is a real shop with a real stocked floor, posting consistently through 2026-09-27 to 2026-10-03, with proportional engagement (4–13 likes, up to 3 comments per post). The pitch below does not mention follower count and does not claim popularity.

## DM draft (for parent to send — not sent)
> Hi! I came across The Plant Spot NZ and loved your shop photos — those pink orchids and the shelves full of colourful plants really stood out. I noticed Auckland plant buyers searching for you can only find your Instagram, with nowhere to see what's in the shop in one place, so I put together a simple preview website using your own photos: https://jackmax1233-ship-it.github.io/devflix-demos/the-plant-spot-nz-auckland/
>
> Would a page like that be useful for the shop? Happy to adjust it to however you'd like it.
>
> — Devflix

## Caveats for the parent
1. Bio link UNVERIFIED (login-walled shell — see §Gap re-verification, point 2). Eyeball the bio before sending.
2. Responsive check was CSS-audit only, not a live viewport check.
3. Site not deployed; preview link is a placeholder until deployed to the GitHub Pages demos repo.
4. "Posted September 2026" for the orchids matches the brief's 2026-09-28 carousel date; the other two gallery captions carry no date claim.
