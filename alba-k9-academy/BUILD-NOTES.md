# BUILD NOTES — Alba K9 Academy (alba-k9-academy)

Preview: https://the-cut-co.pages.dev/alba-k9-academy/
Built: Fri 23 Oct 2026 (afternoon batch). Build-only — no DMs, no deploys, no contact with the business.

## 1. Design intent (deliberately different from Cruz K9)
Warm community-academy voice: warm rust/amber + soft cream, editorial serif display (Fraunces) + Inter body, story-driven layout (Bart 8318 logo story, merch with charity angle, October giving-back community section). No dark forest green, no condensed sans.

## 2. Contrast table (WCAG AA — all computed, all ≥ 4.5:1 normal text)

| Text / element | Foreground | Background | Ratio | Pass |
|---|---|---|---|---|
| Body, headings | #2C1E10 ink | #FAF4E8 cream | 14.74 | ✓ |
| Lede, secondary text | #55422C muted | #FAF4E8 cream | 8.71 | ✓ |
| Eyebrows, outline buttons, service H3, donate line | #7E370D rust-dk | #FAF4E8 cream | 7.86 | ✓ |
| Wordmark accent | #A64B1E rust | #FAF4E8 cream | 5.26 | ✓ |
| Location line | #8A5A12 amber | #FAF4E8 cream | 5.40 | ✓ |
| Primary button label | #FAF4E8 cream | #A64B1E rust | 5.26 | ✓ |
| Primary button hover label | #FAF4E8 cream | #7E370D rust-dk | 7.86 | ✓ |
| Service card text | #55422C muted | #FFFDF7 card | 9.38 | ✓ |
| Service card H3 | #7E370D rust-dk | #FFFDF7 card | 8.46 | ✓ |
| Story copy on warm band | #2C1E10 ink | #F1E7D2 cream2 | 13.15 | ✓ |
| Story strong text | #7E370D rust-dk | #F1E7D2 cream2 | 7.01 | ✓ |
| Kit / muted on warm band | #55422C muted | #F1E7D2 cream2 | 7.77 | ✓ |
| Dark-section eyebrows/H3s | #E8B04B gold | #2C1E10 bark | 8.26 | ✓ |
| Dark-section links | #F2C86D pale gold | #2C1E10 bark | 10.20 | ✓ |
| Dark-section body | #EDE0C8 pale | #2C1E10 bark | 12.38 | ✓ |
| Dark-section list text | #F4EAD6 | #2C1E10 bark | 13.53 | ✓ |
| Strip + dark-section headings | #FAF4E8 cream | #2C1E10 bark | 14.74 | ✓ |

Count: 17 pairs, 17 pass, 0 fail.

## 3. Image-fit audit (all photos = business's own IG posts via public oEmbed; 640px ceiling)

| File | Natural | Frame | Fit | object-position | Full-view note |
|---|---|---|---|---|---|
| img/hero-harley.webp | 640×853 (3:4 portrait) | 3:4, max 560px tall | cover | center | Dog (Harley, German Shepherd pup) centered, tongue out, full body + face visible; ~13px top/bottom crop at max width — subject untouched (verified in source inspection) |
| img/bart.webp | 640×640 (1:1) | 1:1 | cover | center 40% | Exact ratio match — zero crop; Bart sitting on dirt path, full body visible |
| img/merch-hoodies.webp | 640×640 (1:1) | 1:1 | contain | center | Whole hoodie mockup visible incl. badge artwork; sits on light-grey native bg inside matching grey frame |
| img/gift-voucher.webp | 640×427 (3:2) | 3:2 | cover | center | Exact ratio match — voucher graphic fully legible |
| img/wednesday-wisdom.webp | 640×674 | 640/674 exact | cover | center | Exact ratio match — all headline/body text visible |
| img/october-giving.webp | 640×640 (1:1) | 1:1 | cover | center 35% | Exact ratio match — Sherpa + all charity text visible |
| img/dog-journey.webp | 640×640 (1:1) | 1:1 | cover | center | Exact ratio match — all 4 stage columns legible |
| img/guest-speaker.webp | 640×640 (1:1) | 1:1 | cover | center | Exact ratio match — trainer, dog, all text visible |
| img/trainer-tam.webp | 640×640 (1:1) | 1:1 | cover | center 30% | Exact ratio match — Tam's face + husky fully visible |
| img/from-the-field-1.webp | 640×853 (3:4) | 3:4 | cover | center | Exact ratio match — both people + dog fully visible |
| img/from-the-field-2.webp | 640×674 | 640/674 exact | cover | center | Exact ratio match — full Halloween artwork visible |
| img/professional-services.webp | 640×640 (1:1) | 1:1 | cover | center 30% | Exact ratio match — full poster visible |

Full-view verification: every image inspected in-source before placement; faces (Tam, two handlers) and dogs (Harley, Bart, Sherpa, husky) fully in frame. No portrait photo forced into a landscape crop. Photos inspected with eyes, not assumed.

## 4. Fact sources (nothing invented)

- Business name, IG handle @albak9academy, 200 followers, Glasgow / North Lanarkshire: research JSON `batch-afternoon-23oct-UKIE-EU.json` + `instagram-cli user-profile` (author_name "Tam | Dog Trainer | Glasgow | North Lanarkshire")
- Services (Pet & Working Dogs, Obedience, Detection Training, Behaviour Alteration; PAYG & block bookings): IG bio text (user-profile result)
- Focus areas (Detection Training, High-Drive Breeds, Behaviour Modification, K9 Enrichment, Dedicated One-to-One Sessions): Oct 19 Christmas gift-vouchers caption (post 18396712903207144)
- Christmas gift vouchers (number of sessions tailored to choice; DM to enquire): same Oct 19 caption
- Wednesday Wisdom quotes ("Some 'behavioural' issues are really just a misunderstanding…"; "This is your dog's first time on this planet"): Oct 21 caption (post 18108084401111833)
- Bart 8318 story (British Army protection dog, Operation Herrick/Afghanistan, crowd control + wind scenting, took 21-year-old Tam under his wing, later Defence Animal Centre training next-gen handlers, harness Easter egg, "this venture wouldn't exist without him"): Oct 10 caption (post 18118782710047100, 32 likes/9 comments per research JSON)
- Hoodies (£5/hoodie to @heropaws retired working dogs; DM size + address): Oct 13 caption (post 17863895775693434)
- October giving back (£10/session to 999 RE:SET, emergency-services mental health, Sherpa "queen of 999 RE:SET"): Sep 28 post + inspected post graphic (post 18625978999048245)
- Your Dog's Journey 4 stages (Consultation digitally/in person; Training session; Debrief & homework; Ongoing support incl. videos): Sep 18 post graphic (post 17986715976025730)
- Guest speaker (scent detection workshops, Central Belt of Scotland, 15 yrs operational military & private sector, drugs/explosives/live body/cargo capabilities): Oct 3 post graphic (post 18143830102599512)
- Private-security services (HNW client families, dog chaperone home & abroad, CP team familiarisation; 15+ yrs): Sep 8 post graphic (post 18012037688955149)
- Phone 07853 708080 + email training@albak9academy.co.uk: published in the business's own guest-speaker / services post graphics (posts 18143830102599512, 18012037688955149)
- Calendly booking link https://calendly.com/albak9academy ("Booking Link"): bio_links from user-profile
- 10% off codes ALBAK9 at @cragdugs2024 and @hawk.k9; hawk-k9.com gear link ("10% off - ALBAK9"): bio text + bio_links
- "New guy" / Harley free consultation (Aug 4 post 18075097940347832): supports "free consultation" copy in booking note
- Free consultation + block of five sessions (Harley posts, Jul–Aug): supports PAYG/block booking models framing
- No prices, no street address, no published phone (beyond graphics), no reviews/ratings shown anywhere — omitted or "ask"

## 5. Photo harvest log (public oEmbed, author_name verified = albak9academy on all 12)

| Site file | Post URL |
|---|---|
| hero-harley.webp | https://www.instagram.com/p/DboK0bYIT8k/ |
| bart.webp | https://www.instagram.com/p/DeT6uIhiCYZ/ |
| merch-hoodies.webp | https://www.instagram.com/p/Debdlmlow6K/ |
| gift-voucher.webp | https://www.instagram.com/p/DerCCycoYjn/ |
| wednesday-wisdom.webp | https://www.instagram.com/p/Dev8AMjICIC/ |
| october-giving.webp | https://www.instagram.com/p/Dd1gLlGI1mU/ |
| dog-journey.webp | https://www.instagram.com/p/DdbYOzMt13K/ |
| guest-speaker.webp | https://www.instagram.com/p/DeB-z7qojYT/ |
| trainer-tam.webp | https://www.instagram.com/p/Da2lqyYAeCH/ |
| from-the-field-1.webp | https://www.instagram.com/p/Dc8iRXJotUl/ |
| from-the-field-2.webp | https://www.instagram.com/p/DdoJYWJo5GR/ |
| professional-services.webp | https://www.instagram.com/p/DdBl9dkIqfH/ |

oEmbed endpoint: `https://www.instagram.com/api/v1/oembed/?url=<post>` with iPhone UA. All 12 returned `thumbnail_url` + `author_name: albak9academy`. Downloaded with browser UA + `Referer: https://www.instagram.com/`, converted to WebP q78 at native 640px (oEmbed ceiling).

## 6. Personalized DM draft (Devflix outreach)

> Hi Tam — the BART 8318 post stopped me scrolling. A British Army protection dog from Herrick, taking a 21-year-old handler under his wing in Helmand, now living on in your badge — that's not branding, that's a founding story, and it's the kind of thing a website was made for.
>
> Right now that story, your October giving-back work, and the hoodies all live scattered across Instagram posts. I built you a concept site that pulls it together — training, the dog's journey, guest speaking, merch — with your Calendly booking link front and centre: https://the-cut-co.pages.dev/alba-k9-academy/
>
> Photos are all yours from your IG. If you like the direction, happy to build it out properly with your real prices and availability — would a quick look be worth 5 minutes?

## 7. Honest shortfalls
- Photo resolution ceiling is 640px (public oEmbed limit) — fine at display sizes used (≤480px), but a real build should ask Tam for full-resolution originals.
- No Chromium on this VM — no screenshot verification; CSS was carefully audited (breakpoints 640/900/1024px, `overflow-x:hidden` on body, nav collapses to wordmark + CTA on mobile, all sections stack at 390px). **A live visual pass at ~390/768/1440px is recommended before any DM goes out.**
- Reveal-on-scroll is gated behind `.js` (content fully visible with JS off); `prefers-reduced-motion` disables the animation.
- Some facts (phone/email) come from the business's own IG post graphics rather than the bio — verified in inspected images, but the business should confirm before publishing live.
- "Free consultation" copy is supported by the Harley consultation post; if the offer has changed, it should be updated.
