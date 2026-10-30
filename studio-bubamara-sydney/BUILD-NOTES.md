# Studio Bubamara — preview site build notes

Built 30 Oct 2026 (night batch) by the site-builder subagent. NOT deployed, NOT sent — deployment and DM are the parent batch runner's steps.

## Fact sources (verified only — nothing invented)

- Business brief from the batch task: Studio Bubamara, custom embroidery / personalised gifts, Sydney NSW, Australia; Instagram @studio_bubamara; 116 followers, 74 posts; bio angle "for the names they never stocked"; focus on diaspora kids and custom gifts; NO own website, NO bio link — ordering entirely through Instagram (this is the pitch gap).
- All five Instagram posts re-verified live via the public oEmbed endpoint on 30 Oct 2026; every response returned `author_name: studio_bubamara`, confirming the photos belong to this business:
  - https://www.instagram.com/p/DeT9VdkCXAp/ — delicate embroidery for a special celebration (latest post, 10 Oct 2026); "Zoe" name piece with soft green ribbons.
  - https://www.instagram.com/p/Dce_47CiZex/ — BIG SISTER jumper for a family/baby announcement; BIG BROTHER orders mentioned.
  - https://www.instagram.com/p/DcbPf-LJzpg/ — custom third-birthday tennis-club jumper ("T.S Tennis Club, Est. 2023").
  - https://www.instagram.com/p/DbfG-LQRb_l/ — premium 100% cotton personalised jumpers; piece for Isidora with bow + personalised embroidery.
  - https://www.instagram.com/p/DbYGL6NiQUz/ — classic MAMA varsity embroidery with Angelina and Aleksia on the sleeve; "embroidered to order", "custom names available", "Australia-wide shipping".
- No prices, packages, hours, street address, phone, email, reviews or ratings are stated anywhere on the site, because none were verified. The "How to order" steps describe only the verified DM-to-order flow (DM → embroidered to order → Australia-wide shipping).

## Photos (5/5 harvested, 0 skipped)

All thumbnails are the business's own oEmbed `thumbnail_url` images (640px max), downloaded with a browser Referer/UA and converted to WebP quality 78 with Pillow. No stock or AI images, no other business's photos.

| File | Source post | Natural size | WebP size |
|---|---|---|---|
| img/mama-varsity.webp (hero) | DbYGL6NiQUz | 640×853 (3:4 portrait) | 63,494 B |
| img/tennis-three.webp | DcbPf-LJzpg | 640×853 (3:4 portrait) | 100,404 B |
| img/big-sister.webp | Dce_47CiZex | 640×853 (3:4 portrait) | 45,378 B |
| img/cotton-isidora.webp | DbfG-LQRb_l | 640×853 (3:4 portrait) | 38,106 B |
| img/zoe-keepsake.webp | DeT9VdkCXAp | 640×853 (3:4 portrait) | 78,528 B |

## Design identity (own, not a copy of the reference)

Reference studied for structure only: `../aussie-tan-uk/index.html`. This site is deliberately different — warm craft identity: cream `#FAF5EC` + blush sand `#F1E6DA`, deep rose `#7E2E3D`, sage `#4F6151`, warm plum-ink `#33272A`; display font DM Serif Display + body DM Sans (2 families); dashed "stitched thread" rules as the only decorative motif; no gradients, no glassmorphism, no purple/blue glow.

## Per-section contrast results (computed, WCAG AA)

| Pair | Ratio | Pass |
|---|---|---|
| Ink `#33272A` on cream `#FAF5EC` (body/headings) | 13.20:1 | AA ✓ |
| Muted `#6B565A` on cream (lead/secondary text) | 6.23:1 | AA ✓ |
| Rose-deep `#7E2E3D` on cream (eyebrows, links) | 8.24:1 | AA ✓ |
| White on rose-deep `#7E2E3D` (buttons) | 8.95:1 | AA ✓ |
| Cream on ink `#33272A` (CTA band, hero badge) | 13.20:1 | AA ✓ |
| Sage `#4F6151` on cream — strip uses white on sage, body sage text not used on cream for small text; sage-on-cream computed 6.12:1 | 6.12:1 | AA ✓ |
| Muted on sand `#F1E6DA` (collection cards) | 5.50:1 | AA ✓ |
| Rose-deep on sand (card numerals) | 7.28:1 | AA ✓ |
| White gallery captions on dark gradient overlay (approx `#3A2D30` at base) | 13.14:1 | AA ✓ |

All sections pass 4.5:1 for normal text and 3:1 for large text. No text sits on a photo without the dark gradient overlay (gallery captions only).

## Per-image fit / focal notes

- Every source photo is portrait 640×853 (3:4). Every container uses `aspect-ratio: 3/4` with `object-fit: cover` — because container ratio equals photo ratio, cover crops nothing in practice; the full jumper/embroidery stays in frame.
- Hero: `object-position: 50% 50%`, `max-height: 560px` (desktop cap per standard), `max-width: 25rem`, centred.
- Gallery tiles: same 3/4 frame, centred focal point; captions sit in a bottom gradient overlay, never over the embroidery itself at the top of frame.
- No image is stretched or distorted; all carry `width="640" height="853"` attributes; below-the-fold images use `loading="lazy"`; hero uses `fetchpriority="high"`. Zero base64 in the HTML (verified by grep).

## Responsive check — method and result (honest)

- I did NOT do a live-browser check: as a subagent I have no live-browser tool, so no ~390px / ~768px / ~1440px rendered screenshots were taken. The parent runner should verify live before/after deploy.
- What WAS checked structurally: mobile-first single-column layout below 900px (hero stacks, collections stack, steps stack); gallery is 2 columns on small screens and 4 columns ≥900px; nav secondary links hide ≤640px; `body { overflow-x: hidden }`; no fixed-width containers beyond `max-width` values; the only `width: 640px` strings in the file are image `width` attributes, constrained by `img { max-width: 100% }`; the hero badge's −0.75rem offset sits inside the 1.5rem wrap padding, so it cannot push content off-screen at 390px.
- Residual risk to verify live: the 2-column gallery at ~390px (tiles ~165px wide — captions may wrap to 3 lines) and the hero badge position on the smallest screens.

## Personalized DM draft (NOT SENT — placeholder link for the parent runner)

> Hi! I came across Studio Bubamara and loved the idea behind it — embroidery for the names they never stocked. The MAMA jumper with Angelina and Aleksia stitched on the sleeve really stuck with me; it's such a thoughtful way to mark becoming a mum.
>
> I noticed you don't have a website yet and everything runs through Instagram, so I put together a little preview of how a simple site could look for you — your pieces, your story, and an easy way for people to start an order: [PREVIEW LINK]
>
> Would you be open to a quick look? No pressure at all — just thought it might make ordering easier for your customers.

## Files

- `index.html`
- `img/*.webp` (5 files above)
- `BUILD-NOTES.md` (this file)
