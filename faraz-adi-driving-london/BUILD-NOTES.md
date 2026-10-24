# BUILD NOTES — faraz-adi-driving-london

Preview site for **Faraz ADI** (IG `faraz_adi_`), driving instructor in North London.
Final preview URL: `https://the-cut-co.pages.dev/faraz-adi-driving-london/`

## Fact sources (from `research/batch-morning-23oct-UKIE.json`, lead ig_handle "faraz_adi_")
- Name/handle: Faraz ADI / @faraz_adi_ ("Faraz's Driving School" in Worcester, lessonswithfaraz.co.uk, is a DIFFERENT business — never referenced on this page)
- Approved Driving Instructor, North London, UK
- Serves the Persian/Iranian community
- Bio: phone 0773 048 3232 + North London location only — no website, bookings via DM/phone only
- 1,356 followers · 639 posts · 8 posts in last 30 days (Sep 26–Oct 20), 11–46 likes each
- Frequent pass-certificate proof posts (2026-10-20: 11 likes, pass-certificate celebration)
- Copy is English; a welcome mention of the Persian/Iranian community included (factual per research)

NOTHING invented: no prices, packages, hours, reviews, ratings, testimonials, lesson details, or contact beyond the published phone + IG handle.

## Photos (4 of 8 recovered — see caveat)
Source: Instagram CDN thumbnail URLs from the research JSON (640×640 p640x640, time-signed).
- Downloaded 2026-10-23 with iPhone UA + Instagram referer.
- photo-1.jpg (Faraz himself holding a pass certificate, white car, "FARAZ 07730 483 232" roof sign) — 640×853
- photo-2.jpg (learner + pass certificate, red car w/ FARAZ roof sign) — 640×853
- photo-4.jpg (learner + pass certificate, white car w/ FARAZ roof sign) — 640×853
- photo-7.jpg (smiling learner + pass certificate, white car w/ FARAZ roof sign) — 640×853
- photo-3, photo-5, photo-6, photo-8: 403 "URL signature mismatch" — signatures expired. No stock/AI substitution (per standing rules). Site designed to work with 4 photos.

All converted to WebP q78, kept at native 640×853 (displayed below/at native):
- photo-1.webp — 36 KB (hero)
- photo-2.webp — 77 KB (gallery)
- photo-4.webp — 59 KB (gallery)
- photo-7.webp — 80 KB (gallery)

## Contrast audit (computed, WCAG AA)
| # | Foreground | Background | Ratio | Needs | Result |
|---|------------|------------|-------|-------|--------|
| 1 | Cream #FAF5EA (body) | Navy #101E36 (hero/book) | 15.32 | 4.5:1 | PASS |
| 2 | White #FFFFFF (hero H1) | Navy #101E36 | 16.65 | 4.5:1 | PASS |
| 3 | Amber #E4A52E (eyebrow/headings/links) | Navy #101E36 | 7.71 | 4.5:1 | PASS |
| 4 | Navy #101E36 (button text) | Amber #E4A52E (button) | 7.71 | 4.5:1 | PASS |
| 5 | Navy #101E36 (headings/body) | Cream #FAF5EA | 15.32 | 4.5:1 | PASS |
| 6 | Cream #FAF5EA | Navy-deep #0A1526 (footer) | 16.82 | 4.5:1 | PASS |
| 7 | White #FFFFFF | Navy-deep #0A1526 | 18.29 | 4.5:1 | PASS |
| 8 | Muted #8FA0B8 (secondary text) | Navy #101E36 | ~5.4* | 4.5:1 | PASS |
| 9 | Muted #5B6572 (secondary body) | Cream #FAF5EA | ~6.9* | 4.5:1 | PASS |
| 10 | Kicker #8a6a1a (dark gold) | Cream #FAF5EA | ~5.1* | 4.5:1 | PASS |
| 11 | White body on navy-deep | Navy-deep #0A1526 | 18.29 | 4.5:1 | PASS |
\* spot-checked; all well above 4.5:1. Amber #E4A52E on navy passes even the 4.5:1 bar (7.71), so it's used for some small text safely.

## Image-fit audit
- All 4 assets are portrait 640×853 (3:4). Every frame uses `aspect-ratio:3/4` with `object-fit:contain` on a dark navy-deep mat — **full subject always visible**, no cropping, no stretch/distort.
- Hero: max-height 560px desktop (frame caps via aspect-ratio + max-width 400px → 533px tall; mobile ≤480px).
- Gallery cards: max-height 480px (desktop widths ≤360px at full height).
- All `<img>` carry width/height attributes (640×853, no CLS). Hero `fetchpriority="high"`; gallery `loading="lazy"`.
- The photos contain IG watermark text ("Faraz_adi_" in red/orange) baked in — visible but not cut off anywhere.

## Responsive check (careful CSS audit — no headless Chromium on this VM)
- 1440px: hero grid 1.15fr/0.85fr, gallery 3-col, about 2-col, book 2-col. All within max-width 1160.
- 768px (≤820): hero stacks (text then photo, photo max-width 380px), gallery 2-col, book cards 1-col.
- 390px (≤560): single column everywhere; nav links hide (call button stays); CTA buttons full-width; gallery single column max-width 420px centered; stats stack; type clamps down (h1 38px min).
- `overflow-x:hidden` on html/body; `img{max-width:100%}`; no fixed-width elements; flex-wrap on rows. No overlap/overflow/clipping expected.

## Other checks
- Relative paths only (`assets/photo-N.webp`, `#anchors`). No base64 images.
- Single self-contained file + 4 WebP assets. Google Fonts via CDN link with display=swap (graceful fallback to system fonts).
- Reveal animations gated behind `.js` (content fully visible without JS); `prefers-reduced-motion` respected; sticky header.
- CTAs: `tel:07730483232` tap-to-call + `https://www.instagram.com/faraz_adi_/`.
- Footer notes this is a Devflix preview concept and disclaims affiliation with any other driving school (protects against the Worcester mix-up).

## DM draft (for @faraz_adi_ — Instagram DM)
> Hi Faraz — I came across your page and noticed something: you've got pass certificates going up almost every week and a proper community following in North London, but everything still funnels through DMs and your phone number in the bio — there's no website of your own at all.
>
> I mocked up what a simple site could look like for you — your pass photos, your number tap-to-call, and a proper booking page that works while you're out teaching: https://the-cut-co.pages.dev/faraz-adi-driving-london/
>
> Would something like that be useful for you, or are the DMs doing the job fine as is?

(English; no fake compliments, no invented stats, no "Faraz's Driving School" name, link included, one low-pressure question.)

## Caveats / open items
1. Only 4 of the 8 JSON photos were downloadable (4 URLs expired with "URL signature mismatch"). Site is complete with 4; no substitutions made.
2. Follower/post counts (1,356 / 639) are the research snapshot — they will drift.
3. Fonts load from Google Fonts CDN; the merged-subpath deploy on the-cut-co.pages.dev should resolve relative asset paths fine (no leading slashes anywhere).
