# BUILD NOTES — ProShield Pest Control Solutions (Karachi)

- **Slug:** `proshield-pest-control-karachi`
- **Local dir:** `~/workspace/instagram/lead-campaign/sites/proshield-pest-control-karachi/`
- **Preview link (for DM, NOT yet deployed by this task):** https://jackmax1233-ship-it.github.io/devflix-demos/proshield-pest-control-karachi/
- **Built:** Sun 25 Oct 2026, Devflix outreach morning batch. No DM sent, no tracker edited, no deploy made by this task.
- **Design identity:** Trustworthy trade look — deep green `#10382B` + warm amber `#E8A33D` on warm cream `#FAF7F0`. Fonts: Archivo (headings) + Inter (body), 2 families, `display=swap`. No gradients, no glassmorphism, no floating cards.

## (a) Contrast table (WCAG AA: ≥4.5:1 normal text, ≥3:1 large text)

| Foreground | Background | Ratio | Use | Pass |
|---|---|---|---|---|
| #FFFFFF | #10382B (deep green) | 12.94 | Hero text, nav, footer | ✅ |
| #FAF7F0 | #14352A (ink) | 12.48 | Body text on cream | ✅ |
| #E8A33D (amber) | #14352A | 6.19 | Brand accent / eyebrow on cream sections | ✅ |
| #14352A | #E8A33D | 6.00 | Amber button label | ✅ |
| #14352A | #F2B45C (amber hover) | 7.29 | Amber button hover label | ✅ |
| #FFFFFF | #1E5C40 (step cards) | 7.89 | IPM step headings | ✅ |
| #E9EFEA | #10382B | 11.09 | Hero body / dark-section body | ✅ |
| #C9D8CF | #10382B | 8.76 | Hero note + hero figcaption | ✅ |
| #D9E8DC | #10382B | 10.19 | Footer text | ✅ |
| #33473C | #FAF7F0 | 9.31 | Section ledes | ✅ |
| #3A4B41 | #FFFFFF | 9.28 | Card body text | ✅ |
| #47574D | #FAF7F0 | 7.17 | Figcaptions (13px, small text) | ✅ |
| #E8A33D | #10382B | 6.00 | Step numbers (30px, large text) | ✅ |

**Contrast pass: 13/13.** Note: an earlier figcaption grey `#6B7A70` measured 4.23:1 and was replaced with `#47574D` (7.17:1) before delivery. Amber is never used as small text on white/cream — only on dark green, or as a button background with dark text.

## (b) Image-fit audit

All harvested images are the business's own Instagram thumbnails at 640px wide (the oEmbed ceiling). Natural orientations: 640×801 (4:5 portrait) for hero/service photos; 640×640 (1:1 square) for the IPM and coverage graphics.

| File | Natural size | Container | Fit | Max height | Full view? |
|---|---|---|---|---|---|
| hero-team.webp | 640×801 (4:5) | 4:5 frame | cover (no crop — frame ratio = photo ratio) | 520px desktop, 480px ≤900px, 440px ≤560px | ✅ |
| service-1..5.webp | 640×801 (4:5) | 4:5 frame | cover (no crop — frame ratio = photo ratio) | 340px | ✅ |
| ipm.webp | 640×640 (1:1) | 1:1 frame | cover (no crop — frame ratio = photo ratio) | 480px | ✅ |
| coverage-area.webp | 640×640 (1:1) | 180×180 square thumb | cover (no crop — frame ratio = photo ratio) | 180px | ✅ |

No image is stretched, distorted, or cropped in any dimension. No stock/AI/other-business imagery used.

## (c) Fact sources (every claim traced)

| Claim on the site | Source |
|---|---|
| Business name, Karachi, pest control / fumigation | Task brief + @proshieldpestcontrolsolutions IG profile/posts |
| Integrated Pest Management experts; IPM = Identify, Inspect, Treat, Prevent; "isn't just spraying chemicals" | IG post DeyKs6nIGOt ("What is IPM?") caption, verbatim concept |
| Led by a qualified entomologist | Task brief published facts |
| Residential and commercial services; homes, offices, restaurants, factories | IG post De0vuiQkRKs ("Coverage Area") caption |
| Services: ants, cockroach, termite, bed bug, rodent, mosquito control + fumigation | Task brief published facts, corroborated by post hashtags (#cockroachcontrolservice, #fumigationservice) |
| Serving Karachi and expanding across Pakistan | IG post De0vuiQkRKs caption, verbatim |
| Phone 0334-2666994 + "Free Inspection" | Business's own IG bio (published details) — shown as tel:+923342666994 |
| Instagram DM route https://ig.me/m/proshieldpestcontrolsolutions | Task brief CTA |
| **NOT claimed:** no prices, no reviews/ratings, no guarantees, no "best in Karachi", no invented stats | Deliberate — none published by the business |
| **NOT used:** proshield.ae (Dubai) and US ProShield companies | Explicitly excluded per brief; no facts taken from them |

## (d) Photo harvest log (10 attempted, 8 used)

Method: public oEmbed endpoint with iPhone UA; `author_name` verified = `proshieldpestcontrolsolutions` for every shortcode; CDN thumbnails downloaded with browser UA + Instagram Referer; converted to WebP quality 78 via Python PIL. 640px is the oEmbed ceiling.

| Shortcode (post date) | File | Result |
|---|---|---|
| De3TaofkYR2 (2026-10-23) | hero-team.webp (61,500 B) | ✅ harvested |
| DeyKs6nIGOt (2026-10-21) | ipm.webp (26,332 B) | ✅ harvested |
| De0vuiQkRKs (2026-10-22) | coverage-area.webp (22,724 B) | ✅ harvested |
| De0vQDLDpzi (2026-10-22) | service-1.webp (46,980 B) | ✅ harvested |
| DeyKBabjnxc (2026-10-21) | service-2.webp (53,426 B) | ✅ harvested |
| DevjsHVkWLa (2026-10-20) | service-3.webp (69,308 B) | ✅ harvested |
| DetRYcWj0K6 (2026-10-20) | service-4.webp (52,450 B) | ✅ harvested |
| Des69UngKC3 (2026-10-19) | service-5.webp (57,050 B) | ✅ harvested |
| DevjqjGFQmw (2026-10-20) | — | Not used; 8-image target already met, no shortfall to cover |
| DetAbcrgq0E (2026-10-19) | — | Not used; 8-image target already met, no shortfall to cover |

**Harvest shortfall: none.** All 10 oEmbed calls returned the correct author; 8 were downloaded and used. The 2 unused shortcodes were valid but surplus — documented here, not substituted with anything else.

## (e) DM draft (personalized, for the parent agent to send — NOT sent by this task)

> Hi ProShield team — I came across your page while looking at pest control services in Karachi, and your post explaining IPM as Identify, Inspect, Treat, Prevent stood out; most pages just say "spraying", you actually explain the method.
>
> One thing I noticed: your bio has your number but no website link, so anyone searching for a pest control service in Karachi can't find you outside Instagram. I made you a simple one-page site with your services, the IPM method, and your free inspection number so people can reach you directly: https://jackmax1233-ship-it.github.io/devflix-demos/proshield-pest-control-karachi/
>
> Would something like that be useful for you?

## Responsiveness & verification notes

- Layout: 3-col services grid → 2-col ≤900px → 1-col ≤560px; IPM steps 4 → 2 → 1; hero grid stacks ≤900px; header wraps/stacks on mobile. No fixed widths, no absolute positioning, all images `max-width:100%`.
- **Honest caveat:** this VM has no Chromium, so the responsive check is a careful CSS audit only — a live visual pass at ~390px / ~768px / ~1440px is still recommended before the pitch goes out.
- All image paths are relative (`images/xxx.webp`), no leading slash, no absolute URLs, no base64 — GitHub Pages subpath deploy compatible.
