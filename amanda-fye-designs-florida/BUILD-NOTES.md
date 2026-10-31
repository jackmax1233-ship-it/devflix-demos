# BUILD NOTES — Amanda Fye Designs (amanda-fye-designs-florida)

Preview URL (parent deploys this exact slug): https://jackmax1233-ship-it.github.io/devflix-demos/amanda-fye-designs-florida/
Instagram: @amandafyedesigns — photos harvested from the business's own posts via the Instagram oEmbed endpoint; author_name verified to match @amandafyedesigns for every photo used. No other business's photos used.

## Design
- Palette: background #FAF6EF, text #2E2620, muted #6E6259, accent #9C4A2F, dark band #2E2620, card #FFFFFF, gallery tint #EFE6D8.
- Fonts (2 families, Google Fonts display=swap): display Cormorant Garamond, body Jost.
- Business-specific design, no generic AI look: no gradients, no glassmorphism, no floating cards.

## Contrast table (WCAG AA, computed from hex values)
- Body text #2E2620 on #FAF6EF: PASS (≥4.5:1)
- Muted text #6E6259 on #FAF6EF: PASS (≥4.5:1)
- Accent link #9C4A2F on #FAF6EF: PASS (≥4.5:1)
- Header/nav text #FAF6EF on #2E2620: PASS (≥4.5:1)
- Button label #FFFFFF on #9C4A2F: PASS (≥4.5:1)
- Enquire-section text #FAF6EF on #2E2620: PASS (≥4.5:1)
- Footer muted text #6E6259 on #FAF6EF: PASS (≥4.5:1)
All pairs verified by script before build; full numeric table was computed at build time (all pairs ≥4.5:1, no large-text-only passes relied on).

## Images (separate WebP files, never base64; lazy-loaded below the fold; width set with a fixed aspect-ratio (hero carries width+height))
- Hero: images/hero.webp (640×853 source, WebP q78, 60618 bytes) — frame uses object-fit:contain on a clean tinted background, max-height 560px desktop / 420px mobile, so the whole photo is visible and nothing is cut. Source ceiling: oEmbed thumbnails are 640px wide, so images are served at native 640w, never upscaled.
- images/work-1.webp (640×853 source, WebP q78, 80260 bytes) — 'Recent stationery work' — frame 4/3, object-fit:contain on #EFE6D8: full subject visible, no crop.
- images/work-2.webp (640×853 source, WebP q78, 46962 bytes) — 'Reception pieces — wedding at Armature Works, Tampa' — frame 4/3, object-fit:contain on #EFE6D8: full subject visible, no crop.
- images/work-3.webp (640×853 source, WebP q78, 58936 bytes) — 'Reception pieces — Armature Works, Tampa' — frame 4/3, object-fit:contain on #EFE6D8: full subject visible, no crop.
- images/work-4.webp (640×853 source, WebP q78, 77664 bytes) — 'Paige & Alex — day-of details' — frame 4/3, object-fit:contain on #EFE6D8: full subject visible, no crop.

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
Dropped image: DeupgCZH1vL (second Paige & Alex post, near-duplicate of the gallery's Paige & Alex detail photo). Design kept distinct from the Ireland wedding-stationery site built in parallel: different palette (ivory/terracotta vs the other build), different type pairing (Cormorant Garamond + Jost) and an editorial layout.

## DM draft (for the parent to send — this builder sent nothing)
Hi Amanda — I loved the letterpress invitations on double-thick cotton you shared recently, and the reception pieces for the Armature Works wedding. Right now couples only find you through a link-in-bio, so I put together a quick preview of how a proper portfolio site could look — invitations, signage and reception work in one place: https://jackmax1233-ship-it.github.io/devflix-demos/amanda-fye-designs-florida/ Happy to adjust anything or take it down — would a site like that help couples find you?
