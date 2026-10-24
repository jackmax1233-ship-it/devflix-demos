# BUILD NOTES — Aussie Tan UK preview site
Built: 2026-10-23 ~01:30 PKT by subagent (night outreach batch)
Deploy target (parent to deploy): subpath `aussie-tan-uk` on the-cut-co Pages project → https://the-cut-co.pages.dev/aussie-tan-uk/
All asset paths are relative (`img/*.webp`, Google Fonts only absolute).

## Photo harvest — SUCCESS (research-file block claim was wrong)
- The research JSON said photo harvesting was BLOCKED (oEmbed login-walled). That claim is inaccurate from this environment: the public `instagram.com/api/v1/oembed/?url=<post>` endpoint returns full JSON **including `thumbnail_url`** when called with a real browser User-Agent (curl + UA, no login).
- Harvested 8/8 post thumbnails via curl from the research file's post URLs; each verified as a real RGB photo (640×853, photo-8 640×842) and visually checked — all are genuine bridal-tan portfolio shots from @aussietan_uk. Downloaded 2026-10-22 ~20:10 PKT.
- Limitation: thumbnails are 640w (Instagram CDN `p640x640`); requesting `p1080x1080` variants 403s. Resolution is adequate for the chosen layout (hero max-width ~26rem, gallery tiles ≤ ~20rem wide; images are display-size-native, not upscaled beyond their width).
- Converted to WebP q78 (PIL): 14–72 KB each. JPG originals deleted; only WebP ships.

| File | Source post | Subject (verified visually) | Focal point set |
|---|---|---|---|
| img/photo-1.webp | instagram.com/p/DexEt7fjZoy/ | Bride on grass, face upper-right | 70% 25% |
| img/photo-2.webp | instagram.com/p/DdUb-XBjStx/ | Bride indoors, face center-top | 50% 20% |
| img/photo-3.webp | instagram.com/p/DctfERrDXRU/ | Bride outdoors w/ bouquet, face top-left | 30% 15% |
| img/photo-4.webp | instagram.com/p/DctatRCjfLd/ | Bride off-shoulder indoor, face center-top | 50% 20% |
| img/photo-5.webp | instagram.com/p/DcjX1Z7DUFA/ | Bride full-length, face upper-center | 50% 22% |
| img/photo-6.webp | instagram.com/p/Dcgg3fMjQ6n/ | Bride by window, face top-right | 65% 15% |
| img/photo-7.webp | instagram.com/p/DbyYyFHDYUt/ | Wedding ceremony close-up, faces center-left | 35% 40% |
| img/photo-8.webp | instagram.com/p/Dblp3cgDcB_/ | Bride in garden (their 135-like Aug 3 post), face center-top | 50% 15% |

Usage: photo-8 = hero; photo-1..6 = results gallery; photo-7 = "why" section. Alt text describes the photo content only, no invented names.

## Contrast audit (WCAG AA, computed with Python luminance — all PASS at 4.5:1+)
- #3A2415 ink on #FAF3E7 cream (body/headings): **13.19:1** PASS
- #FFFFFF on #7E3517 (primary buttons): **8.72:1** PASS
- #A24B26 terra on #FAF3E7 (eyebrow labels, small accent text): **5.33:1** PASS
- #FAF3E7 on #2A1A10 (dark CTA band + badge): **15.19:1** PASS
- #6B4A33 muted on #FAF3E7 (body secondary): **7.18:1** PASS
- #7E3517 on #F1E4D0 sand (numbers, links on sand band): **6.95:1** PASS
- #FAF3E7 on #8F3F1C (button hover): **6.57:1** PASS
- Gallery captions: white text on dark gradient overlay (rgba(42,26,16,.88)) — PASS
- Focus states: 3px terra outline on buttons. No text over unshaded photos.

## Image-fit audit
- All source photos are portrait ~3:4; all frames use `aspect-ratio:3/4` with `object-fit:cover` + per-photo `object-position` (table above) → ≤1% edge trim, no subject cut. Hero ≤560px tall; "why" image ≤480px; gallery tiles natural height (full-view wins over uniformity per standing order).
- Faces checked full-frame at 390/768/1440 screenshots — no faces, heads, or bouquets cut.
- width/height attrs set on all `<img>`; hero uses `fetchpriority="high"`; below-fold images `loading="lazy"`; zero base64 (AGENTS.md standard).

## Responsive audit (headless Chromium, real screenshots)
- 390px: stacks cleanly; nav collapses to logo + CTA; hero photo full-view below copy; 2-col gallery; CTA band rounded margins intact. No horizontal overflow.
- 768px: same stack; photo centered; no overlap/clipping.
- 1440px: asymmetric editorial hero (copy left / portrait right); 3-col gallery with lead tall tile; why section 2-col; CTA band centered. No overflow.
- Programmatic probe at all widths: `documentElement.scrollWidth == clientWidth` (0 page-level overflow), all 8 images `complete && naturalWidth>0`. One cosmetic fix applied: "Australian-made" now uses non-breaking hyphen (was wrapping as "Australian / -made formula" at narrow widths).
- Motion: `.reveal` gated behind `.js` (content visible without JS); IntersectionObserver reveal; `prefers-reduced-motion` respected. Note: a `?static=1` query flag skips the reveal animation — used only for QA screenshots, harmless in production.

## Fact sources (nothing else claimed)
- "Spray tanning studio, London UK" / "Ultimate Natural Looking Spray Tan" / "Australian-made product" / sister branch @aussietan_israel / no website field: from research JSON verified_facts (batch-afternoon-22oct-UKIE.json, entry author_id 17841405315298626) and the dm_observation.
- "Bridal tans / bridal glow": from their own post captions (bridal-glow posts Aug 3 – Oct 21 2026).
- "Booking starts with a DM": from verified "DM to book" pattern + no other published booking route. No prices, hours, addresses, reviews, or stats anywhere on the page.
- Contact CTAs: `https://ig.me/m/aussietan_uk` (Instagram DM) and `https://www.instagram.com/aussietan_uk` (profile). No invented contact details.

## DM draft (~80 words) — DO NOT SEND (task says build only)
author_id: 17841405315298626

Hi Aussie Tan UK! Your before-and-after carousel portfolio is stunning — the "ultimate natural-looking spray tan" promise really shows in your results, especially the bridal glows. One thing I noticed: people Googling "spray tan London" can't find you, since everything lives on Instagram. I'm Mudassar from Devflix, and I built a quick preview of what a site for you could look like, using your own photos: [PREVIEW LINK] If you like the direction, happy to build it out properly. Would that be of interest?
