# BUILD-NOTES — Solevento Studio (Penela, Portugal)

## Business
- Name: Solevento Studio | Handle: @solevento.studio | Author ID (instagram-cli): 17841476483058328
- Location: Penela, Portugal (IG bio: "Penela"; profile country field PT)
- Followers: 76 | Posts: 30 (profile, 26 Oct 2026) | Industry: Pottery/ceramics studio
- Language: site in English; the business posts bilingually (Portuguese + English). Portuguese touches kept only where the business itself uses them ("Workshops de olaria", "estúdio aberta").
- Gap evidence: IG profile website = null, bio_links = [] (instagram-cli profile, 26 Oct 2026). No website, no booking page; captions say "DM me to book your spot". Web search found no own site.
- Activity: latest verified posts 15 Oct 2026 (atelier photo, 7 likes) and 11 Oct 2026 (autumn-morning workshop, 3 likes) — within 30 days of 26 Oct 2026. Small but real engagement, consistent with a 76-follower studio; not padded.

## Design
- Identity: cream clay background, dark brown ink, terracotta accent, deep teal band (echoes the studio's own teal logo colour without copying its poster art). Fonts: Fraunces (display) + Inter (body), Google Fonts display=swap.
- Layout: mobile-first; hero is text + full-view image (contain, max-height 540px); gallery image contain, max-height 340px. No horizontal overflow: single-column below 760px, images max-width 100%.

## Contrast table (WCAG AA, computed)
| Pair | Ratio | Verdict |
|---|---|---|
| Ink #2B2118 on cream #FBF6ED | 14.63:1 | PASS |
| White #FFFFFF on terracotta-dark #8C3B1F (buttons) | 7.61:1 | PASS |
| Terracotta-dark #8C3B1F on cream #FBF6ED | 7.07:1 | PASS |
| White #FFFFFF on teal-dark #1F5A50 (band) | 7.96:1 | PASS |
| Cream #FBF6ED on ink #2B2118 (footer text) | 14.63:1 | PASS |

## Image-fit audit
- 2 photos used, both the business's own IG photos, 640px, separate WebP files in images/ (no base64, no stock/AI). Hero 640x640 contain — full studio shelves visible. Classes poster 640x640 contain — the studio's own announcement graphic; its bottom age line is slightly clipped in the source crop itself (see flag below), so it is used only as a small supporting tile, never as hero.
- DROPPED after visual check: 5 other harvested frames (workshop posters whose text is cut left/right by Instagram's square og crop, and a logo/hours poster). Using them would have shown cut-off text.

## Fact sources (business's own IG only)
- Bio: "Ceramics & pottery workshops • Workshops de olaria / Open studio | Estúdio aberta / Penela / Handmade ceramics > @solevento.ceramics".
- Posts: https://www.instagram.com/p/DehwBPlMgkU/ (15 Oct 2026, atelier); https://www.instagram.com/p/DeW8u8yjAoi/ (11 Oct 2026, "cosy, creative autumn morning… slow down, get your hands in clay"); https://www.instagram.com/p/Dd65B5vjEEY/ (30 Sep 2026, regular art classes); https://www.instagram.com/p/DdrWLAdDDMO/ (24 Sep 2026, weekly ceramic classes in Penela); gift vouchers (Sep 2025 post: "We have gift vouchers for their special days"); "DM me to book your spot" (25 Jun 2026 caption).
- NOT claimed: prices (the studio's posters show €30/€35 workshop prices, but the og crops cut the inclusions lists, so no price is printed on the site), hours, address, reviews — none printed.

## Photo-harvest log (26 Oct 2026)
- NOTE: the public oEmbed endpoint returned 403 ("Private media") for these accounts on 26 Oct 2026, so the documented fallback was used: the public post page's og:image (640px CDN file) for each shortcode. Each page's og:description confirmed the author handle, post date and like count matching the instagram-cli post record before download. Downloads used a browser Referer + iPhone UA; files converted to WebP quality 78.
- Carousels yield only their first frame via og:image — noted, not worked around by inventing frames.

## DM draft
Hi — I came across Solevento Studio in Penela, especially your cosy autumn-morning workshops and that peaceful atelier you posted recently. Right now someone looking for a pottery workshop in Penela only finds your Instagram, with no page showing the studio, the classes and how to book. I built a quick concept site from your own photos so people can see the studio and the workshops in one place: https://jackmax1233-ship-it.github.io/devflix-demos/solevento-studio-penela/ — would a simple site like that be useful for Solevento?

## Honest flags
- Very small account (76 followers, 3–10 likes) — real studio, modest reach; not padded.
- Only 2 photos survived the visual check; the site is deliberately design-led rather than gallery-heavy so no cut-off poster text ships.
- The studio also runs classes for children (its own posts say so); site copy describes "regular art classes" without targeting children directly.
