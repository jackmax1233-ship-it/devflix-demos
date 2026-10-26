# BUILD-NOTES — Ty the Tiler (Greenhithe, Kent)
## Business
- Name: Ty the Tiler | Handle: @ty_the_tiler | Author ID (instagram-cli): 17841440866184407
- Location: Greenhithe, Kent; covering Kent, London and Essex (IG bio) | Country: GB
- Followers: 510 | Posts: 94 (profile) | Industry: Tiling (domestic & commercial)
- Gap evidence: IG profile website = null, bio_links = [] (instagram-cli profile, 26 Oct 2026). No website, no booking link — enquiries only via Instagram. Web search found no own site.
- Activity: latest verified post 20 Oct 2026 (instagram-cli post 17917308114261632, shortcode DevrKQKDdc7, little floor repair in Castle Hill) — within 30 days. Sampled likes 9–25, comments 0–3 — real, small-trade scale.
## Design
- Identity: deep teal + warm cream + dark terracotta accent. Fonts: Space Grotesk (display) + Inter (body), Google Fonts display=swap.
- Layout: mobile-first; hero is text + full-view landscape bathroom photo (contain), gallery with per-image natural orientation preserved via contain.
## Contrast table (WCAG AA, computed)
| Pair | Ratio | Verdict |
|---|---|---|
| Cream #F4F1E8 on teal #0F3D3E (dark band) | 10.58:1 | PASS |
| Teal #0F3D3E on cream #F4F1E8 | 10.58:1 | PASS |
| Terracotta-dark #A64A26 on cream #F4F1E8 | 5.12:1 | PASS |
| White #FFFFFF on terracotta #A64A26 (buttons) | 5.79:1 | PASS |
## Image-fit audit
- 6 own IG photos: 4 portrait 640x853, 1 square 640x640, 1 landscape 640x480. Hero max-height 540px contain; gallery max-height 340px contain on a clean card background. No cropping: portrait photos stay portrait, landscape stays landscape. Width/height attributes set; gallery lazy-loaded.
## Fact sources (business's own IG only)
- Bio: "Domestic and Commercial Tiling Service / Greenhithe, Kent / Covering Kent, London and Essex".
- Posts: https://www.instagram.com/p/DevrKQKDdc7/ (little floor repair, Castle Hill, 20 Oct 2026); https://www.instagram.com/p/Dej2JVADdm1/ (60x60 floor, New Bond Street); https://www.instagram.com/p/DegwMpBRZDw/; https://www.instagram.com/p/Dee8o9mkf8d/ (splashback, Grays); https://www.instagram.com/p/DebRmF0kUsi/ (floor tiling project); https://www.instagram.com/p/DeKd70JkVm1/ (terrace, Southend-on-Sea); https://www.instagram.com/p/DbBJtoxDc9G/ (completed bathroom, Meopham — 1200x600 porcelain, waterproof wood-effect wall panelling, per caption).
- NOT claimed: prices, phone, hours, address — none in the bio/captions checked, so the site's contact route is Instagram DM only.
## Photo-harvest log (oEmbed, iPhone UA, 26 Oct 2026)
- All 6 shortcodes returned author_name = ty_the_tiler (match). Thumbnails downloaded with browser Referer/UA, converted to WebP quality 78, separate files in images/.
## DM draft
Hi Ty — your tiling work stood out, especially that Meopham bathroom and the little floor repair in Castle Hill you posted recently. At the moment people can only find that work inside Instagram, with nowhere to land on and see your range. I put together a concept site from your own photos so Kent, London and Essex customers can see the bathrooms, floors and splashbacks in one place: https://jackmax1233-ship-it.github.io/devflix-demos/ty-the-tiler-kent/ — would a simple site like that help you pick up work?
## Honest flags
- No phone/email published by the business, so the site deliberately gives no phone number.
- oEmbed thumbnails are 640px; carousel posts show one frame only.
