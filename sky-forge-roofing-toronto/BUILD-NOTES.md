# Sky Forge Roofing — Toronto, Ontario — Preview Site Build Notes

Built: Sun 25 Oct 2026, Devflix afternoon outreach batch.
Folder: `~/workspace/instagram/lead-campaign/sites/sky-forge-roofing-toronto/`
Files: `index.html` + `images/` (6 WebP files). No DM sent, tracker untouched.

## Design
- Palette (roofing trade, no gradients / no glassmorphism): charcoal ink `#16181B`,
  warm paper `#F7F3EC`, secondary paper `#EFE9DD`, rust accent `#9A3412`
  (dark rust `#7C2D12` for links on paper), muted grey `#3F444A`,
  muted-on-dark `#D9D2C4`.
- Fonts (2 families, Google Fonts, display=swap): Fraunces (display serif) + Inter (body sans).
- Layout: editorial — top bar, masthead, split hero, dark feature strip,
  4-column services, 3-column gallery, contact, dark footer. No card-grid clutter
  in the hero; services are plain bordered panels, not floating cards.

## Contrast table (WCAG AA: 4.5:1 normal text, 3:1 large text — all pass)
Ratios computed from the exact hex pairs used:

| Text | On | Ratio | Result |
|---|---|---|---|
| `#16181B` body/headings | `#F7F3EC` paper | 16.08:1 | Pass AA (AAA) |
| `#3F444A` muted body / captions | `#F7F3EC` paper | 8.88:1 | Pass AA (AAA) |
| `#7C2D12` links, eyebrow, service numbers | `#F7F3EC` paper | 9.37:1 | Pass AA (AAA) |
| White `#FFFFFF` button label | `#9A3412` rust button | 7.31:1 | Pass AA (AAA) |
| `#F7F3EC` headings/body | `#16181B` dark sections/footer | 16.08:1 | Pass AA (AAA) |
| `#D9D2C4` muted text | `#16181B` dark sections/footer | 11.83:1 | Pass AA (AAA) |
| `#F7F3EC` on `#7C2D12` (hover button, not used for body text) | — | 8.47:1 | Pass AA |
| Large display headings (Fraunces, 30–64px) exceed the 3:1 large-text bar on every pair above. | | | |

## Image-fit audit (FULL VIEW — container ratio matched to each photo's natural ratio)
All source thumbnails are the Instagram oEmbed 640px ceiling. No `object-fit: cover`
cropping loses subject matter, because every frame's aspect ratio equals the photo's
natural ratio; images are shown whole. No image is stretched or distorted.

| File | Source post | Natural size | Frame | Fit |
|---|---|---|---|---|
| `images/roof-portrait-01.webp` (hero + gallery) | DecVF-8iZ-B | 640×853 (3:4 portrait) | 3:4, max-height 560px desktop | Whole image, no crop |
| `images/roof-metal-02.webp` | DdMtEORiesg | 640×360 (16:9 landscape) | 16:9 | Whole image, no crop |
| `images/roof-portrait-03.webp` | DcjbjxrCTw7 | 640×853 (3:4 portrait) | 3:4 | Whole image, no crop |
| `images/roof-metal-04.webp` | Db8Rnm5DvYb | 640×360 (16:9 landscape) | 16:9 | Whole image, no crop |
| `images/roof-metal-05.webp` | DbyXxeqidEx | 640×360 (16:9 landscape) | 16:9 | Whole image, no crop |
| `images/roof-06.webp` | DbQYpe8jhrF | 640×360 (16:9 landscape) | 16:9 | Whole image, no crop |

- Hero capped at 560px tall on desktop (frame max-height 560px, max-width 420px).
- Gallery frames are moderate (16:9 landscape / 3:4 portrait cards, well under ~340px
  tall at card widths). All below-fold images carry `loading="lazy"`; the hero image
  is eager with `width`/`height` attributes on every image.
- Optimisation: JPEG → WebP, quality 78, 640px wide (source ceiling); total images ≈ 310 KB.
- No base64 images, no stock/AI photos, no absolute/local paths — all image and
  page references are relative (`images/…`, `index.html`).

## Responsive audit (CSS audit, no live browser in this subagent)
- Mobile-first: single column by default; 2-column hero / 2-column grids at ≥768px;
  4-column services and 3-column gallery at ≥1024px.
- All widths fluid (`width:100%`, `max-width`), images `max-width:100%`,
  flex/grid containers wrap (`flex-wrap`, grid reflow), no fixed pixel widths on
  text containers. Header wraps on narrow screens. No horizontal overflow expected
  at ~390px / ~768px / ~1440px. Live-browser check at those widths is still owed
  by the parent (this subagent cannot drive a live browser).

## Fact sources (verified facts only — nothing invented)
- Business: Sky Forge Roofing Ontario, Instagram `@sky_forge_roofing`
  (author_id 17841456453535580 per brief; oEmbed author_id 56524641784 —
  author_name verified as `sky_forge_roofing` on all 6 posts), 356 followers,
  Toronto, Ontario, Canada.
- Services: metal, shingles, flat, standing seam roofing (from brief).
- Feed: 41 posts of finished roofing; engagement 27–57 likes, up to 6 comments.
- Latest post 13 Oct 2026: 12-slide carousel of a completed black standing-seam
  metal roof (57 likes, 6 comments, tagged Mono, Ontario).
- GAP: no website — bio links are only two personal Instagram accounts, no booking
  link, DM-only enquiries.
- Captions are hashtag-only, so site copy leans on photos + stated services only.
  No project locations (other than the tagged Mono, Ontario for the 13 Oct carousel),
  prices, testimonials, reviews, ratings or contact details are claimed anywhere.
- The 13 Oct carousel photo itself was not among the 6 harvested posts, so no gallery
  image is labelled as that specific roof — the feature strip describes it in text
  only, and gallery captions claim only what each post's hashtags support
  (metalwork / metal roofing) or generic "finished roofing".

## Photo harvest log (public oEmbed, 25 Oct 2026)
Method: `curl -A "Mozilla/5.0 (iPhone; CPU iPhone OS 17_0 like Mac OS X)"
"https://www.instagram.com/api/v1/oembed/?url=https://www.instagram.com/p/<POST_ID>/"`,
author_name checked against `sky_forge_roofing` for every post, thumbnail downloaded
with browser Referer/UA. All 6 posts returned usable photos — no shortfall.

| Post | author_name | Result |
|---|---|---|
| https://www.instagram.com/p/DecVF-8iZ-B/ | sky_forge_roofing | OK — hero + gallery |
| https://www.instagram.com/p/DdMtEORiesg/ | sky_forge_roofing | OK — gallery |
| https://www.instagram.com/p/DcjbjxrCTw7/ | sky_forge_roofing | OK — gallery |
| https://www.instagram.com/p/Db8Rnm5DvYb/ | sky_forge_roofing | OK — gallery |
| https://www.instagram.com/p/DbyXxeqidEx/ | sky_forge_roofing | OK — gallery |
| https://www.instagram.com/p/DbQYpe8jhrF/ | sky_forge_roofing | OK — gallery |

## Name-collision note
- `skyforgerf.com` is a DIFFERENT Pacific Northwest firm (Portland / Seattle) — NOT used, NOT linked.
- `skyroofing.ca` and `skyriseroofing.ca` are other Toronto firms — NOT used, NOT linked.
- The footer states this explicitly so a visitor cannot mistake this Toronto business
  for any of them. No domain is claimed for Sky Forge Roofing anywhere on the site.

## DM draft (for the parent to send — NOT sent by this subagent)
> Hi, I came across Sky Forge Roofing while looking at Toronto roofing work — the black standing-seam metal roof you posted on 13 October really stood out, and your feed shows a lot of finished work across metal, shingle, flat and standing-seam jobs.
>
> One thing I noticed: right now people can only reach you through Instagram DM, since your bio links to personal accounts rather than a website. I put together a quick preview site for you using your own photos — it shows your services and finished work in one place so homeowners don't have to dig through the feed to get in touch: [PREVIEW LINK]
>
> Would you be open to a quick look and telling me if anything on it needs changing?

## Verification (run before finishing)
- `index.html` present: yes.
- Every image reference resolves to an existing file: yes (6 references, 6 files).
- Base64 strings: 0. Absolute paths (`src="/…`, `href="/…`): 0.
- `BUILD-NOTES.md` present: yes.
- Open items for parent: live-browser check at ~390px / ~768px / ~1440px; deploy
  (GitHub Pages per current hosting standard) and replace `[PREVIEW LINK]`; then DM.
