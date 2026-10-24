# BUILD-NOTES — The Stitchery (private home tailoring, UAE)

Preview site built 2026-10-22 ~morning PKT for Devflix outreach batch (PK/Gulf).
Directory: `~/workspace/instagram/lead-campaign/sites/the-stitchery-dubai/` → zipped as `the-stitchery-dubai.zip`.

## Photos — how they were obtained (all real, business-owned)
Direct CDN harvesting was documented as impossible in the research file, but two
live routes worked on 2026-10-22:
1. `https://www.instagram.com/api/v1/oembed/?url=<post>` returned `thumbnail_url`
   (signed `scontent…cdninstagram.com` URLs) for all 7 verified post URLs — no
   signature tampering needed (a `p640x640`→`p1080x1080` rewrite returned 403, so
   the as-issued URLs were used).
2. `…/embed/captioned/` also carried the feed-size CDN URLs.
All 7 thumbnails downloaded, converted to WebP q78. Raw JPGs kept in
`.scratch/raw/` (excluded from the zip).

Image audit (all shown at natural aspect — NO cropping, `height:auto`, `width:100%`):

| File | Native | Ratio | Placed | Frame behaviour |
|---|---|---|---|---|
| home-service.webp | 640×793 | 0.807 portrait | Hero (right column, max 430w → ~533px tall ≤ 560 cap) | Full view, no crop |
| abaya-fitting.webp | 640×850 | 0.753 portrait | About (max 430w) | Full view, no crop |
| bridal.webp | 640×853 | 0.750 portrait | Services figure | Full view, no crop |
| craft.webp | 640×853 | 0.750 portrait | Services figure | Full view, no crop |
| delivery.webp | 640×640 | 1.0 square | How-it-works figure | Full view, no crop |
| mauve-abaya-reel.webp | 640×1138 | — | NOT used | Reel thumbnail, subject covered by other images |
| vip-wardrobe.webp | 640×1138 | — | NOT used | Busy "DOO STEP" text overlay, redundant with home-service |

Per-image `width`/`height` attributes set; `loading="lazy"` on all below-fold
images, `fetchpriority="high"` on hero. No base64 anywhere.

## Contrast table (WCAG AA — all pass)

| Pair | Ratio | Gate | Result |
|---|---|---|---|
| Ivory #F8F4EA on ink-black #14110C (hero/nav/footer text) | 17.14:1 | 4.5:1 | PASS |
| Gold #C9A24B on ink-black (hero eyebrow, kicker on dark, phone) | 7.85:1 | 4.5:1 | PASS |
| Black text on gold button (#14110C on #C9A24B) | 7.85:1 | 4.5:1 | PASS |
| Body #2A251D on ivory | 13.85:1 | 4.5:1 | PASS |
| Muted #57503F on ivory | 7.29:1 | 4.5:1 | PASS |
| Bronze #7A5C14 on ivory (sub-copy) | 5.68:1 | 4.5:1 | PASS |
| Gold-deep #8A6714 on ivory (section kickers) | 4.74:1 | 4.5:1 | PASS |
| Ivory #F8F4EA on button-black #1C1812 | 16.08:1 | 4.5:1 | PASS |

Brighter gold #C9A24B was deliberately NOT used for text on ivory (would fail);
dark sections carry gold, light sections carry gold-deep/bronze instead.

## Design
Ink-black + champagne gold + ivory; Cormorant Garamond (display serif) + Jost
(body sans), 2 families, display=swap. No gradients/glass/floating cards.
Editorial two-column hero, numbered process steps, service rows with tick
markers, pull-quote about block. IntersectionObserver reveal gated behind `.js`
(content visible without JS), `prefers-reduced-motion` disables animation.
Mobile-first: grids collapse to one column ≤820–900px; mobile nav hides
text links, keeps "Book via Instagram" CTA.

## Responsiveness (no live browser available to this builder — code-reviewed)
- 390px: single column everywhere, images max-width 100% / height auto,
  nav keeps brand + CTA only, buttons wrap.
- 768px: single/double column per section (no fixed widths that overflow).
- 1440px: content capped at 1140px wrap; hero 2-col.
No horizontal-overflow sources: `box-sizing:border-box`, no 100vw, no
absolute-positioned decor.

## Fact sources (nothing invented)
- Business facts: task brief (verified 22 Oct 2026): name, IG handle,
  "UAE's Premier Private Home Tailoring Service", bio "Bespoke. Private.
  Perfection.", home-visit measurement/pinning → workshop alterations →
  doorstep delivery, no website/no bio link.
- Post captions via oEmbed (their own words, used on site): "custom stitching
  for all types of attire", "expert alterations for branded & designer outfits",
  "female tailor service available / on request", abayas + custom outfits +
  altered dresses, "No traffic. No extra trips", bridal gown work ("delicate
  lace and intricate beadwork"), "More than tailoring. It's a better you.",
  "Your style, crafted in the comfort of your home."
- ⚠️ PHONE: the task brief said phone was NOT published, but the business's own
  Oct 20 caption (via oEmbed) prints "📞 052 123 6559" — same number as on
  their flyer image. Included on the site as a tel: link with caption
  "as published on @stitchery_tailoring". Parent: decide whether to keep.
- Location: captions say "Abu Dhabi, UAE"; bio says UAE-wide; flyer names
  Corniche/Electra/Khalidiya (Abu Dhabi). Site says "UAE" only — no
  city-specific coverage claims.
- No prices, hours, turnaround times, reviews, or ratings anywhere — none published.
- DM booking CTA links to https://www.instagram.com/stitchery_tailoring/.

## DM draft (for parent — personalized, [PREVIEW LINK] placeholder)
> Hi! I came across The Stitchery while looking at home tailoring services in
> the UAE — the "tailor comes to your doorstep" idea really stands out, and
> your abaya fitting posts show the craft clearly. One thing I noticed: with no
> website, everything a new customer can learn about the service lives inside
> Instagram captions, so Google can't find you at all. I built a small concept
> site for The Stitchery so you can see what a proper web presence would look
> like: [PREVIEW LINK] — no charge, just an idea. Would you be open to a quick
> look and telling me what you think?
