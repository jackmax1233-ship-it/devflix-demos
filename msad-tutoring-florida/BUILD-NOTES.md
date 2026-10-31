# BUILD NOTES — MSAD Tutoring (msad-tutoring-florida)

Preview URL (parent deploys this exact slug): https://jackmax1233-ship-it.github.io/devflix-demos/msad-tutoring-florida/
Instagram: @msadtutoring — photos harvested from the business's own posts via the Instagram oEmbed endpoint; author_name verified to match @msadtutoring for every photo used. No other business's photos used.

## Design
- Palette: background #FFFBF2, text #123C40, muted #5C665F, accent #B03A24, dark band #0F5257, card #FFFFFF, gallery tint #E4EFEA.
- Fonts (2 families, Google Fonts display=swap): display Fraunces, body Nunito Sans.
- Business-specific design, no generic AI look: no gradients, no glassmorphism, no floating cards.

## Contrast table (WCAG AA, computed from hex values)
- Body text #123C40 on #FFFBF2: PASS (≥4.5:1)
- Muted text #5C665F on #FFFBF2: PASS (≥4.5:1)
- Accent link #B03A24 on #FFFBF2: PASS (≥4.5:1)
- Header/nav text #FFFFFF on #0F5257: PASS (≥4.5:1)
- Button label #FFFFFF on #0F5257: PASS (≥4.5:1)
- Enquire-section text #FFFFFF on #0F5257: PASS (≥4.5:1)
- Footer muted text #5C665F on #FFFBF2: PASS (≥4.5:1)
All pairs verified by script before build; full numeric table was computed at build time (all pairs ≥4.5:1, no large-text-only passes relied on).

## Images (separate WebP files, never base64; lazy-loaded below the fold; width set with a fixed aspect-ratio (hero carries width+height))
- Hero: images/hero.webp (640×853 source, WebP q78, 109132 bytes) — frame uses object-fit:contain on a clean tinted background, max-height 560px desktop / 420px mobile, so the whole photo is visible and nothing is cut. Source ceiling: oEmbed thumbnails are 640px wide, so images are served at native 640w, never upscaled.
- images/work-1.webp (640×842 source, WebP q78, 42406 bytes) — 'Figurative-language lesson' — frame 4/3, object-fit:contain on #E4EFEA: full subject visible, no crop.
- images/work-2.webp (640×853 source, WebP q78, 35058 bytes) — 'Word parts: prefixes, roots and suffixes' — frame 4/3, object-fit:contain on #E4EFEA: full subject visible, no crop.
- images/work-3.webp (640×718 source, WebP q78, 82146 bytes) — 'Learning beyond the desk' — frame 4/3, object-fit:contain on #E4EFEA: full subject visible, no crop.
- images/work-4.webp (640×853 source, WebP q78, 61290 bytes) — 'Celebrating the school community' — frame 4/3, object-fit:contain on #E4EFEA: full subject visible, no crop.

## Image-fit audit
- Hero: object-fit:contain on a clean tinted background with max-height 560px desktop / 420px mobile — the whole photo stays visible at desktop and mobile widths (contain, not cover, so text graphics are never clipped).
- Gallery: uniform 4/3 frames with object-fit:contain on a clean tinted background — the whole photo (faces, hair work, stationery, job scenes) stays visible; no cropping. This satisfies the full-view gate over uniform-frame uniformity.
- No faces, products or work are cut in any image.

## Fact sources (only published facts used; nothing invented)
- Services, positioning, service area and contact channel: research file batch-afternoon-31oct-USCA-EAST.json (from the business's Instagram bio and post captions) — see that file for the per-business published_facts.
- Gallery captions: from the businesses' own post captions/titles returned by oEmbed.
- NOT on the site (because not published): no prices, no opening hours, no reviews, no ratings, no invented services.
- Enquiry channel: only the channel the business itself states (see Enquire section on the page).

## Flags
FLAG — size: 44 followers, just under the usual ~50 floor; kept because engagement is real (e.g. 48 likes / 14 comments on the 4 Sep 2026 post) and posting is several times a week through 29 Oct 2026. Dropped image: DfAHVZDxHMe (Thanksgiving-break closure notice — a dated announcement, not evergreen site material).

## DM draft (for the parent to send — this builder sent nothing)
Hi — I saw your figurative-language and word-parts lessons for grades 1–8, and the lovely parent engagement on your posts. Right now families can only reach you through a form link and DMs, so I put together a quick preview of how a simple website could look for MSAD Tutoring — subjects, how sessions work and a clear way to enquire: https://jackmax1233-ship-it.github.io/devflix-demos/msad-tutoring-florida/ Happy to change anything or take it down — would a site like that help parents find you?
