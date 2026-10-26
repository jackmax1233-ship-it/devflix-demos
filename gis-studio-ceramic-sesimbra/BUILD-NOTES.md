# BUILD-NOTES — Gis Studio & Ceramic (Sesimbra, Portugal)

## Business
- Name: Gis Studio & Ceramic | Handle: @gisstudioCeramic | Author ID (instagram-cli): 17841446320714805
- Location: Sesimbra, Portugal (IG bio: "Sesimbra.Portugal"; profile country field PT)
- Followers: 529 | Posts: 201 (profile, 26 Oct 2026) | Industry: Pottery/ceramics studio (wild clay)
- Language: site in English; Portuguese terms kept only where the business itself uses them ("barro coletado", "mão, barro, fogo").
- Gap evidence: IG profile website = null; the ONLY bio link is a WhatsApp link (https://wa.me/351969890550) — a messaging link, not a website, per the brief's gate. No own site, no booking page; bio says "visit by appointment". Web search found no own site.
- Activity: latest verified post 21 Oct 2026 (carousel, 49 likes, 3 comments) — within 30 days of 26 Oct 2026. Engagement 8–49 likes on sampled posts; real, consistent with a 529-follower studio.

## Design
- Identity: warm sand background, dark brown ink, iron-clay accent, moss-green contact band (garden-studio feel). Fonts: Cormorant Garamond (display) + Inter (body), Google Fonts display=swap. Distinct from the Solevento site (different display font, palette and layout tone).
- Layout: mobile-first; hero text + full-view image (contain, max-height 540px); gallery images contain, max-height 340px. No horizontal overflow: single-column below 760px, images max-width 100%.

## Contrast table (WCAG AA, computed)
| Pair | Ratio | Verdict |
|---|---|---|
| Ink #2A2118 on cream #F7F2E9 | 14.17:1 | PASS |
| White #FFFFFF on clay-dark #7A3E1D (buttons) | 8.29:1 | PASS |
| Clay-dark #7A3E1D on cream #F7F2E9 | 7.43:1 | PASS |
| White #FFFFFF on moss-dark #3E5A3A (band) | 7.70:1 | PASS |
| Cream #F7F2E9 on ink #2A2118 (footer text) | 14.17:1 | PASS |

## Image-fit audit
- 3 photos used, all the business's own IG photos, 640px, separate WebP files in images/ (no base64, no stock/AI). Hero (Clay & wine gathering, 640x640) contain — full scene visible. Maker-at-work (640x640) contain — full figure and studio interior visible. Wild-clay detail (640x640) contain — full texture subject visible.
- DROPPED after visual check: sky-reflection photo (not work), two wood-fire frames carrying a baked-in video play-button overlay, a sky-only "Céu" photo (not work), a studio-ceiling photo (not work), and a bowl-rim close-up whose bowl is cut by the frame.

## Fact sources (business's own IG only)
- Bio: "Since 2017 / Ceramic by @gislamara / local clay from Azoia & Arrábida / Garden studio & store / ceramic workshop / visit by appointment / Sesimbra.Portugal".
- Posts: https://www.instagram.com/p/DewFpHxjWxU/ (21 Oct 2026, 49 likes); https://www.instagram.com/p/Ddi83g1gGCL/ (21 Sep 2026, "Barro coletado em Azoia & Arrábida"); https://www.instagram.com/p/DbrMWF5jUke/ (5 Aug 2026, "Wood fire + local clay"); https://www.instagram.com/p/DZ9rCYJDUYr/ (24 Jun 2026, "Mão / Barro / Fogo"); https://www.instagram.com/p/DPUkpO7jT6-/ (2 Oct 2025, "Azoia wild clay collection"); birthday-party-in-studio post (22 Oct 2025); "Clay & wine" gathering posts.
- Contact: WhatsApp link wa.me/351969890550 is the business's own published bio link, so it is linked as a button; Instagram profile linked as the second contact route.
- NOT claimed: prices, hours, street address, reviews, catalogue contents beyond what captions describe — none printed.

## Photo-harvest log (26 Oct 2026)
- NOTE: the public oEmbed endpoint returned 403 ("Private media") for these accounts on 26 Oct 2026, so the documented fallback was used: the public post page's og:image (640px CDN file) for each shortcode. Each page's og:description confirmed the author handle, post date and like count matching the instagram-cli post record before download. Downloads used a browser Referer + iPhone UA; files converted to WebP quality 78.
- Carousels yield only their first frame via og:image — noted, not worked around by inventing frames.

## DM draft
Hi — I came across Gis Studio in Sesimbra, especially your wild clay from Azoia and the Arrábida and the wood-fired work you posted recently. Right now someone searching for a ceramics studio in Sesimbra only finds your Instagram, with no page showing the studio, the clay story and how to visit. I built a quick concept site from your own photos so people can see the work and the garden studio in one place: https://jackmax1233-ship-it.github.io/devflix-demos/gis-studio-ceramic-sesimbra/ — would a simple site like that be useful for Gis Studio?

## Honest flags
- Modest account (529 followers); engagement is real (up to 49 likes) and not padded.
- The studio's captions mix Portuguese and English; the site is English-first with the studio's own Portuguese phrases kept intact.
- WhatsApp is the studio's only published contact link; it is shown as a button because the business itself publishes it — no phone number is typed out in site copy beyond that link.
