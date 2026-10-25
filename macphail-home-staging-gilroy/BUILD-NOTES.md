# BUILD NOTES — MacPhail Home Staging & Design (Gilroy, California, USA)

Preview site built: 2026-10-25 (PKT, evening). Built by the site-builder subagent.
No one was contacted. Nothing was deployed. No tracker was edited.

## 1. Facts used (all from the business's own published material — nothing invented)

- Business: MacPhail Home Staging & Design. Founder/operator: Jessica MacPhail.
- Instagram: @macphailhomestagingdesign — business account, 235 followers, 448 following, 12 posts, country US (instagram-cli profile lookup, 2026-10-25 ~23:03 PKT).
- Location: Gilroy, California, USA (profile posts tagged Gilroy, California; bio says Gilroy + South Bay). NOT India-based.
- Operator age check: her own reintroduction post presents her as a wife and mother of three running the business — an adult operator, not under 18.
- Bio line (paraphrased): beautifully staged, strategically marketed; home staging for agents and sellers in Gilroy + South Bay; "book a free consult".
- Contact details as published by the business itself on Instagram: phone (408) 710-6803, email macphailhomestagingdesign@gmail.com, Instagram DM. These are the only contact routes shown on the site — no phone, email, address, hours or prices were invented.
- Services (from the business's own 2026-10-20 packages post, paraphrased):
  - Signature Staging — full staging for a complete home (described for a 3-bed / 2-bath home), 45 days.
  - The Essentials — focused staging of the key main living spaces, 45 days.
  - The Refresh — a styling refresh for a lived-in home, up to 5 hours.
  - Realtor note from the same post: $400 off a first staging project plus a complimentary walk-through. The site states this "as shared on Instagram" — no expiry was stated in the post, so none is claimed.
- No package prices are published by the business, so none appear on the site.
- About section (paraphrased from her 2026-10-16 reintroduction post): Jessica is born and raised in Gilroy; staging grew out of a lifelong love of intentional, beautiful spaces; she works with local realtors, homeowners preparing for a move, and interiors lovers.
- Strongest-engagement post: 2026-10-16 reintroduction carousel (Dekjp0_EpcG) — 97 likes / 22 comments per instagram-cli (the research brief said 96 likes; the live CLI count is 97 — small drift, CLI figure used here).

## 2. Gap re-verification (done by the builder before building)

1. **Bio link check (instagram-cli profile, 2026-10-25):** `website` field is null and `bio_links` is empty. There is NO website link on the profile. The bio's only enquiry route is "book a free consult" + phone — i.e. Instagram/phone only. No services page, portfolio page or enquiry form exists for this business.
2. **Web search "MacPhail Home Staging Gilroy" (2026-10-25):** NO own website found. Results were unrelated: Liz MacPhail Interiors (Austin, Texas — a different business/person), Gilroy real-estate blog posts, and Gilroy property listings. A second search on the handle returned no business website either.
3. **Graphics / domain check:** all 12 harvested thumbnails were visually inspected. NONE contains a URL, domain name or booking link — the logo graphic shows only the business name; the two text graphics show only a greeting and a tagline-style message. No domain is printed anywhere in the business's post graphics.
4. **Directory listings:** no directory listing found that gives this business a website or booking system.
5. **Conclusion: the gap is real.** No working website or booking system for THIS business was found, so building proceeded.

## 3. Photo harvest log (photo gate: PASSED — 12 harvestable, ≥3 required)

Method: public oEmbed endpoint with iPhone UA (`https://www.instagram.com/api/v1/oembed/?url=https://www.instagram.com/p/<POST_ID>/`), then CDN download with browser Referer + iPhone UA. Every oEmbed response returned `author_name: macphailhomestagingdesign`, matching the business handle. oEmbed returns only the FIRST frame of a carousel — later carousel slides were not harvested and are not claimed.

| Post (shortcode) | Type | Date | oEmbed thumb | Author match | Used on site as |
|---|---|---|---|---|---|
| Deu4NFoAZYD | carousel | 2026-10-20 | 640×800 | yes | NOT used (text-heavy graphic; portrait + message duplicate the About section) |
| Dekjp0_EpcG | carousel | 2026-10-16 | 640×800 | yes | about-jessica.webp (About section) |
| DQC1wKqEu4F | carousel | 2025-10-20 | 640×480 | yes | gallery-living-room.webp |
| DPxUco0D5xs | carousel | 2025-10-13 | 640×853 | yes | gallery-bedroom-vaulted.webp |
| DPw20hBkqrz | image | 2025-10-13 | 640×640 | yes | logo.webp (header logo — the business's own logo graphic) |
| DZsdBJ7undw | reel | 2026-06-17 | 640×1138 | yes | gallery-coffee-table.webp |
| DZGGCsjBkku | reel | 2026-06-02 | 640×1136 | yes | hero-bedroom.webp (hero) |
| DY98h0ZPF_7 | reel | 2026-05-30 | 320×567 | yes | gallery-bedroom-light.webp |
| DYpK3ujy5rk | reel | 2026-05-22 | 640×1138 | yes | gallery-kitchen-hutch.webp |
| DXPSXP-CRDA | reel | 2026-04-17 | 640×1136 | yes | gallery-dining-living.webp |
| DW5E3T2Dw_j | reel | 2026-04-08 | 640×1138 | yes | gallery-dining-nook.webp |
| DUyRpvoDiy0 | reel | 2026-02-15 | 640×1137 | yes | gallery-home-office.webp |

- Harvested: 12 photos. Used on site: 11. Not used: 1 (Deu4NFoAZYD graphic).
- **Reel poster frames / play buttons:** all 12 thumbnails were visually inspected. NONE has a baked-in play button — the 7 reel posters are clean still frames of staged rooms. No play-button disclosure is needed on the site.
- **No stock / AI photos used.** Every image on the site is the business's own Instagram photo. Captions describe only the room visible (no invented project names, addresses or client names).
- Conversion: JPEG → WebP, quality 78, native width kept (no upscaling; native max 640w, within the ≤1600w hero / ≤1100w content limits). Total images payload ≈ 576 KB.
- Caveat: `gallery-bedroom-light.webp` (DY98h0ZPF_7) is only 320w natively — it is displayed at gallery width and may look slightly softer than the 640w images. It was kept because it is a genuine staged bedroom; if the parent prefers, it can be dropped without breaking the layout.

## 4. Contrast table (WCAG AA, computed 2026-10-25 — all pairs ≥ 4.5:1)

Palette: cream background #FBF8F3, warm sand #EFE7DB, ink #2A2320, muted #6B5F55, clay #8C4A2F, dark clay buttons #7A3E26, sand text #E8DCCB, white #FFFFFF. No gradients, no glassmorphism, no glowing borders, no decorative icons.

| Text | On background | Ratio | Result |
|---|---|---|---|
| Ink #2A2320 | Cream #FBF8F3 | 14.58:1 | PASS |
| Ink #2A2320 | Sand #EFE7DB | 12.59:1 | PASS |
| Cream #FBF8F3 | Dark #2A2320 | 14.58:1 | PASS |
| Clay #8C4A2F (links, eyebrow) | Cream #FBF8F3 | 6.32:1 | PASS |
| Clay #8C4A2F | Sand #EFE7DB | 5.46:1 | PASS |
| White #FFFFFF (button label) | Dark clay #7A3E26 | 8.25:1 | PASS |
| Muted #6B5F55 (secondary text) | Cream #FBF8F3 | 5.84:1 | PASS |
| Muted #6B5F55 | Sand #EFE7DB | 5.05:1 | PASS |
| Sand text #E8DCCB | Dark #2A2320 | 11.42:1 | PASS |

Every section — header, hero, strip, gallery, packages, realtor note, about, contact, footer, buttons and hover states — uses only pairs from this table. **Contrast result: PASS everywhere.**

## 5. Image-fit audit (full view — no cropping anywhere)

- No `object-fit: cover` is used anywhere. Every image is rendered at its natural aspect ratio (`width: 100%; height: auto` in the gallery, `width: auto` in the hero).
- Hero: portrait photo (640×1136) in a split editorial hero, capped at `max-height: 540px` on desktop (under the ~560px cap). Full bedroom visible, nothing cut.
- Gallery: each figure's frame follows the photo's own orientation — portrait photos in portrait frames, the one landscape photo (640×480 living room) in a landscape frame. No face, product or room is cut.
- About portrait (640×800) and logo (640×640) shown whole.
- All 11 `<img>` tags carry native `width`/`height` attributes (no layout shift).
- **Responsive verification: CSS audit only** (this subagent cannot run a live viewport check — the parent should confirm live at ~390/768/1440 if a viewport pass is required). CSS audit findings: mobile-first single column at ~390px; gallery 2 columns ≥640px, 3 columns ≥1024px; hero stacks on mobile and splits ≥860px; container max-width 1120px; no fixed pixel widths beyond the container; every image has `max-width: 100%`; no horizontal overflow or overlap is possible from the declared rules. Nav wraps on narrow screens.
- Relative paths only: all internal links/images are `images/*.webp` or `#anchors`. No absolute paths, no pages.dev / Netlify / GitHub URLs inside the site. The only external links are Google Fonts (CDN, allowed) and the business's own Instagram profile + tel:/mailto: contact links (its published contact routes).

## 6. Site structure

- Header (business logo + name + nav) → hero ("Beautifully staged. Strategically marketed." — the business's own bio tagline) → audience strip → Recent staging work (8 photos) → Staging packages (Signature / Essentials / Refresh + realtor note) → Meet Jessica → Book a free consult (phone / email / Instagram) → footer with Devflix concept-preview credit.
- Design identity: warm editorial staging look — cream + sand + deep warm brown + clay accent, Fraunces serif display + Inter body. Distinct from other Devflix demos; no generic template styling.

## 7. DM draft (for the parent to send — NOT sent by the builder)

> Hi Jessica! I came across MacPhail Home Staging & Design and loved your reintroduction post — it's clear how much thought you put into making each home feel like home, not just look good in photos. I noticed you don't have a website yet, so right now agents and sellers can only find your work and packages through Instagram. I put together a preview site for you with your staging photos, your three packages and a proper contact section, so a potential client could see the work and book a free consult in one place. Here's a look: https://jackmax1233-ship-it.github.io/devflix-demos/macphail-home-staging-gilroy/ — would something like that be useful for your listings? — Devflix

Notes for the parent: short, natural, personalised (name, Gilroy, the reintroduction post, the packages); states the genuine observation (no website beyond Instagram); no invented results, percentages, audits or claims; one low-pressure question; signed Devflix; placeholder preview link as instructed (link not yet verified live — the parent deploys it).

## 8. Opportunity + why a good prospect

- A real, operating personal-brand staging business (12 posts of genuine staging work, consistent Gilroy/South Bay focus, business account, public phone + email) with a clear, evidenced gap: strong Instagram engagement but no website, no services page, no portfolio page, and no enquiry route beyond Instagram DM/phone.
- The product photographs beautifully — 9 clean staged-room photos made a strong, credible preview without any stock imagery.
- The buyer audience is high-intent (realtors and sellers preparing a listing), so a site that shows work + packages + a consult route directly serves how she already wins work.
- Small follower count (235) is not a weakness here: the business is real, the need is genuine, and the reintroduction post's engagement (97 likes / 22 comments) shows an audience that already responds to her personally.

## 9. Author ID notes (for the parent's DM)

- **instagram-cli numeric author ID: 17841475275621203** (the profile `user_id` and the `author_id` on all 12 posts returned by instagram-cli).
- **oEmbed author ID: 75209629187** (returned by the public oEmbed endpoint for all 12 posts; it also appears as the suffix of the oEmbed `media_id`, e.g. `4009486374285776646_75209629187`).
- The two IDs differ because they come from two different Instagram ID systems (the connected-tooling scoped ID vs the legacy public ID).
- **Parent should use 17841475275621203** whenever a tool or lookup asks for the author's/user ID — it is the ID the connected Instagram tooling consistently returns for this account. The oEmbed ID (75209629187) should only be cited for oEmbed references, not substituted into tooling lookups.

## 10. Files delivered

- `index.html`
- `images/` — 11 WebP files (hero-bedroom, about-jessica, logo, 8 gallery images; see harvest log)
- `BUILD-NOTES.md` (this file)
