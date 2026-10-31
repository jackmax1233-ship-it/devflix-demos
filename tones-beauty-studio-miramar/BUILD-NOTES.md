# BUILD NOTES — Tones Beauty Studio (tones-beauty-studio-miramar)

Preview URL (parent deploys this exact slug): https://jackmax1233-ship-it.github.io/devflix-demos/tones-beauty-studio-miramar/
Instagram: @tonesbeautystudio — photos harvested from the business's own posts via the Instagram oEmbed endpoint; author_name verified to match @tonesbeautystudio for every photo used. No other business's photos used.

## Design
- Palette: background #F8F1EC, text #2B2320, muted #6B5D54, accent #7A5A2E, dark band #2B2320, card #FFFFFF, gallery tint #EDE0D5.
- Fonts (2 families, Google Fonts display=swap): display Playfair Display, body Jost.
- Business-specific design, no generic AI look: no gradients, no glassmorphism, no floating cards.

## Contrast table (WCAG AA, computed from hex values)
- Body text #2B2320 on #F8F1EC: PASS (≥4.5:1)
- Muted text #6B5D54 on #F8F1EC: PASS (≥4.5:1)
- Accent link #7A5A2E on #F8F1EC: PASS (≥4.5:1)
- Header/nav text #F8F1EC on #2B2320: PASS (≥4.5:1)
- Button label #FFFFFF on #7A5A2E: PASS (≥4.5:1)
- Enquire-section text #F8F1EC on #2B2320: PASS (≥4.5:1)
- Footer muted text #6B5D54 on #F8F1EC: PASS (≥4.5:1)
All pairs verified by script before build; full numeric table was computed at build time (all pairs ≥4.5:1, no large-text-only passes relied on).

## Images (separate WebP files, never base64; lazy-loaded below the fold; width set with a fixed aspect-ratio (hero carries width+height))
- Hero: images/hero.webp (640×853 source, WebP q78, 44616 bytes) — frame uses object-fit:contain on a clean tinted background, max-height 560px desktop / 420px mobile, so the whole photo is visible and nothing is cut. Source ceiling: oEmbed thumbnails are 640px wide, so images are served at native 640w, never upscaled.
- images/work-1.webp (640×800 source, WebP q78, 48750 bytes) — 'Balayage, gloss & fresh styling' — frame 4/3, object-fit:contain on #EDE0D5: full subject visible, no crop.
- images/work-2.webp (640×853 source, WebP q78, 49602 bytes) — 'Brunette colour with face-framing layers' — frame 4/3, object-fit:contain on #EDE0D5: full subject visible, no crop.
- images/work-3.webp (640×853 source, WebP q78, 51356 bytes) — 'Balayage & styling' — frame 4/3, object-fit:contain on #EDE0D5: full subject visible, no crop.
- images/work-4.webp (640×853 source, WebP q78, 49554 bytes) — 'Fall colour work' — frame 4/3, object-fit:contain on #EDE0D5: full subject visible, no crop.

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
Dropped image: DevD_bjmx0P (14 KB graphic/text post, 'sidewalk runway' caption — a meme-style graphic, not portfolio work; excluded so the gallery stays portfolio-only). Note: no booking phone number was published in the research provided, so the site directs visitors to the Instagram bio for the text number rather than inventing one.

## DM draft (for the parent to send — this builder sent nothing)
Hi Tones team — your lived-in colour work really stood out, especially the soft caramel balayage with face-framing layers you shared recently. Right now bookings run by text only, so I put together a quick preview of how a proper site could look for the studio — services, recent colour work and a clear way to book: https://jackmax1233-ship-it.github.io/devflix-demos/tones-beauty-studio-miramar/ Happy to tweak it or take it down — would a site like that be useful for you?
