# Blissfully Sorted Weddings — Preview Site Build Notes

Built: Sun 25 Oct 2026, Devflix afternoon outreach batch.
Folder: `~/workspace/instagram/lead-campaign/sites/blissfully-sorted-weddings/`
Files: `index.html` + `images/` (6 WebP files). No DM sent, tracker untouched (per brief).

## Design

- Palette: soft ivory neutrals with one deep-sage accent. No gradients, no glassmorphism.
- Fonts (2 families, Google Fonts, display=swap): Cormorant Garamond (display serif) + Inter (body sans).
- Editorial split hero, text beside the photo — never text over a photo.
- Motion: scroll-reveal via IntersectionObserver, gated behind a `.js` class, so all
  content is visible without JavaScript; respects `prefers-reduced-motion`.

## Contrast table (WCAG AA: 4.5:1 normal text, 3:1 large text)

Ratios computed from the exact hex values used (relative-luminance formula):

| Text colour | On background | Ratio | Passes |
|---|---|---|---|
| #2B2622 (ink) | #FDFBF7 (ivory page) | 14.48:1 | AA normal + large |
| #FDFBF7 (ivory) | #2B2622 (ink, contact section) | 14.48:1 | AA normal + large |
| #3E4A38 (sage) | #FDFBF7 (ivory) | 9.06:1 | AA normal + large |
| #FDFBF7 (ivory button label) | #3E4A38 (sage button) | 9.06:1 | AA normal + large |
| #6B5F55 (muted body/eyebrow text) | #FDFBF7 (ivory) | 5.99:1 | AA normal |
| #2B2622 (ink) | #EFE9DC (stone offer band) | 12.37:1 | AA normal + large |
| #3E4A38 (sage) | #EFE9DC (stone offer band) | 7.74:1 | AA normal + large |
| #E8E2D6 (contact body text) | #2B2622 (ink) | 11.60:1 | AA normal |

No section places dark text on a dark image, and no text sits on top of any photo.

## Image-fit audit (FULL VIEW — no cropping anywhere)

All images use `width: 100%; height: auto` with their natural aspect ratio. No
`object-fit: cover` is used anywhere, so no subject is ever cut.

| File | Source post | Natural size | Display | Subject fully in frame? |
|---|---|---|---|---|
| images/hero-bride-sister.webp | DeRIVo7RDVY | 640×640 (1:1) | Hero split, max-width 520 px → ≤520 px tall (cap ~560) | Yes — bride + sister, bouquets, garden path all visible |
| images/gallery-cake.webp | DeZA-HtIaMN | 640×640 (1:1) | Gallery grid, natural ratio | Yes — whole heart-shaped "Just Married" cake visible |
| images/gallery-wedding-morning.webp | DePPvlLiJJ2 | 640×640 (1:1) | Gallery grid, natural ratio | Yes — bridal-dressing help scene; note: the post's own "WHO'S HELPING YOU INTO YOUR DRESS?" text overlay is baked into her original photo and is kept as-is |
| images/gallery-couple.webp | DeBz-JtRyqH | 640×640 (1:1) | Gallery grid, natural ratio | Yes — bride and groom, both faces in frame |
| images/gallery-venue-exit.webp | Dd-su0VRYk_ | 640×640 (1:1) | Gallery grid, natural ratio | Yes — bride, helper, venue steps, full scene |
| images/gallery-reception-wide.webp | Dd55oQgRn8u | 640×360 (16:9) | Own row, max-width 600 px → 338 px tall (≤~340 cap) | Yes — full reception room, all tables visible |

## Responsive audit (CSS audit — no live browser available to this builder)

- Mobile-first: single-column hero/services/steps at base width; 2-column gallery grid
  at base, 4-column at ≥768 px; hero splits into two columns at ≥768 px.
- Fluid widths throughout: `.wrap` max-width 1100 px + `width: 100%`, all images
  `max-width: 100%`, flex/grid containers wrap (`flex-wrap`, grid reflow).
- Breakpoints: ≤390 px (smaller headings/body), ≥768 px (desktop layout).
- No fixed pixel widths on content containers, no horizontal overflow sources
  (no wide tables, no absolute-positioned elements).
- Limitation to flag to the parent: this could not be verified in a live browser at
  390/768/1440 px from this subagent — the CSS audit above is the verification done.
  Recommend a live-browser check before the DM link is sent.

## Fact sources (verified facts only — nothing else invented)

- Business: Blissfully Sorted Weddings, Instagram @blissfullysorted.weddings,
  Lisburn, Co Antrim, Northern Ireland, UK; 1,023 followers; 279 posts.
- Service type: wedding planning / coordination — explicitly NOT décor, NOT florist.
  The site says this plainly so couples are not misled.
- Services (Hitched.co.uk directory listing): bridal dressing, day coordination,
  final-weeks coordination, across Northern Ireland. The Hitched page is a
  third-party marketplace listing, NOT her own website — the site says so in the
  contact section ("also listed on Hitched.co.uk"), never presenting it as her site.
- Offer: £100 off the next 5 bookings, weddings in 2026/2027/2028 — from the
  12 Oct 2026 coordination post (DeZA-HtIaMN), labelled on the site as a current
  offer from that post, with "confirm availability" wording.
- Gap: no website, no bio links; enquiries via DM only ("Enquire about your date").
- NOT invented: no address beyond Lisburn/Co Antrim as briefed, no email, no phone,
  no opening hours, no prices other than the verified offer, no reviews or ratings.
- The coordinator's first name, visible in one post caption, was deliberately NOT
  used, as it was not in the brief.

## Photo harvest log (public oEmbed, 25 Oct 2026)

All 6 posts returned `author_name: blissfullysorted.weddings` (verified match).
Thumbnails downloaded at the 640 px ceiling with a browser Referer/UA, then
converted to WebP at quality ~78. No stock or AI photos used. No shortfall: 6/6 usable.

| Post | Post URL | Result |
|---|---|---|
| DeZA-HtIaMN | https://www.instagram.com/p/DeZA-HtIaMN/ | OK — gallery-cake.webp (640×640) |
| DeRIVo7RDVY | https://www.instagram.com/p/DeRIVo7RDVY/ | OK — hero-bride-sister.webp (640×640) |
| DePPvlLiJJ2 | https://www.instagram.com/p/DePPvlLiJJ2/ | OK — gallery-wedding-morning.webp (640×640) |
| DeBz-JtRyqH | https://www.instagram.com/p/DeBz-JtRyqH/ | OK — gallery-couple.webp (640×640) |
| Dd-su0VRYk_ | https://www.instagram.com/p/Dd-su0VRYk_/ | OK — gallery-venue-exit.webp (640×640) |
| Dd55oQgRn8u | https://www.instagram.com/p/Dd55oQgRn8u/ | OK — gallery-reception-wide.webp (640×360) |

## DM draft (for the parent to send — not sent by this builder)

> Hi! I came across Blissfully Sorted while looking at wedding coordinators in
> Northern Ireland, and your post about couples actually getting to enjoy their
> wedding day instead of running it really stood out — it's a clear, honest pitch
> for what coordination is actually for.
>
> One thing I noticed is that couples can only enquire by DM at the moment, with
> no website to send them to — so anyone searching for a coordinator in Lisburn
> or across Northern Ireland, or wanting to check your services and your £100-off
> offer before messaging, has nowhere to land.
>
> I made you a quick preview of what a simple site could look like, using your
> own photos and services: [PREVIEW LINK]
>
> Would you be open to a quick look and telling me if anything on it needs
> changing?

Notes on the draft: one genuine observation (the "enjoy it, don't run it" positioning
from her own 12 Oct post), why a site helps her specifically (DM-only enquiries, no
website), the preview link placeholder, one low-pressure question. No fake
compliments, no invented stats, reviews or results.
