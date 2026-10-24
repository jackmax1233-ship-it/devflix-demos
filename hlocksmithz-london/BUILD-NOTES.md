# HLocksmithz — London locksmith preview site — BUILD NOTES

Built: 2026-10-22 ~01:20 PKT (night batch). Deploy target: `https://the-cut-co.pages.dev/hlocksmithz-london/`
All asset paths are RELATIVE (`img/*.webp`, no leading slash) — merges cleanly as a subfolder.

## Photo harvest (SUCCESS — real photos, no stock/AI)
Method: Instagram public oEmbed API `https://www.instagram.com/api/v1/oembed/?url=<post-url>` → `thumbnail_url` (640px CDN), downloaded via curl, converted to WebP q78 with PIL.
- instagram-cli `posts` returned post metadata + captions but NO per-post media URLs (only `profile_picture_url`).
- `/embed/` page and `browser.open` on post URLs are JS/login-walled (no media data).
- oEmbed `thumbnail_url` works and is rate-friendly.

8 photos harvested (all @hlocksmithz's own posts):
| file | size | post | caption basis |
|---|---|---|---|
| img/job-cylinder-keys.webp | 640×853 | https://www.instagram.com/p/DcyT-cAhiOl/ | "Faulty cylinder replaced with new one + 3 keys" (2 Sep) → HERO |
| img/job-deadlocks.webp | 640×853 | https://www.instagram.com/p/DbEalTCCESN/ | "2x 3 lever deadlocks fitted" → service card 01 |
| img/job-thumbturn.webp | 640×853 | https://www.instagram.com/p/Dc_R5l1CMcJ/ | "New thumb turn 60mm euro cylinder fitted" → service card 02 |
| img/job-emergency-call.webp | 640×853 | https://www.instagram.com/p/DceVWKBiJpm/ | "EMERGENCY OUT CALL" → service card 03 |
| img/job-nightlatch.webp | 640×853 | https://www.instagram.com/p/DernK0UiGra/ | "like for like nightlatch fitted" → gallery |
| img/job-door-closer.webp | 640×853 | https://www.instagram.com/p/Dd8ovt9COdc/ | "Adjusted the main entrance door closer" → gallery |
| img/job-garden-gate.webp | 640×853 | https://www.instagram.com/p/DcsodqwiCw9/ | "New garden gate lock fitted" → gallery |
| img/hero-halloween.webp | 640×640 | https://www.instagram.com/p/DetUhyiICM_/ | Halloween promo infographic (AI-generated art, his own post) — ARCHIVED, NOT used on site (real-job-photo policy; gallery kept to genuine job photos). |

All `<img>` carry `width`/`height` attrs, `alt` text, `loading="lazy"` below the fold, `fetchpriority="high"` on hero.

## Contrast audit (WCAG AA, computed 2026-10-22)
Palette: navy #0d1b30 / navy-2 #13263f / ink #16273e / slate #56677b / paper #f7f4ed / white / amber #f2a81d / amber-deep #8f6206.
| fg → bg | ratio | verdict |
|---|---|---|
| #fff → #0d1b30 (hero H1, footer, nav text) | 17.26:1 | AA pass |
| #f2a81d → #0d1b30 (eyebrow, badge, accents on navy) | 8.54:1 | AA pass |
| #d7dee9 → #0d1b30 (hero lede) | 12.75:1 | AA pass |
| #c9d3e0 → #0d1b30 (trustline, hero caption) | 11.41:1 | AA pass |
| #0d1b30 → #f2a81d (amber CTA button label) | 8.54:1 | AA pass |
| #16273e → #f7f4ed (body text) | 13.72:1 | AA pass |
| #56677b → #f7f4ed (secondary text) | 5.28:1 | AA pass |
| #8f6206 → #f7f4ed (kickers, card numbers) | 4.88:1 | AA pass |
| #16273e → #ffffff (card headings) | 15.07:1 | AA pass |
| #56677b → #ffffff (card body text) | 5.80:1 | AA pass |
Fixes applied during build: original amber-deep #c07f0a failed AA-normal (3.04:1 on paper) → darkened to #8f6206 (4.88:1 / 5.36:1); step numbers were #f2a81d on white (2.02:1, FAIL) → switched to amber-deep. All current pairs ≥ 4.5:1.

## Image-fit audit (full-view gate)
- All used photos are portrait 640×853 (3:4). All display frames are `aspect-ratio:3/4` with `object-fit:cover` → frame matches natural ratio, zero subject cropping.
- Hero: max-width 430px → ~573px tall incl. caption; photo itself 430×573… frame capped by max-width; hero section ≈ 490px tall at 1440px (≤560px cap OK).
- Service cards: 3:4 frames, `max-height:340px` (300px mobile) — full-view wins over uniformity; subjects (locks, keys, doors) fully in frame.
- Gallery: 3:4 frames, full subject visible at all widths.
- Verified live in headless Chromium screenshots at 390 / 768 / 1440: no horizontal overflow (fixed a 390px nav-button overflow by hiding nav CTA ≤600px), no overlap, no clipped text, every image shows its full subject. (Screenshots: /tmp/hlock-verify/ — ephemeral.)

## Motion
Scroll-reveal via IntersectionObserver, gated on `.js` class added by script (content fully visible without JS); `@media (prefers-reduced-motion: reduce)` disables transforms/transitions.

## Fact sources (ONLY these published facts used)
- IG bio (via instagram-cli): "TRUSTED and INSURED! Standard lock change overs 🔁 / New lock fitting / keys 🔑 / ** emergency openings** 🚨 / ** DM for more contact info** 🔒 / LONDON". Followers 218.
- Post captions (listed in photo table above). No phone, email, prices, hours, or reviews anywhere — bio explicitly says "DM for more contact info", so all CTAs point to https://www.instagram.com/hlocksmithz/ only.
- Nothing invented. No testimonials. "Trusted & Insured" = his exact bio words.

## Design
Identity: trustworthy tradesman. Fonts: Zilla Slab (slab display) + Inter (body), 2 families, Google Fonts display=swap. Palette: deep navy / amber / slate / warm paper. Custom inline-SVG key logo mark (no raster logo invented). Sections: topbar → sticky nav → hero (portrait job photo) → amber service strip → 3 service cards → recent-jobs gallery → 3-step "one message gets it sorted" → navy CTA → footer.

## Personalized DM draft (~80 words)
author_id: 17841476569516221 (recipient-user-fbids for instagram-messages-cli)

> Hi — I've been following your posts and the nightlatch and cylinder jobs look proper. One observation: you post real work every few days, but it just disappears in the feed — anyone Googling "locksmith London" never sees any of it. I built you a one-page preview site using your own job photos: [PREVIEW LINK]. If you like it, this could live as your permanent site with a quote page so Google searches land somewhere real. Worth a look? — Mudassar, Devflix
