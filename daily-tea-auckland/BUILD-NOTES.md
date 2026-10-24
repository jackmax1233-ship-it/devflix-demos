# BUILD NOTES — Daily Tea NZ preview (daily-tea-auckland)

## Source
- Business: Daily Tea, Instagram **@dailyteanz**, author_id **17841445756305482**
- Location: Auckland, New Zealand — Henderson + Birkenhead
- Followers: 1,193 (at research time, 2026-10-22)
- Research file: `~/workspace/instagram/lead-campaign/research/batch-night-22oct-AUNZ.json` (rank-3 qualified candidate)
- Site deploy target (by outreach batch, not this task): https://the-cut-co.pages.dev/daily-tea-auckland/ — relative asset paths only.

## Photos (all THEIR OWN Instagram photos, downloaded via signed CDN URLs from instagram-cli post records + hatch-zeitgeist raw)
| file | source post | subject | size (orig) | size (WebP q78) |
|---|---|---|---|---|
| img/hero.webp | https://www.instagram.com/p/DeQ4EofpUUD/ (2026-10-08) | 1L Bucket promo — Three Brother Milk Tea & Fruity Green Tea | 1350x1688 | 900x1125, 44 KB |
| img/pistachio.webp | https://www.instagram.com/p/DdqTJC9iRax/ (2026-09-24) | Pistachio Limited Series — 4 drinks w/ prices | 1080x1350 | 800x1000, 46 KB |
| img/snack.webp | https://www.instagram.com/p/DdGXTMMJdPu/ (2026-09-10) | $7 Daily Snack — 6 items w/ prices | 1885x2514 | 800x1066, 69 KB |
| img/mochi.webp | https://www.instagram.com/p/DYEe4FmCbOE/ (2026-05-08) | Cloudy Mochi series — Oreo, Biscoff, Pearls | 1885x2514 | 800x1066, 50 KB |
| img/matariki.webp | https://www.instagram.com/p/DakJVNGJha8/ (2026-07-09) | Matariki Day 9% off poster | 1350x1687 | 700x874, 80 KB |
| img/egg-cake.webp | https://www.instagram.com/p/CuGSu7oyS0-/ (2023-06-29) | Egg cake pop-up + Mango Sago (w/ @morninggoogoo) | 1440x1800 | 800x1000, 65 KB |
- No stock, no AI images. No base64. `loading="lazy"` below the fold; `fetchpriority="high"` + width/height attrs on hero.
- All 6 images used on-page (hero.webp is reused in the 1L Bucket drink card). Original high-res JPGs were deleted after conversion; sources documented above.

## Image-fit audit (full-view gate)
- ALL promo images carry text/prices at their edges → full view is mandatory; cover-cropping is not allowed.
- Frames match each image's natural orientation exactly: hero/pistachio/matariki/egg-cake = aspect-ratio 4/5; snack/mochi = aspect-ratio 3/4; object-fit: cover on a same-ratio frame → zero cropping.
- Hero: max-height 560px (portrait frame ~448px wide at cap). Card images: portrait frames (max ~340px wide on desktop) — full-view gate supersedes the 340px card-height guideline (AGENTS.md: full view wins over uniform frames).
- Alt text describes subject + visible pricing for accessibility.

## Contrast audit (WCAG AA, computed with sRGB relative-luminance script)
Palette: --cream #FBF6EA · --ink #2A331E · --matcha #3F6B24 · --matcha-deep #2E521A · --taro #6B2FA0 · --soft #5C6647 · --pink #C43D7C
| pair | ratio | verdict |
|---|---|---|
| ink on cream (body text) | 12.24 | PASS |
| white on matcha (buttons) | 6.29 | PASS |
| white on matcha-deep (button hover) | 8.98 | PASS |
| matcha on cream (kick­ers/nav?) | 5.83 | PASS (matcha-deep used for kickers: 8.33 PASS) |
| taro on cream (em-headings, series labels) | 7.67 | PASS |
| cream on ink (marquee, visit, footer) | 12.24 | PASS |
| soft on cream (secondary text) | 5.65 | PASS |
| white on taro | 8.27 | PASS |
| pink — not used for text | — | — |
All text pairs ≥ 4.5:1 (large-text ≥ 3:1 also covered).

## Fact sources (only published facts; nothing invented)
- Bio (via instagram-cli post record): "Opening hours: 11am - 8pm"; "385 Great North Road, Henderson 0204352320"; "13A Mokoia Road, Birkenhead 02040328384".
- Post captions (hatch-zeitgeist raw): 1L bucket flavours & customisation ("choose your tea base + 5 toppings"); Pistachio series names; Cloudy Mochi free-w/-$15+ Mother's Day (dates 09/05–10/05, presented WITHOUT the expired promo mechanics in-page); Daily Snack availability at both stores; egg-cake/Night Market collab with @morninggoogoo.
- Prices (as printed in the business's own post images): 1L Three Brother Milk Tea $10, 1L Fruity Green Tea $12; Pistachio Cocoa Cream / Sea Salt Latte / Coconut Matcha $8.50, Pearl Jasmine MT $8; all Daily Snacks $7.
- NOT published / NOT claimed: full menu, delivery/online ordering, email, days of week for hours, reviews/ratings.

## Motion
- Scroll reveal via IntersectionObserver on `.js`; content visible without JS; `prefers-reduced-motion` disables reveal, marquee and transitions.

## Responsive check (headless Chromium / Playwright, verified 2026-10-23)
- 390 / 768 / 1440px: `document.documentElement.scrollWidth == innerWidth` (no page-level overflow or overlap) at all widths. The only out-of-viewport elements are marquee separators inside the overflow:hidden ticker (by design).
- Full-view images: frames match each image's natural ratio (4/5 for hero/pistachio/matariki/egg-cake; 3/4 for snack/mochi) — promo text/prices never cropped. All images lazy-load correctly; zero broken images after scroll-through.
- Hero image height: 432px (390) / 538px (1440) — within the ≤560px cap.
- Two contrast/visual fixes applied after screenshot review: (1) `.snack-item span` was overriding `.price-pill` white text (specificity bug → grey text on green); added guard `.snack-item .price-pill{color:#fff}`, verified white via computed style. (2) Hero tag pill overlaid the promo image's own price text — moved below the image as a caption.
- Reveal-on-scroll verified per section at 390px (drinks/snacks/moments/visit all reveal on scrollIntoView); content visible without JS (reveal gated on .js class).

## DM draft (~80 words, outreach batch to send; [PREVIEW LINK] = deployed URL)
Hi Daily Tea team! I spotted your 1L buckets and that Pistachio Limited Series on your grid — beautiful drinks, but people Googling "bubble tea Henderson / Birkenhead" only find directory pages, never you. I made you a free one-page concept site with your menu prices, the $7 Daily Snack list and both stores on one page: [PREVIEW LINK]. No catch — if you like the direction, Devflix builds proper sites like this for small Auckland businesses. Happy to tweak anything — worth a look?

## author_id
17841445756305482
