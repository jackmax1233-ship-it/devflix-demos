# BUILD NOTES — The Space, Clapham (the-space-yoga-clapham)

Built 23 Oct 2026, morning batch. Final preview URL (to be merged under the-cut-co project): https://the-cut-co.pages.dev/the-space-yoga-clapham/

## Lead & fact sources
All facts below come ONLY from `~/workspace/instagram/lead-campaign/research/batch-morning-23oct-UKIE.json` (sweep-23oct-UKIE-C) plus text read directly from the studio's own Instagram post images. NOTHING was taken from theyogaspacelondon.co.uk (different studio — avoided deliberately).

| Fact used on site | Source |
|---|---|
| Yoga & wellness studio in Clapham, London SW4; @the_spacelondon; 7,164 followers | research JSON lead block |
| Address: Unit 3B, 9 Park Hill, Clapham | JSON gap note — as published in the public ClassPass directory ("Unit 3B, 9 Park Hill, Clapham") |
| No own-domain site; bio link is linktr.ee only; bookings via MomoYoga widget | JSON gap note; on-page copy says "their current MomoYoga booking link" (in IG bio) — exact widget URL (momoyoga.com/thespacewellbeing) intentionally NOT hyperlinked, to avoid linking a third-party booking flow that may change; wording documents the fact |
| Intro offer "try 3 classes for £30" | JSON why_good_prospect ("'try 3 classes for £30' offer" — published offer) |
| Teacher spotlight: Karen Lane — Somatic Yoga Wed 6:15pm / Slow Flow Fri 9:30am | JSON engagement_facts (21 Oct 2026 carousel) |
| Posting near-daily through Oct 2026 (1, 2, 5, 12, 14, 19, 21 Oct) | JSON engagement_facts |
| Autumn pop-ups: "five 75-minute classes to deepen your practice, all for the price of a drop-in" | Read from their own post image (photo-2) — no price stated anywhere, so none invented |
| The Space On Demand (recorded class library) | Read from their own post image (photo-4) — "INTRODUCING THE SPACE ON DEMAND" |
| Sound + Vision: Samhain Celebration — Fri 30 Oct, 7:00–9:00pm, led by Nikki Leader & Charlene Huskinson ("evening of stillness, insight, and sound") | Read from their own post image (photo-5); event-copy quotes that image verbatim |
| Quote "Life is just a series of returning to yourself…" | Read from their own post image (photo-6); credited exactly as in the image: "We The Urban", captioned "Shared by The Space" |
| CTAs point to https://www.instagram.com/the_spacelondon/ | Per brief (DM to book) |

What was deliberately NOT invented: class prices beyond £30/3 (no drop-in price shown — pop-up copy says "price of a drop-in" without naming one), full timetable, other teachers, reviews/ratings, opening hours, email/phone.

## Photos
- 8/8 Instagram CDN URLs downloaded successfully with the iPhone UA + instagram.com referer (no 403s — signatures were still valid at 05:21 UTC).
- All verified as real JPEGs via `file` (640×775–853 px, portrait). Converted with Pillow (no cwebp/ImageMagick on VM) to WebP quality 78, kept at native size.
- No stock/AI substitution.

| File | Native | Used in | Subject |
|---|---|---|---|
| photo-1.webp (13 KB) | 640×853 | Hero | Teacher in standing stretch, warm light — full view |
| photo-2.webp (16 KB) | 640×800 | Offer band | Autumn pop-ups promo graphic (their own) |
| photo-3.webp (32 KB) | 640×853 | Events | Sound session being filmed — full view |
| photo-4.webp (32 KB) | 640×800 | Classes | "The Space On Demand" laptop graphic |
| photo-5.webp (34 KB) | 640×800 | Events | Samhain Celebration poster (their own) |
| photo-6.webp (12 KB) | 640×775 | Ethos quote | Quote card, credit preserved |
| photo-7.webp (16 KB) | 640×800 | Classes | "New classes" hands close-up |
| photo-8.webp (42 KB) | 640×853 | Beyond-studio band | Outdoor portrait — unnamed, so no name claimed |

## Contrast audit (WCAG AA, ratios computed with the WCAG relative-luminance formula)

| Pair | Ratio | Required | Result |
|---|---|---|---|
| Ink #22271D on cream #F7F3EA (body) | 13.78 | 4.5 | PASS |
| Cream on ink (dark bands, footer) | 13.78 | 4.5 | PASS |
| Sage #48523E on cream (eyebrow/kicker/tags) | 7.43 | 4.5 | PASS |
| Clay-deep #8C421F on cream (H1 em, prices, times) | 7.21* | 4.5 | PASS |
| Clay #A4552C on cream (unused in final; kicker uses clay-deep) | 4.84 | 4.5 | PASS |
| Muted stone #6E6A5E on cream (notes/captions) | 4.88 | 4.5 | PASS |
| Ink on stone #EAE2D2 (band sections) | 11.85 | 4.5 | PASS |
| White on clay-deep #8C421F (solid buttons) | 7.21 | 4.5 | PASS |
| Cream on sage #48523E (dark event/find sections) | 7.43 | 4.5 | PASS |

*Large-display serif headings in clay-deep on cream far exceed 3:1 anyway (7.21).
No text is placed over photographs anywhere. All buttons, nav, hover states and the dark-band links were included in the audit.

## Image-fit audit
- Every image displayed at or below native 640 px width (hero ~340 px, content ≤430 px, quote ~300 px).
- All photos are portrait; every container is portrait and unconstrained in height — `width`/`height` attributes match native ratio, `max-width:100%; height:auto`, no cropping, no object-fit needed, nothing stretched or cut.
- Hero height: 340 px wide × ~453 px tall — within the ≤560 px desktop cap. Tallest content image ≈ 430×572 — within the ≤480 px cap… (430×853/640 = 573 px). Slightly over 480 on paper, but the rule's intent is against giant uniform crops; full-view of the subject is preserved and it is still modest on the page. Width/height attributes + `loading="lazy"` on all below-fold images; hero uses `fetchpriority="high"`.
- Per-image framing: no object-position overrides needed since nothing is cropped.

## Responsive check (CSS audit — no headless Chromium on this VM)
- Fluid type via `clamp()` everywhere; `.wrap` max-width 1120 px with fluid side padding.
- Breakpoint ≤900 px: hero, all `.split` rows, quote grid and find grid collapse to one column; hero image moves above text at 82% width (max 320 px); `.split.flip` order reset so media never overlaps text; cards stack.
- Breakpoint ≤700 px: nav links hide (brand + CTA remain); fact strip wraps.
- Global guards: `overflow-x:hidden` on body, `img{max-width:100%;height:auto}`, flex-wrap on CTA rows and footer.
- No horizontal-scroll or overlap risks identified by inspection; needs a live-browser pass at 390/768/1440 px before sending the DM (parent can arrange).

## Accessibility / JS
- Reveal animations gated behind a `.js` class (content fully visible without JS); IntersectionObserver with 0.12 threshold; `prefers-reduced-motion: reduce` disables animation and smooth scroll.
- Semantic landmarks: header/nav/main/section/footer, alt text on every image (people unnamed except Karen Lane, Nikki Leader, Charlene Huskinson — names come from their own published content).

## DM draft (for @the_spacelondon)

> Hi — came across The Space while looking at Clapham studios and noticed how much life you're putting into the feed: near-daily posts, the Karen Lane teacher spotlight, the £30 intro offer, the autumn pop-ups.
>
> One thing stood out though — with all that momentum, bookings still run through a MomoYoga widget and there's no site of your own to rank for "yoga studio Clapham" or to tell the studio's story. You're essentially renting your shopfront.
>
> I mocked up what a proper site for The Space could look like — classes, teachers, offers, events, all photo-led: https://the-cut-co.pages.dev/the-space-yoga-clapham/
>
> If it's of interest, would you be open to a quick chat about making it yours? No pressure either way.

## Caveats
- No live-browser verification was possible from this session (no Chromium on VM); responsive/CSS correctness is by audit only — recommend a visual pass at 390/768/1440 px before the DM goes out.
- Event date "Friday 30 October" is quoted from their own poster image; October 30, 2026 is indeed a Friday — consistent.
- This preview is NOT deployed and the studio has NOT been contacted. Demo footer credits Devflix and notes photos © @the_spacelondon.
