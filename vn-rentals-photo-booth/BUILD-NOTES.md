# VN Rentals — Preview Site Build Notes

Business: VN Rentals (@vnrentals, author_id 17841456111605855) — 360 / luxury photo booth rental, USA (bio phone 661-564-0906, California area code), insured, 2,096 followers.
Gap: no real website — bio link is only a HoneyBook booking widget; no services/pricing discoverable on the web.
Deploy path: relative asset paths only; merges as subfolder of the-cut-co Pages project → https://the-cut-co.pages.dev/vn-rentals-photo-booth/

## Photos (8, all VN Rentals' own Instagram posts — no stock, no AI)
Source post URLs → file (WebP, ≤1100w, q78, separate files, lazy below fold, width/height attrs):

| Post URL | File | Dims | Subject |
|---|---|---|---|
| instagram.com/p/Dew30MVGlZg | img/hero-glam.webp | 1100×733 | B&W Glam Booth wedding portrait (monogram "A+M 10.3.26") — hero |
| instagram.com/p/DanzR3bCqx3 | img/setup-detail.webp | 1086×1086 | White booth kiosk + printer beside champagne draped backdrop, outdoor event |
| instagram.com/p/DVR5RqOErYQ | img/iconic-booth.webp | 1100×1466 | ICONIC booth kiosk with studio umbrella light + printer at outdoor wedding |
| instagram.com/p/DZx3Qt8jylJ | img/custom-prints.webp | 1100×733 | Guests with "I'm the Birthday Girl" sign, white draped backdrop |
| instagram.com/p/DdpgV0jgbCE | img/senior-sunrise.webp | 1080×1350 | "Senior Sunrise Class of 2027" framed print product |
| instagram.com/p/Dd-QQh5khvm | img/quinceanera.webp | 1080×1350 | Quinceañera 2-frame strip, pink rose wall |
| instagram.com/p/DdmffZfAcj2 | img/rancho-chabela.webp | 1080×593 | "La Princesa" quinceañera portrait (grey IG-thumbnail bars cropped off — content untouched) |
| instagram.com/p/DZYUBFqEmaF | img/black-gold-50th.webp | 1080×1350 | Black/gold "Andre's Retirement & 50th Birthday" collage design |

## Contrast audit (WCAG AA, computed programmatically)
| Pair | Ratio | Verdict |
|---|---|---|
| Ink #241B10 on cream #F6F0E2 (body/headings) | 14.91 | PASS |
| Cream #F6F0E2 on black #100C08 (dark sections) | 17.14 | PASS |
| Gold #C9A227 on black #100C08 (accents, kicker, strip) | 8.05 | PASS |
| Black #100C08 on gold #C9A227 (CTA buttons) | 8.05 | PASS |
| Bronze #6E5216 on cream #F6F0E2 (kicker on light) | 6.41 | PASS |
| Muted #5E5344 on cream #F6F0E2 (secondary text) | 6.61 | PASS |
| Cream #F6F0E2 on brown #3A2C1C | 11.87 | PASS |
| Gold #C9A227 on cream #F6F0E2 | 2.13 | FAIL — rule: gold text is used ONLY on dark backgrounds |
| Gold-deep #8A6A1C on cream #F6F0E2 | 4.44 | FAIL — not used anywhere |
No text is placed over photos (all copy sits on solid panels), so no overlay contrast issues.

## Image-fit audit
- All 8 images verified opened individually: full subject visible, no faces/products cut.
- Full-view rule: every image uses `object-fit: contain` inside frames matched to orientation (landscape→16/10 or natural ratio; portrait→4/5 or natural), never cropped. Hero ≤560px tall desktop; cards ≤340px; band ≤480px.
- Responsive verified in headless Chromium at 390 / 768 / 1440: zero horizontal overflow, no overlap, all reveal-on-scroll elements trigger (threshold lowered to 0.05 after a test caught 6 contact-section items unrevealed on coarse scrolling), all 8 images load.
- Motion: IntersectionObserver reveal gated behind `.js` class (content fully visible with JS off); `prefers-reduced-motion` disables transitions.

## Fact sources (nothing invented)
- "360 Video Booth / Luxury Photo Booth / Digital & Instant prints / Insured / 661-564-0906" — Instagram bio of @vnrentals (verified via instagram-cli post lookup, author_bio).
- "signature Glam Booth", "timeless black + white" — post Dew30MVGlZg caption.
- "Meet ICONIC — our newest addition … created for upscale weddings" — post DVR5RqOErYQ caption.
- "custom designed prints, studio quality photos, keepsakes guests take home that same night" — post DZx3Qt8jylJ caption.
- "setup fits beautifully into any event space" — post DVyeSaplAPE caption.
- Occasions (weddings, quinceañeras, sweet 16s, birthdays, retirements, school events) — evidenced by the posts' own captions/venues. No prices, packages, reviews, or service-area claims beyond what is published.

## DM draft (~80 words)
Hi! I came across your Glam Booth portraits — that black-and-white wedding shot with the "A+M" monogram is stunning, and your setup looks genuinely upscale, not the usual clunky booth. I noticed you don't have a real website yet (just the booking widget), so I built you a concept one using your own photos: [PREVIEW LINK]. It shows off the 360 booth, the ICONIC setup, and your custom prints. Would you be open to me finishing something like this for VN Rentals? — Mudassar, Devflix
