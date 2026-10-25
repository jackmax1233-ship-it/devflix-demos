# BUILD NOTES — Heat Sync Plumbing & Heating

- **Slug:** heatsync-plumbing-edinburgh
- **Business:** Heat Sync Plumbing & Heating — plumbing & heating, Edinburgh (Lothians and Fife), Scotland, UK
- **Instagram:** @heatsync_ph (88 followers at brief time)
- **Built:** Sun 25 Oct 2026, morning batch
- **Status:** Files on disk only. NOT deployed, NO DM sent, NO tracker edited (per task).
- **Preview link (for DM, once deployed):** https://jackmax1233-ship-it.github.io/devflix-demos/heatsync-plumbing-edinburgh/

## Design

- Palette (trade-appropriate, no gradients/glassmorphism): deep navy `#102A43`, body ink `#1A2E3D`, muted slate `#46586A`, warm copper accent `#A84E1C`, warm off-white `#F4EFE8`, pale copper tint `#E8C9A8` (decorative / navy text only).
- Fonts (2 families, Google Fonts, display=swap): Archivo (display/headings) + Inter (body).
- Layout: sticky header, split hero, text service cards, 8-photo recent-work gallery, areas, dark contact section, footer.

## (a) Contrast table (WCAG AA — computed from relative luminance)

| Foreground | Background | Ratio | Verdict |
|---|---|---|---|
| `#FFFFFF` white | `#102A43` navy | 14.64:1 | PASS (normal + large) |
| `#FFFFFF` white | `#1A2E3D` ink | 13.98:1 | PASS |
| `#FFFFFF` white | `#A84E1C` copper (buttons) | 5.57:1 | PASS |
| `#F4EFE8` warm off-white | `#A84E1C` copper | 4.87:1 | PASS |
| `#102A43` navy | `#FFFFFF` white | 14.64:1 | PASS |
| `#102A43` navy | `#F4EFE8` warm | 12.80:1 | PASS |
| `#1A2E3D` ink | `#FFFFFF` white | 13.98:1 | PASS |
| `#1A2E3D` ink | `#F4EFE8` warm | 12.22:1 | PASS |
| `#46586A` muted | `#FFFFFF` white | 7.33:1 | PASS |
| `#46586A` muted | `#F4EFE8` warm | 6.41:1 | PASS |
| `#A84E1C` copper | `#FFFFFF` white (eyebrow text) | 5.57:1 | PASS |
| `#E8C9A8` pale copper | `#102A43` navy (contact sub-labels) | 9.31:1 | PASS |
| `#102A43` navy | `#E8C9A8` pale copper | 9.31:1 | PASS |

- **Contrast pass count: 13/13 pairs pass AA (≥4.5:1 normal text).**
- Note: a lighter copper `#C96A2B` was considered and REJECTED for text (3.89:1 vs navy) — it is not used anywhere.

## (b) Image-fit audit — FULL VIEW

All harvested photos are portrait 640px wide (Instagram oEmbed ceiling). Every image frame uses `aspect-ratio: 4/5`, matching the photos' natural 4:5 ratio, so `object-fit: cover` crops nothing in practice. No face, product or job subject is cut.

| File | Natural size | Frame | Fit | Full-view note |
|---|---|---|---|---|
| `images/radiators-column.webp` (hero + gallery) | 640×800 (4:5) | 4:5, max 448px wide → ≤560px tall | cover (= no crop at 4:5) | Full radiators in frame |
| `images/worcester-boiler.webp` | 640×800 (4:5) | 4:5 gallery | cover (= no crop) | Full boiler in frame |
| `images/shower-leak-repair.webp` | 640×791 (≈4:5) | 4:5 gallery | cover (≤1% edge trim on 791px height) | Enclosure fully visible; negligible trim only |
| `images/toilet-repair.webp` | 640×800 (4:5) | 4:5 gallery | cover (= no crop) | Full toilet in frame |
| `images/shower-towel-rail.webp` | 640×800 (4:5) | 4:5 gallery | cover (= no crop) | Full shower + rail in frame |
| `images/gas-cooker.webp` | 640×800 (4:5) | 4:5 gallery | cover (= no crop) | Full cooker in frame |
| `images/recent-jobs.webp` | 640×800 (4:5) | 4:5 gallery | cover (= no crop) | Full frame |
| `images/recent-jobs-2.webp` | 640×791 (≈4:5) | 4:5 gallery | cover (≤1% edge trim) | Full frame; negligible trim only |

- Size caps: hero ≤560px tall desktop (448px wide × 4:5 = 560px); gallery images ≤~340px tall at desktop 4-column width; mobile gallery switches to 2 columns so images stay moderate and uncropped. All images WebP quality ~78, lazy-loaded except the hero.
- All image paths are RELATIVE (`images/xxx.webp`) — no leading slash, no absolute URLs, no base64 in HTML — so GitHub Pages subpath deploys work.

## (c) Fact sources — every claim traced

| Claim on site | Source |
|---|---|
| Business name, trade (plumbing & heating), Gas Safe trade | Task brief / business bio |
| Area: Edinburgh, Lothians and Fife | Task brief |
| Services: boiler installs/servicing, radiator fitting, shower/toilet/gas-cooker fitting, leak tracing, repairs/installs/maintenance | Task brief + post captions |
| Column radiators fitted (hero + gallery) | Post DecZPNbkSQe caption, 2026-10-13 |
| Worcester 4000 install + Drayton programmer, Honeywell wireless controls, 3-port zone valve, magnetic filter | Post Dc4AVVTiABW caption, 2026-09-04 |
| Shower enclosure leak traced, stripped/cleaned/refitted/resealed (flat below affected) | Post Ddb_Uk3CGvw caption, 2026-09-18 |
| Running toilet: flush valve passing, cistern off, flush + fill valves replaced | Post DdURlDMERhh caption, 2026-09-15 |
| Shower fitted + towel rail installed, left neat and tidy | Post DdOFjASkZhk caption, 2026-09-13 |
| Gas cooker installed and tested | Post DdCL6DiiBmS caption, 2026-09-08 |
| Contact: Heatsyncph@outlook.com; Instagram @heatsync_ph; IG DM link https://ig.me/m/heatsync_ph | Task brief / business bio |
| **Deliberately omitted (not published):** phone number, opening hours, prices, testimonials, ratings, years in business, review counts | Nothing published — nothing invented |

## (d) Photo harvest log — 8/8 attempted, 8/8 harvested

Method: public Instagram oEmbed endpoint with iPhone UA; `author_name` verified = `heatsync_ph` on every post; thumbnails downloaded with browser UA + Instagram Referer; converted to WebP quality ~78 via Python PIL. 640px is the oEmbed ceiling.

| Shortcode | Post date | Caption subject | File | Result |
|---|---|---|---|---|
| DecZPNbkSQe | 2026-10-13 | Column radiators | `images/radiators-column.webp` | OK (640×800) |
| DeB4GD-kSbJ | 2026-10-03 | Another week of jobs | `images/recent-jobs.webp` | OK (640×800) |
| DdgF1_HCLAy | 2026-09-20 | A few recent jobs | `images/recent-jobs-2.webp` | OK (640×791) |
| Ddb_Uk3CGvw | 2026-09-18 | Shower-enclosure leak | `images/shower-leak-repair.webp` | OK (640×791) |
| DdURlDMERhh | 2026-09-15 | Toilet repair | `images/toilet-repair.webp` | OK (640×800) |
| DdOFjASkZhk | 2026-09-13 | Shower + towel rail | `images/shower-towel-rail.webp` | OK (640×800) |
| DdCL6DiiBmS | 2026-09-08 | Gas cooker | `images/gas-cooker.webp` | OK (640×800) |
| Dc4AVVTiABW | 2026-09-04 | Worcester boiler install | `images/worcester-boiler.webp` | OK (640×800) |

- **Shortfall: none on photos.** All 8 shortcodes harvested; no substitutions, no stock/AI imagery.
- Note: the oEmbed `author_id` returned (39341900137) differs from the brief's `author_id` (17841439244137737); `author_name` matched `heatsync_ph` on all 8 posts, which is the verification that mattered.

## Responsive audit (CSS audit — no Chromium on this VM)

- Breakpoints 390 / 520 / 900px: hero stacks to one column, services 3→2→1 columns, gallery 4→2 columns, areas stack, nav collapses to CTA-only on mobile (anchors still reachable by scroll; no hamburger needed for a one-page preview).
- `box-sizing: border-box` everywhere, `max-width: 100%` on images, `overflow-x: hidden` on body — no horizontal overflow expected at 390/768/1440px.
- Reveal animation is gated behind a `.js` class added by the script, so all content is fully visible without JavaScript; `prefers-reduced-motion` disables it.
- **Live visual pass still recommended** at ~390px / ~768px / ~1440px in a real browser before the link is sent, per the build standard.

## (e) Personalized DM draft

> Hi there — I came across Heat Sync on Instagram and really liked how clearly your recent jobs show the work itself, like the column radiators you fitted and the shower leak you traced back and resealed properly instead of just patching over it. I noticed you don't have a website yet, so anyone finding you has to message or email just to see what you do — I put together a simple preview site using your own job photos, with your services, the areas you cover and your Instagram and email front and centre, so new customers in Edinburgh, the Lothians and Fife can see the standard of work before they get in touch. You can have a look here: https://jackmax1233-ship-it.github.io/devflix-demos/heatsync-plumbing-edinburgh/ — would something like that be useful for you?
