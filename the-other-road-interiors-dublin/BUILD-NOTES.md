# BUILD NOTES — the-other-road-interiors-dublin

Preview URL (final): https://the-cut-co.pages.dev/the-other-road-interiors-dublin/
Batch: morning 23 Oct 2026 (UK + Ireland) · Lead: **The Other Road Interior Design** (@theotherroadinteriors, Dublin, Ireland, 954 followers)

## 1. Photo download log (honest)

| # | Status | File | Native size | WebP (q78) |
|---|--------|------|-------------|------------|
| 1 | ✅ OK | photo-1.webp | 640×1136 | 21.6 KB — bathroom: tiled vanity, veined stone vessel basin, brass taps, mirror, hex floor |
| 2 | ✅ OK | photo-2.webp | 640×1138 | 95.0 KB — Emma & Ava (founders) in glass sunroom; burned-in reel-cover text "The Other Road Interiors" (their own graphic) |
| 3 | ✅ OK | photo-3.webp | 640×1136 | 50.7 KB — living-room corner: round timber tables, linen sofa, patterned rug, tall plant |
| 4 | ❌ 403 | — | — | CDN signature expired (also failed with desktop UA) |
| 5 | ❌ 403 | — | — | CDN signature expired |
| 6 | ❌ 403 | — | — | CDN signature expired |

- Downloaded 2026-10-23 ~10:21 PKT with iPhone UA + `Referer: https://www.instagram.com/`; verified real JPEGs via `file`.
- Converted with PIL (libwebp), quality 78, kept at native 640px width. Original JPEGs deleted after conversion; only `.webp` ships.
- Re-harvest attempted: Instagram `web_profile_info` API returned **429 (rate-limited)** — hard stop, no retry. No post URLs in the research JSON, so oEmbed re-harvest was not possible without them.
- **Design consequence:** only 3 of 6 photos available, so `photo-1.webp` (bathroom) is used twice — hero + first work entry — rather than padding the site with fewer portfolio images. **No stock/AI photos substituted.**

## 2. Contrast audit (WCAG AA — computed, not estimated)

Palette: cream `#F6F1E6` · forest `#1E3329` · ink `#26302B` · muted `#4A544E` · clay `#9A5B33` · clay-light `#D9A97E` · parchment `#EFE8D8` · parchment-soft `#CFC7B4` · white `#FFFFFF`.

| Text | Background | Ratio | AA (4.5:1) | Where |
|------|-----------|-------|-----------|-------|
| ink `#26302B` | cream `#F6F1E6` | 12.11:1 | ✅ PASS | body |
| forest `#1E3329` | cream `#F6F1E6` | 11.95:1 | ✅ PASS | H1/H2/headings, wordmark, ghost button |
| white `#FFFFFF` | forest `#1E3329` | 13.46:1 | ✅ PASS | primary buttons, hover states |
| clay `#9A5B33` | cream `#F6F1E6` | 4.76:1 | ✅ PASS | eyebrow labels |
| muted `#4A544E` | cream `#F6F1E6` | 6.98:1 | ✅ PASS | lede, secondary copy |
| clay `#9A5B33` | white `#FFFFFF` | 5.36:1 | ✅ PASS | eyebrows in work section |
| muted `#4A544E` | white `#FFFFFF` | 7.87:1 | ✅ PASS | work copy, figcaptions |
| forest `#1E3329` | white `#FFFFFF` | 13.46:1 | ✅ PASS | work headings |
| parchment `#EFE8D8` | forest `#1E3329` | 11.02:1 | ✅ PASS | studio headings, footer name |
| parchment-soft `#CFC7B4` | forest `#1E3329` | 8.00:1 | ✅ PASS | studio body, footer copy |
| clay-light `#D9A97E` | forest `#1E3329` | 6.36:1 | ✅ PASS | eyebrows on dark |
| cream `#F6F1E6` | forest `#1E3329` | 11.95:1 | ✅ PASS | (reserved) |

**Result: all 12 text/background pairs PASS WCAG AA.** Decorative-only colour (`--cream-deep` shadow) carries no text.

## 3. Image-fit audit (FULL VIEW)

- All three photos are **portrait** (640×1136/1138). Every `<img>` is displayed with `height` set (hero 540px desktop / 440px ≤900px / 400px ≤560px; content 460px / 420px / 380px) and `width:auto` — aspect ratio is **never distorted**, no `object-fit: cover`, no cropping of any subject.
- Images displayed **at/below native size** (max rendered width ≈ 304px at 540px height < 640px native).
- `width`/`height` attributes on every image (prevents layout shift); hero `fetchpriority="high"`, below-fold images `loading="lazy"`.
- Hero ≤560px tall ✓ (540px). Content images ≤480px tall ✓ (460px).
- Alt text describes the visible scene (bathroom details, founders, living-room details) — no invented project names.

## 4. Fact sources (from `research/batch-morning-23oct-UKIE.json` ONLY)

| Site claim | JSON source |
|-----------|-------------|
| "Dublin, Ireland" studio | city: Dublin, country: Ireland; posts tagged "Dublin, Ireland" |
| Founded by Emma & Ava | why_good_prospect: "founded by Emma and Ava (per Oct 9 intro reel)"; engagement_facts: 2026-10-09 reel (studio intro, founders Emma & Ava) |
| Residential interior design, bespoke schemes, colour | industry: "interior design studio (residential, bespoke schemes, colour)" |
| 954 followers | followers: 954 |
| No website; bio link is only Linktree (linktr.ee/theotherroad) | gap field |
| Enquiries/bookings via Instagram/DM only | gap field |
| Supplier tags @capietra, Synk Concrete, @finlinefurniture | why_good_prospect + engagement_facts ("caption names real suppliers (@capietra, Synk Concrete)") |
| Bathroom project reveal Oct 16, tagged Dublin | engagement_facts: "2026-10-16 reel (bathroom project reveal, tagged Dublin): 10 likes, 4 comments" |
| Enquiry CTA → https://www.instagram.com/theotherroadinteriors/ | task brief |

Nothing else asserted: **no prices, no reviews/ratings, no hours, no phone/email, no service claims beyond the industry line.**

## 5. Responsive check (CSS audit — no headless browser on this VM)

- Breakpoints: default (desktop, max-width 1152px grid), ≤900px (all grids collapse to single column), ≤560px (nav links hide, CTA button remains).
- 390px: hero stacks, image 400px tall (~226px wide, full view); work/studio stack; header fits (wordmark + one button); no fixed widths > viewport; figures have `min-width:0`.
- 768px: single-column layouts already active (≤900px); no horizontal overflow sources (no negative margins, no wide tables).
- 1440px: `.wrap` caps content at 1152px, centred.
- Sticky header is solid cream (no glassmorphism). Reveal animations: `.js`-gated (visible without JS); `prefers-reduced-motion` disables them.

## 6. Design notes

- Warm editorial feel: plaster cream + deep forest green + terracotta clay. Fraunces (display serif) + Inter (body), Google Fonts `display=swap`, max 2 families.
- No gradients, no glassmorphism, no floating cards. Single self-contained `index.html`, **relative paths only** (works under the merged `/the-other-road-interiors-dublin/` subpath).
- Footer credit: "Concept preview made by Devflix" (standard for outreach demos).

## 7. Honest caveats

1. **Only 3 of 6 photos downloadable** — CDN signatures for photos 4–6 expired (403s); re-harvest blocked by IG 429. Bathroom image reused as hero + project 1.
2. **Not verified in a live browser** — no headless Chromium on this VM; responsive behaviour verified by CSS audit only. Parent should spot-check the merged deploy at 390/768/1440px before the DM goes out.
3. The founders photo carries their own burned-in reel-cover text ("The Other Road Interiors") — kept as-is; it is their authentic asset.
4. **Do NOT deploy** — left for the batch deploy step (merged subpath under the-cut-co project).

## 8. DM draft (for parent's send step)

> Hi Emma & Ava — came across your studio while looking at Dublin interiors, and your October bathroom reveal really stood out. Love how you credit the actual makers in your captions (@capietra, Synk Concrete) — that kind of transparency is rare.
>
> One thing I noticed: everything funnels through Instagram DMs right now, with just the Linktree as a "website". We made you a quick concept of what a proper site could look like — portfolio, your story, and a clear enquiry flow, all in your warm style:
> https://the-cut-co.pages.dev/the-other-road-interiors-dublin/
>
> Would a real website with a proper enquiry page be useful for the studio at this stage, or is Instagram working fine for you?
