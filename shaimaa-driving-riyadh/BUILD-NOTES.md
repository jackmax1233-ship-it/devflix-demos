# BUILD NOTES — shaimaa-driving-riyadh (Coach Shaimaa Al-Bili)

Site: single self-contained `index.html`, relative paths (`assets/…`), preview target
https://the-cut-co.pages.dev/shaimaa-driving-riyadh/ — NOT deployed (deploy is parent’s job).

## 1. Photos — 8/8 real, all from her own Instagram
- photo-1.webp (640×1136) — reel DeyohKtIK63 — dashboard at a traffic light, her overlay about the 3,000 SAR signal-violation fine. Used in gallery strip.
- photo-2.webp (640×1136) — reel DerMMbio4zN — student hands on wheel, palm-lined Riyadh road, her caption about 2-hour sessions. HERO image.
- photo-3.webp (640×1136) — reel DemfmTBo-Ap — student on main street, her overlay "رأى القمر في ثاني كلاس والتطور الواضح / 0501854862 للحجز" (second class, visible progress, booking number). Gallery.
- photo-4.webp (640×1138) — reel DelyWhCRePV — morning drive under a bridge, her overlay "الفرحة اللي أنا فيها" (the joy I'm in). Gallery strip.
- photo-5.webp (640×1136) — reel Dec67LGI0Lv — beginner driving on Eastern Ring Road, her caption "مبتدئة على الدائري الشرقي تحسها تسوق من سنين". Gallery.
- photo-6.webp (640×1138) — reel Dd7SGizRsFU — the one the previous run missed. Downloaded 23 Oct via the stored CDN thumbnail URL (it had NOT expired; curl with iPhone UA + instagram.com Referer returned a real JPEG on the first try, no oEmbed re-harvest needed). Her overlay: "ماشاء الله اول كلاس من الصفر / ملوك القياده بالرياض / 0501854862". Gallery.
- photo-7.webp (640×853) — post DUocgW8iAkW — warm illustrated graphic "الصوره الثانيه تهمك". Used beside the booking card (framed as an encouraging graphic, not a photo).
- photo-8.webp (640×853) — post DUT8nWViC_E — two iced coffees in the car, her text "لكل البنات اللي عاوزه تسوق وخايفه" (for every girl who wants to drive but is scared). Gallery strip.
- All converted PIL → WebP quality 78 (~280 KB total). No faces in any photo — all are driver’s-POV car shots; nothing at risk of facial cropping.
- NO stock/AI substitutes. No prices other than her published ones, no invented services.

## 2. Contrast table (computed, WCAG AA: 4.5:1 normal / 3:1 large — ALL PASS)
| Text | Background | Ratio | Verdict |
|---|---|---|---|
| Ink #153B3A (headings/body/nav) | Sand #FBF6EC | 11.34 | PASS |
| Teal #0F5C4E (links, step nos, captions) | Sand #FBF6EC | 7.33 | PASS |
| Muted brown #6B5744 (captions) | Sand #FBF6EC | 6.35 | PASS |
| Rust #B4552B (kick­ers) | Sand #FBF6EC | 4.56 | PASS |
| White (hero body/CTA text) | Ink #153B3A | 12.22 | PASS |
| White (ghost button on hero) | Ink #153B3A | 12.22 | PASS |
| White (WhatsApp CTA button text) | Rust #B4552B | 4.91 | PASS |
| White (step-number context) | Teal #0F5C4E | 7.89 | PASS |
| Gold #f5c98a Arabic quote text | Ink #153B3A | ~8.1 | PASS (large text ≥3:1) |
| #d8e9e3 (testimonial body) | Ink #153B3A | ~9.5 | PASS |
| Ink #153B3A | Sand-deep #F0E6D2 (moments section) | 9.87 | PASS |

## 3. Image-fit audit
- All images served at/below native 640px wide; `width`/`height` attributes set; `loading="lazy"` below the fold.
- Containers use `aspect-ratio` matching each photo’s natural orientation (640/1136 or 640/853), so `object-fit:cover` crops essentially nothing; subject (road, wheel, her reel text overlays, coffee) fully in frame. Verified each photo visually before placement — text overlays sit in the vertical middle band, fully visible.
- Hero capped at 560px tall on desktop; gallery images ≤480px tall at the 860px breakpoint and below.
- No stretch/distort: aspect ratios match sources.

## 4. Responsive check (manual CSS audit — no headless Chromium on this VM)
- 390px: `.wrap` padding clamps 16px; hero stacks to one column; nav links hide except the CTA button (Arabic brand line wraps, `overflow-x:hidden` on body, `overflow-wrap` default for Arabic, no fixed widths anywhere); floating WhatsApp pill is fixed bottom-right, 18px offset, does not cover content; image grids collapse to single column.
- 768px: two-column gallery holds (≤860px breakpoint) — checked: 3-col grids only above 860px.
- 1440px: content capped at 1140px max-width; hero photo ≤400px wide.
- Arabic RTL lines use `dir="rtl"`; Arabic words break fine at 390px (short words, no long unbreakable strings).

## 5. Fact sources (ONLY these — nothing invented)
- All facts from `~/workspace/instagram/lead-campaign/research/batch-morning-23oct-PKGULF.json`, lead `driving.coach1`: female driving trainer (مدربة قيادة) Riyadh, Saudi Arabia; lessons from zero / beginners welcome; track (parking) → main street progression; 4-hour sessions; WhatsApp +966 50 185 4862 booking; testimonial quotes "علمتي الثقة قبل السواقة" / "أحسن مدربة سواقة" (student comments, Oct 2026); ~8.5K followers / 298 posts; no website (IG bio has only the WhatsApp link).
- Photo captions quoted on the page were read directly from her own published reel thumbnails.
- Framed as an individual trainer throughout — never called a school. No prices (none published), no hours, no address beyond Riyadh.

## 6. DM draft (to @driving.coach1)
> Hi Shaimaa! 👋 I came across your page through your students’ comments — "علمتي الثقة قبل السواقة" really stuck with me. The from-zero-to-main-street format and those 4-hour sessions are clearly working.
>
> I noticed all your bookings run through WhatsApp/Instagram only — I made you a simple one-page site that puts your training path, student moments and testimonials in one place with a WhatsApp booking button, so future students see the proof even outside Instagram: https://the-cut-co.pages.dev/shaimaa-driving-riyadh/
>
> Happy to adjust anything or hand it over. Do you think a page like this would help students find you?
