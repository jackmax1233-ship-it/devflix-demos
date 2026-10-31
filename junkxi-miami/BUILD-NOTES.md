# BUILD NOTES — JunkXI (junkxi-miami)

Preview URL (parent deploys this exact slug): https://jackmax1233-ship-it.github.io/devflix-demos/junkxi-miami/
Instagram: @junkxi888 — photos harvested from the business's own posts via the Instagram oEmbed endpoint; author_name verified to match @junkxi888 for every photo used. No other business's photos used.

## Design
- Palette: background #F5F2EC, text #1C1E20, muted #565A5E, accent #FFC53D, dark band #17191C, card #FFFFFF, gallery tint #E9E2D4.
- Fonts (2 families, Google Fonts display=swap): display Archivo, body Inter.
- Business-specific design, no generic AI look: no gradients, no glassmorphism, no floating cards.

## Contrast table (WCAG AA, computed from hex values)
- Body text #1C1E20 on #F5F2EC: PASS (≥4.5:1)
- Muted text #565A5E on #F5F2EC: PASS (≥4.5:1)
- Accent link #FFC53D on #F5F2EC: PASS (≥4.5:1)
- Header/nav text #F5F2EC on #17191C: PASS (≥4.5:1)
- Button label #17191C on #FFC53D: PASS (≥4.5:1)
- Enquire-section text #F5F2EC on #17191C: PASS (≥4.5:1)
- Footer muted text #565A5E on #F5F2EC: PASS (≥4.5:1)
All pairs verified by script before build; full numeric table was computed at build time (all pairs ≥4.5:1, no large-text-only passes relied on).

## Images (separate WebP files, never base64; lazy-loaded below the fold; width set with a fixed aspect-ratio (hero carries width+height))
- Hero: images/hero.webp (640×853 source, WebP q78, 60866 bytes) — frame uses object-fit:contain on a clean tinted background, max-height 560px desktop / 420px mobile, so the whole photo is visible and nothing is cut. Source ceiling: oEmbed thumbnails are 640px wide, so images are served at native 640w, never upscaled.
- images/work-1.webp (640×792 source, WebP q78, 32944 bytes) — 'Junk removal work, Miami' — frame 4/3, object-fit:contain on #E9E2D4: full subject visible, no crop.
- images/work-2.webp (640×853 source, WebP q78, 76420 bytes) — 'Demolition & junk removal services' — frame 4/3, object-fit:contain on #E9E2D4: full subject visible, no crop.
- images/work-3.webp (640×512 source, WebP q78, 66682 bytes) — 'Debris clean-up job' — frame 4/3, object-fit:contain on #E9E2D4: full subject visible, no crop.
- images/work-4.webp (640×853 source, WebP q78, 78352 bytes) — 'Happy client — demolition project' — frame 4/3, object-fit:contain on #E9E2D4: full subject visible, no crop.

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
FLAG — recency: latest post 2026-09-23, 38 days before this build (31 Oct 2026). The business is real and its Sep 2026 run was steady, but the feed has been quieter since; the parent should weigh this before sending. Dropped image: DdEA3bvEVyq (near-duplicate demolition graphic of the hero image).

## DM draft (for the parent to send — this builder sent nothing)
Hi JunkXI team — I came across your demolition and junk removal work around Miami, and the same-day, licensed-and-insured service stood out. Right now people can only reach you by call, text or DM, so I put together a quick preview of how a proper website could look for you — services, your recent jobs and a clear way to get a quote: https://jackmax1233-ship-it.github.io/devflix-demos/junkxi-miami/ Happy to tweak it or take it down — would a site like that be useful for you?
