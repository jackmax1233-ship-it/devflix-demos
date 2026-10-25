# Dancebeat Studio — Preview Site Build Notes

- Business: Dancebeat Studio, Glasgow, UK — Instagram @dancebeatstudio1 (author_id 17841448446765236 in brief; oEmbed author_id 48281894892, author_name verified as dancebeatstudio1 on every photo used)
- Followers at brief time: 2,143
- Output folder: `sites/dancebeat-studio-glasgow/` — `index.html` + `images/` (5 WebP files)
- No DM sent. Tracker not edited. (Per task scope.)

## Verified facts used (nothing else invented)

- Established 1999; Glasgow dance studio at 5 Skibo Drive, Glasgow.
- Recreational + competitive training across a range of styles. No specific class styles, times, prices, ages, teachers, reviews or ratings are claimed anywhere on the site — the brief said not to name styles unless a post names them, so the site keeps to "a range of styles".
- GAP (from brief): no own website; bio link is only a Facebook page; captions say "Message us to join" — enquiries via Instagram/Facebook message only. The site's join CTA therefore links to https://www.instagram.com/dancebeatstudio1/
- Recent-post activity in brief: 19 Oct 2026 (84 likes, 13 comments), 14 Oct (87 likes), 11 Oct (31 likes). These counts are NOT displayed on the site (they are not a selling claim).
- Other "Dance Beat" websites found (Stevenage, Hong Kong) belong to different businesses and were NOT used.

## Contrast table (WCAG AA: 4.5:1 normal text, 3:1 large text)

Ratios computed from hex luminance (relative-luminance formula).

| Text | Background | Ratio | Passes |
|---|---|---|---|
| #1A1512 (body/headings) | #FFF6EC (cream page) | 16.94:1 | AA normal ✓ |
| #5A4A3F (muted notes/captions) | #FFF6EC | 7.90:1 | AA normal ✓ |
| #FFFFFF (CTA button label) | #B3001B (red button) | 7.16:1 | AA normal ✓ |
| #FFF6EC (dark-section text) | #141210 (charcoal) | 17.48:1 | AA normal ✓ |
| #FFC53D (yellow display accents) | #141210 (charcoal) | 11.84:1 | AA normal + large ✓ |
| #1A1512 (text on yellow band) | #FFC53D (yellow band) | 11.47:1 | AA normal ✓ |
| #FFFFFF (footer/nav text) | #141210 (charcoal) | 18.69:1 | AA normal ✓ |

No text is placed over a photograph. No purple/blue/pink glowing gradients, no glassmorphism. Palette: cream + charcoal ink + dance-red + poster yellow. Fonts (2 families): Bebas Neue (display) + Inter (body), Google Fonts with display=swap.

## Image-fit audit (FULL VIEW — no dancer/faces cut)

All harvested photos are portrait. No `object-fit: cover` is used anywhere on photos.

| File | Source post | Natural size | Display treatment | Result |
|---|---|---|---|---|
| photo-1.webp | https://www.instagram.com/p/DerJ6GhKEyy/ | 640×791 (portrait) | Hero + gallery, aspect 4/5 frame, `object-fit: contain`, max-height 560px (hero) / 340px (gallery) | Full subject visible; slight letterbox only |
| photo-2.webp | https://www.instagram.com/p/DefCCPUinJK/ | 480×640 (portrait, 3:4) | Gallery, 4/5 frame, `object-fit: contain`, max-height 340px | Full subject visible |
| photo-3.webp | https://www.instagram.com/p/DeW0Y0uqCHD/ | 640×800 (portrait) | Gallery, 4/5 frame, `object-fit: contain`, max-height 340px | Full subject visible |
| photo-4.webp | https://www.instagram.com/p/DeKM8rWCpr4/ | 640×853 (portrait, 3:4) | Gallery, 4/5 frame, `object-fit: contain`, max-height 340px | Full subject visible |
| photo-5.webp | https://www.instagram.com/p/Dd9fhxHqJQZ/ | 640×853 (portrait, 3:4) | Gallery, 4/5 frame, `object-fit: contain`, max-height 340px | Full subject visible |

- Hero media capped at 560px tall on desktop (CSS `max-height:560px`); gallery frames capped at 340px.
- All images are separate WebP files (quality 78, via Pillow), lazy-loaded below the fold (`loading="lazy"`), with width/height attributes. Hero image uses `fetchpriority="high"` and no lazy-load.
- Captions are generic ("Competition celebrations", "Workshop day", etc.) — no dancer or teacher is named on the site.

## Photo harvest log

Method: public Instagram oEmbed (`curl`/Python with iPhone UA + Instagram Referer), `author_name` checked against `dancebeatstudio1`, `thumbnail_url` downloaded (640px ceiling).

| Post | Author check | Result |
|---|---|---|
| DerJ6GhKEyy | dancebeatstudio1 ✓ | Used → photo-1.webp |
| DefCCPUinJK | dancebeatstudio1 ✓ | Used → photo-2.webp |
| DeW0Y0uqCHD | dancebeatstudio1 ✓ | Used → photo-3.webp |
| DePPHPTjMZQ | **albursts ✗** (a third-party post about the studio, not the studio's own post) | **Excluded** — author did not match, per the verification rule |
| DeKM8rWCpr4 | dancebeatstudio1 ✓ | Used → photo-4.webp |
| Dd9fhxHqJQZ | dancebeatstudio1 ✓ | Used → photo-5.webp |

**Photo shortfall: 1 of 6 supplied posts excluded** (DePPHPTjMZQ, author mismatch). 5 verified studio photos used; no stock or AI photos substituted.

## Responsive audit (CSS audit — no live-browser tool available to this builder)

- Mobile-first: single-column base, grid switches to multi-column at ≥700px; gallery drops to 1 column below 400px.
- `img { max-width:100%; height:auto }`, `.wrap { max-width:1100px }`, flex/grid wrapping on nav, no fixed pixel widths on containers.
- Breakpoints checked in CSS: ~390px (1-col gallery, smaller brand), ~768px (2/3-col grids active), ~1440px (max-width container centres content, no overflow).
- Caveat for parent: live-browser verification at 390/768/1440px was NOT possible from this subagent (no live browser); the CSS audit above is the verification performed. Recommend a quick live check before calling the site fully done.

## Verification checklist

- [x] index.html present
- [x] Every image reference resolves to an existing file (5/5 checked)
- [x] 0 base64 strings in index.html
- [x] 0 leading-slash local paths; all image paths relative (`images/*.webp`)
- [x] BUILD-NOTES.md present
- [x] No DM sent, tracker untouched

## DM draft (for parent to send — preview link to be inserted)

> Hi! I came across Dancebeat Studio while looking at dance studios in Glasgow — you've been going since 1999, which really stood out, and I loved seeing your dancers' recent competition and workshop posts.
>
> I noticed you don't have your own website yet, and new dancers currently have to message you to join — so I made you a quick preview of what a proper site could look like, using your own photos: [PREVIEW LINK]
>
> It covers your recreational and competitive classes, your Glasgow studio, and a simple "message us to join" button. No pressure at all — would you like to take a look and tell me what you'd change?
