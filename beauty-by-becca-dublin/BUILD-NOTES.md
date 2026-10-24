# BUILD NOTES — Beauty by Becca preview site

Built 2026-10-23 (night batch) by Devflix. Business: **Beauty by Becca (LASHES | BROWS | FACIALS)**,
Sallynoggin, South Dublin, Ireland — IG @beautybybecca.xx (881 followers, public, author_id 17841463249972434).
Contact: NOT contacted by this build; DM draft included below for the outreach batch.

## Files
- `index.html` — single page (header, hero, facts strip, services, gallery, about, booking band, footer)
- `img/*.webp` — 7 optimized WebP images (native 640px wide, q78). No base64 anywhere.
- `excluded/brow-lam.webp` — 1 harvested image intentionally NOT used (see below).
- Zip: `~/workspace/instagram/lead-campaign/sites/beauty-by-becca-dublin.zip` (index.html at top level + img/)

## Design identity
Boutique lash/brow studio: warm ivory canvas, espresso ink, raspberry-rose accent,
champagne-gold details. Display serif **Cormorant Garamond** + body **Jost** (2 families,
display=swap). Arched hero portrait frame, dark booking band, serif italic accents —
no generic AI look.

## Photos — all HER OWN work, none stock
Harvested 2026-10-23 via Instagram's public oEmbed API (`instagram.com/api/v1/oembed/`);
every response returned `author_name: beautybybecca.xx`. Each file visually inspected.

| file | natural px | post | subject (visually verified) |
|---|---|---|---|
| hybrid-set.webp | 640x743 | /p/DeFW0E1Rxg4/ (Oct 4 "Hybrids" post) | Eye close-up: dark full hybrid lash set + styled brow — hero |
| classic-set.webp | 640x727 | /p/DcbwZYoxwsD/ | Both eyes: classic lash set close-up — services card |
| full-set.webp | 640x824 | /p/DdmHlmViJlV/ | Full lash set + bold defined brow — services card |
| facial-glow.webp | 640x760 | /p/DdCv-ldotih/ | Client post-facial: glowing skin, defined brows — services + about |
| lash-detail.webp | 640x720 | /p/DaQ8261COOn/ | Natural lash detail with groomed brows — gallery |
| mirror-check.webp | 640x679 | /p/DY0OGPDoeVv/ | Client admiring fresh full set in hand mirror — gallery |
| skin-promo.webp | 640x791 | /p/DYP7TxIiEo1/ | HER OWN pink promo graphic: "MICRONEEDLING + SKIN BOOSTER / SMOOTHER SKIN, NATURALLY. / BeautyBy Becca — BROW & LASH TECHNICIAN" — gallery (captioned as her own post) |
| (excluded) brow-lam.webp | 640x612 | /p/DX7K-bGCOdi/ | Extreme nose close-up (blackhead/extraction detail) — harvested but excluded: not representative of her portfolio and unflattering as a preview; kept in `excluded/` for transparency |

## Image-fit treatment
All photos are portrait (roughly 1:1 to 4:5). Full-view wins over uniformity:
- Hero uses `object-fit:cover` in an arch frame (640x743 native, ~4:4.65 frame) —
  crop ≈ 0-8%, subject (lashes/brows) centred; `object-position:center 20%` keeps the
  set framed. Hero capped at 540px tall (desktop), 420px (mobile).
- Service cards: 4/4.6 frames, `object-fit:cover`, near-native ratio (crop <10%);
  eyes/brows are centred in every shot — verified no subject cut.
- Gallery tiles: 4/4.4 frames; captions sit BELOW images, never overlaid.
- skin-promo.webp (her own text graphic) uses `object-fit:contain` on a pink
  (#FE69C4, sampled from the graphic) background so her "MICRONEEDLING + SKIN
  BOOSTER / SMOOTHER SKIN, NATURALLY / BeautyBy Becca" branding text is fully
  visible — no crop on her own wording.
- About image: `object-position:center 30%` after inspection — glowing skin + brow
  remain fully in frame.
- Verified in headless Chromium screenshots at 390 / 768 / 1440px: every image's
  full subject (lashes, brows, skin) visible; no faces cut.

## Contrast audit (WCAG AA: 4.5:1 normal text, 3:1 large) — all PASS
Computed with relative-luminance formula:

| text | on background | ratio | verdict |
|---|---|---|---|
| #241A17 body/headings | #FBF7F3 ivory | 15.95:1 | PASS |
| #6F5E54 muted body | #FBF7F3 ivory | 5.79:1 | PASS |
| #9C3D5C rose (links, kickers, tags) | #FBF7F3 ivory | 6.09:1 | PASS |
| #9C3D5C rose (em accents in h1) | #FBF7F3 ivory | 6.09:1 | PASS (large text, needs 3:1) |
| #FFFFFF button label | #9C3D5C rose button | 6.09:1 | PASS |
| #FBF7F3 ivory headings | #241A17 dark band | 15.95:1 | PASS |
| #D9CFC4 book paragraph | #241A17 dark band | 11.07:1 | PASS |
| #B98A3E gold (facts numerals) | #241A17 dark band | 5.48:1 | PASS |
| #A89B8E footer small print | #241A17 dark band | 6.27:1 | PASS |

No failures — nothing to fix.

## Responsive verification (headless Chromium, local serve)
Verified 2026-10-23 with Playwright scroll-through (real scrolling to fire
IntersectionObserver + lazy loads) at 390 / 768 / 1440px:
- Horizontal overflow: 0px at all three widths (PASS)
- Reveal: 14/14 `.rv` elements triggered at all widths (PASS)
- Images: 9/9 loaded, 0 broken at all widths (PASS)
- Visual check of screenshots: hero stacks cleanly at 390/768; service cards
  3-col → 2-col (768) → 1-col (390); gallery 2-col → 1-col (390); no overlapping
  text/buttons; all photo subjects fully in frame at every width (PASS)
- Caveat: Google Fonts failed to load inside the sandbox
  (ERR_TUNNEL_CONNECTION_FAILED — sandbox proxy); headings fell back to Georgia
  and remained fully readable. Fonts will load normally on the live Pages URL.

## Fact sources (only what SHE published)
- Name / tagline "LASHES | BROWS | FACIALS" — IG bio, @beautybybecca.xx
- "AIT/ABT Qualified" — bio (research verified_facts)
- "3+ years" — bio (research verified_facts)
- Services: lash extensions (hybrids, classics), brows, facials — bio/captions (verified_facts)
- "DM to book" — booking method from bio (verified_facts)
- "Using @thelashhause lashes" — Oct 4 post caption (DeFW0E1Rxg4)
- Sallynoggin, South Dublin, Ireland — location (verified_facts)
- Microneedling + skin booster graphic — her own IG post (captioned as her post, not added as a named service card)
- NOT published: no prices, no hours, no phone/email — none appear on the site.

## Motion
Scroll-reveal via IntersectionObserver, gated on `.js` added in `<head>` (content fully
visible without JS); `prefers-reduced-motion: reduce` disables reveal and transitions.

## Relative paths
All assets referenced as `img/…` (no leading slash) — deploy-safe as subfolder
`https://the-cut-co.pages.dev/beauty-by-becca-dublin/`.

## DM draft (~80 words) — DO NOT SEND (parent batch sends)
> Hi Becca! I came across your hybrids post from the 4th — that set using @thelashhause lashes is gorgeous, and your brow work is so clean. Noticed bookings all run through DM, which means Google searches for "lash tech Sallynoggin" can't find you. I built you a little preview site with your own photos — [PREVIEW LINK] — would love your thoughts. If you like the direction, I could build the real thing for you. Worth a chat?

author_id: 17841463249972434 · handle: @beautybybecca.xx
