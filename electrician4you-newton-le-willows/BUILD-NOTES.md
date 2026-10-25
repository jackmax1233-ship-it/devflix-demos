# BUILD NOTES — Electrician4you (Newton-le-Willows / Liverpool area)

- **Slug:** `electrician4you-newton-le-willows`
- **Local dir:** `~/workspace/instagram/lead-campaign/sites/electrician4you-newton-le-willows/`
- **Preview link (for DM, NOT yet deployed by this task):** https://jackmax1233-ship-it.github.io/devflix-demos/electrician4you-newton-le-willows/
- **Status:** Built on disk only. NOT deployed, NO DM sent, NO tracker edited (per task scope).
- **Instagram:** [@local_electrician4you](https://www.instagram.com/local_electrician4you) — 443 followers (per brief).
- **Design:** Dark charcoal + safety-amber trade look. Fonts: Archivo (headings, 700/800/900) + Inter (body) via Google Fonts with `display=swap`. No gradients, no glassmorphism, no floating-card clutter, no oversized meaningless hero headline — the hero line is the business's own tagline from its captions.
- **Responsive audit:** CSS audit only — no Chromium on this VM, so no live screenshot pass was possible. Layout is mobile-first with breakpoints at 900px and 560px; nav collapses below 900px, all grids stack to one column at mobile width, images use `max-width:100%; height:auto`, `box-sizing:border-box` is global. **A live visual pass at ~390px / ~768px / ~1440px is still recommended before the pitch goes out.**
- **Paths:** All image `src` values are relative (`images/xxx.webp`, no leading slash, no absolute URLs), so the page works under a GitHub Pages subpath. No base64 images anywhere in the HTML.

## (a) Contrast table — all pairs pass WCAG AA

Ratios computed from relative luminance (WCAG formula). Pass = ≥4.5:1 for normal text, ≥3:1 for large text. Every pair below passes for normal text, so the whole page passes.

| Text | Background | Ratio | Result |
|---|---|---|---|
| #FFFFFF body/headings | #17181A hero, header strip, band, footer | 17.77:1 | ✅ PASS |
| #F5B301 amber eyebrow/headline accent | #17181A dark sections | 9.59:1 | ✅ PASS (large + normal) |
| #17181A ink text | #F5B301 amber buttons / strip | 9.59:1 | ✅ PASS |
| #17181A ink text | #FAF7F0 paper background | 16.61:1 | ✅ PASS |
| #3A3D42 body grey | #FAF7F0 paper background | 10.19:1 | ✅ PASS |
| #5A5E66 muted grey (captions, small print) | #FAF7F0 paper background | 6.08:1 | ✅ PASS |
| #17181A ink text | #FFFFFF service cards | 17.77:1 | ✅ PASS |
| #3A3D42 body grey | #FFFFFF service cards | 10.19:1 (approx; same pair family as on paper) | ✅ PASS |
| #D8D5CC muted light | #17181A dark sections | 12.11:1 | ✅ PASS |
| #FFFFFF | #1E2023 figure backgrounds | 16.33:1 | ✅ PASS |
| #F5B301 amber links | #17181A footer/topbar | 9.59:1 | ✅ PASS |
| #8A5B00 dark amber (kicker labels) | #FAF7F0 paper background | ~5.9:1 (measured #FFFFFF on #8A5B00 = 5.87:1; dark-on-light is higher) | ✅ PASS |

**Contrast pass count: 12/12 pairs pass WCAG AA (all at normal-text level). No text is placed over a photo** — every caption sits on a solid dark or paper background, so photo contrast is never an issue.

## (b) Image-fit audit — full view, no cropping

All images are shown at their natural aspect ratio (`width:100%; height:auto`, no `object-fit:cover` cropping anywhere). Nothing is cut.

| File | Natural size | Ratio | Used as | Container behaviour | Height at desktop | Verdict |
|---|---|---|---|---|---|---|
| `images/fusebox-upgrade.webp` | 640×452 | 1.42:1 landscape | Hero | Full width of hero column, natural ratio | ~365px (column ~515px wide) — under the ~560px hero cap | ✅ Full view |
| `images/eicr-inspection.webp` | 640×800 | 0.80:1 portrait | Landlords split | Natural ratio, stacks above text on mobile | ~400px at split-column width | ✅ Full view |
| `images/fusebox-ev-charger.webp` | 640×853 | 0.75:1 portrait | Gallery (wide, 2-col span) | Natural ratio, spans 2 gallery columns | ~480px at wide-column width | ✅ Full view (see note) |
| `images/soffit-lighting-liverpool.webp` | 640×800 | 0.80:1 portrait | Gallery card | Natural ratio | ~450px at card width | ✅ Full view (see note) |
| `images/van-signage.webp` | 640×853 | 0.75:1 portrait | Gallery card | Natural ratio | ~480px at card width | ✅ Full view (see note) |
| `images/electrical-safety.webp` | 640×640 | 1.00:1 square | Gallery card | Natural ratio | ~360px at card width | ✅ Full view |
| `images/damaged-cables.webp` | 640×853 | 0.75:1 portrait | Fault-finding band | Natural ratio | ~480px at band-column width | ✅ Full view (see note) |

**Honest note on the 340px card guideline:** the portrait gallery/band photos run taller than the ~340px card-height guideline at desktop width because they keep their natural portrait ratio. Per the standing FULL-VIEW hard gate in AGENTS.md, full view wins over uniform card frames — cropping these portrait job photos to 340px would cut the fuse boxes, van and cables that are the whole point. Hero (~365px) is inside the ~560px cap; no full-bleed band exceeds ~480px of image height.

## (c) Fact sources — every claim traced

| Claim on the site | Source |
|---|---|
| Business name "Electrician4you", IG @local_electrician4you | Task brief + oEmbed `author_name` verified on all 7 posts |
| Area: Newton-le-Willows / Liverpool area | Brief; posts tagged Newton-le-Willows; one job in Liverpool (soffit lighting post DdLvZcRCv9f) |
| Tagline "Improving your electrical safety, one property at a time" | Business's own captions (DeusngnDWFr, DeusMH1jcX2) |
| Services: fuse-box/fuse-board swaps, RCD/mains-board work, floodlights, landlord work, EICRs, house rewires, electrical safety, inspection & testing, EV charger fitting, soffit lighting | Brief's service list, drawn from bio/captions |
| "Saturday morning fuse-box upgrade" | Caption DeusngnDWFr (2026-10-20) |
| "New fuse-box upgrade and EV charger fitted this week in Newton-le-Willows" | Caption DeusMH1jcX2 (2026-10-20) |
| Landlord section copy (identify hidden faults / keep tenants safe / protect your property / stay up to date; "tenants don't always report issues") | Caption DdcWcmZDexV (2026-09-18) — paraphrased, no added legal claims |
| "Proudly serving Newton-le-Willows and surrounding areas", "clear advice, no unnecessary jargon", "Your property. Your safety. Our expertise." | Caption DdLx2GWipU_ (2026-09-12) — paraphrased |
| "New soffit lighting went in last week in Liverpool" | Caption DdLvZcRCv9f (2026-09-12) |
| Van sign-written, "ready for action" | Caption DcjLVeFjZwE (2026-08-27) |
| Damaged lighting cables found during fault-finding | Caption DcQtiQRteTP (2026-08-20) |
| CTA is Instagram DM only | Brief: bio is hashtags only, no link/phone/email on the profile |

**NOT on the site, deliberately:** no prices, no opening hours, no reviews/testimonials, no ratings, no years-in-business, no qualifications/certifications, no invented statistics. None of these appear in the supplied facts.

## (d) Photo harvest log — 7/7 harvested, 0 failures

Method: public oEmbed endpoint with iPhone UA; `author_name` verified = `local_electrician4you` for every post before download; thumbnails downloaded with browser UA + Instagram Referer; converted to WebP quality ~78 via Python PIL. 640px is the oEmbed ceiling, as expected.

| Shortcode | Post date (brief) | Subject | author_name verified | File | Status |
|---|---|---|---|---|---|
| DeusngnDWFr | 2026-10-20 | Fuse-box upgrade | ✅ local_electrician4you | `images/fusebox-upgrade.webp` (27 KB, 640×452) | ✅ Harvested |
| DeusMH1jcX2 | 2026-10-20 | Fuse-box + EV charger | ✅ local_electrician4you | `images/fusebox-ev-charger.webp` (25 KB, 640×853) | ✅ Harvested |
| DdcWcmZDexV | 2026-09-18 | EICR | ✅ local_electrician4you | `images/eicr-inspection.webp` (23 KB, 640×800) | ✅ Harvested |
| DdLx2GWipU_ | 2026-09-12 | Electrical safety | ✅ local_electrician4you | `images/electrical-safety.webp` (97 KB, 640×640) | ✅ Harvested |
| DdLvZcRCv9f | 2026-09-12 | Soffit lighting, Liverpool | ✅ local_electrician4you | `images/soffit-lighting-liverpool.webp` (56 KB, 640×800) | ✅ Harvested |
| DcjLVeFjZwE | 2026-08-27 | Van signage | ✅ local_electrician4you | `images/van-signage.webp` (101 KB, 640×853) | ✅ Harvested |
| DcQtiQRteTP | 2026-08-20 | Damaged lighting cables | ✅ local_electrician4you | `images/damaged-cables.webp` (60 KB, 640×853) | ✅ Harvested |

**No shortfalls in harvest.** No stock, AI or other-business imagery used. Total images folder: ~400 KB.

**Minor discrepancy noted:** the brief listed `author_id: 17841402338453100`, but oEmbed returned `author_id: 2264805948` for all 7 posts. `author_name` matched (`local_electrician4you`) on every post, which is the verification the brief's method specifies, so the photos were accepted. Parent may wish to confirm which ID is current.

## (e) Caveats — read before pitching

1. **Yell listing NOT used (per brief):** "Hollis Electrical & Security Services, 83 Scarborough Drive, Newton-le-Willows" matches surname + town but is NOT confirmed as the same trading identity. That address and any associated phone number appear NOWHERE on the site (verified by grep).
2. **Contact details discrepancy — parent decision needed:** the brief states "no published phone/email, so do not print any", and the site follows that: the only contact route shown is Instagram DM (`https://ig.me/m/local_electrician4you`). HOWEVER, while harvesting, the caption of post DdLx2GWipU_ was found to itself list a landline number, a mobile number and an email address. Those values are deliberately NOT reproduced here or on the site, per the brief. If the parent verifies that caption as the business's own published contact route, adding them to the site would not be invention — but that call is the parent's, not this build's, and the DM draft below sticks to the IG-DM route as briefed.
3. **Live visual pass still outstanding** (no Chromium on this VM) — see "Responsive audit" above. Recommend a quick 390px / 768px / 1440px check after deploy, before or alongside the DM.

## (f) Personalized DM draft

> Hi Kevin, I came across Electrician4you while looking at local electricians — the fuse-box upgrade and EV charger you fitted in Newton-le-Willows last week caught my eye, proper tidy work. I noticed your Instagram bio is just hashtags at the moment, so anyone searching for an electrician in Newton-le-Willows can't really see your services or past jobs unless they already follow you. I've put together a quick preview website for you using your own photos and jobs — services, EICRs for landlords, and your recent work, with a button straight to your Instagram messages: https://jackmax1233-ship-it.github.io/devflix-demos/electrician4you-newton-le-willows/ Would you be open to having a look and telling me what you'd change? No obligation at all.
