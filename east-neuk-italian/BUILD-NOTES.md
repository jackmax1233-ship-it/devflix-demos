# East Neuk Italian — Preview Site Build Notes

Built: Sun 25 Oct 2026, for the Devflix afternoon outreach batch.
Folder: `instagram/lead-campaign/sites/east-neuk-italian/` — `index.html` + `images/` (5 WebP files) + this file.
No DM sent. Tracker not edited.

## Design
Warm Italian-inspired editorial design: cream background, terracotta accents, olive venue rules,
Fraunces (display serif) + Inter (body sans) — 2 font families only. No gradients, no glassmorphism,
no generic AI look. Mobile-first CSS: fluid widths, `max-width: 100%` on all images, grids that
collapse to a single column below 768px, one media query at 768px, no fixed pixel widths on text
containers. Audit at ~390px / ~768px / ~1440px is by CSS audit (no live-browser tool available to
this subagent): no horizontal overflow sources — all containers are `max-width: 1100px` with
percentage/fluid padding, nav wraps, grids stack.

## Contrast table (WCAG AA: 4.5:1 normal text, 3:1 large text)
Ratios computed from relative luminance of the exact hex pairs used.

| Text / foreground | Background | Ratio | Pass? |
|---|---|---|---|
| Ink #2E2013 (body, headings, nav) | Cream #FDF6EC | 14.69:1 | ✅ AA (normal + large) |
| Ink #2E2013 (body) | Cream-2 #F5E6CE (alt sections) | 12.83:1 | ✅ AA |
| Terracotta-dark #7A2E1F (eyebrow, links, price) | Cream #FDF6EC | 8.74:1 | ✅ AA |
| Olive #3D5A3A (venue rule only, no text) | Cream #FDF6EC | 7.19:1 | n/a decorative |
| White #FFFFFF (button label) | Terracotta #8F3423 (button) | 7.83:1 | ✅ AA |
| White #FFFFFF (taster heading/body) | Terracotta #8F3423 (taster panel) | 7.83:1 | ✅ AA |
| Terracotta-dark #7A2E1F (light button label) | White #FFFFFF (light button) | 8.74:1 | ✅ AA |
| Cream #FDF6EC (footer text/links) | Ink #2E2013 (footer) | 14.69:1 | ✅ AA |
| Brown #5C3A1E (captions, small print) | Cream #FDF6EC | 10.10:1 | ✅ AA |

No text sits over a photograph. All text-over-colour pairs pass AA.

## Image-fit audit (full view — no cropping of any subject)
All images are the business's own Instagram thumbnails (640px ceiling), converted to WebP at
quality 78, with `width`/`height` attributes and `height: auto`. No `object-fit: cover` is used
anywhere, so nothing is cropped; frames follow each photo's natural ratio.

| File | Source post | Natural size / ratio | Placement | Fit check |
|---|---|---|---|---|
| `images/classroom.webp` | DeW1_kxCMwi | 640×853, portrait 3:4 | Hero, max-height 560px, width auto | Full view: whole screen, bookshelves, chairs and laptop visible; height cap scales width proportionally, no crop |
| `images/poster.webp` | DeHVqXgo-5q | 640×439, landscape ~3:2 | Classes, container max-width 480px → height ≈ 329px | Full view: whole hand-drawn poster, all handwriting legible, no crop |
| `images/dundee.webp` | Dd4E-slCOkY | 640×360, landscape 16:9 | Venues, container max-width 600px → height ≈ 338px | Full view: whole V&A/ship graphic and all overlaid text visible, no crop |
| `images/venice.webp` | DctI9KMo7oE | 640×853, portrait 3:4 | Gallery, max-height 340px, width auto | Full view: whole lion statue, building and both text boxes visible, no crop |
| `images/taster.webp` | De6YsYroxN1 | 640×839, portrait 3:4 | Gallery, max-height 340px, width auto | Full view: whole lion statue and taster text visible, no crop |

Hero ≤ 560px tall (desktop) ✅. Card/gallery images ≤ ~340px tall ✅. Below-fold images lazy-load ✅.
No base64 images ✅. All image paths relative (`images/*.webp`), no leading `/` ✅.

## Fact sources (verified only — nothing invented)
- Business: East Neuk Italian, Instagram @eastneukitalian, 156 followers, East Neuk / St Andrews /
  Dundee, Scotland. Language school: Italian, in-person classes. (Task brief.)
- Free taster 11am–12pm via Zoom, no previous experience required, link on request:
  post https://www.instagram.com/p/De6YsYroxN1/ (25 Oct 2026; caption + graphic text).
  The site words this as "announced 25 Oct 2026 — message for the next session" so a past
  date is never presented as upcoming.
- Sunday beginners class at Space café, St Andrews; intermediate group (congiuntivo) same mornings:
  post https://www.instagram.com/p/DeW1_kxCMwi/ (11 Oct 2026).
- Beginners course, Sundays 11am–12pm, Space Café, St Andrews; hand-drawn (not AI) poster:
  post https://www.instagram.com/p/DeHVqXgo-5q/.
- Conversation cafés; Dundee hybrid course in negotiation at time of posting:
  post https://www.instagram.com/p/Dd4E-slCOkY/ — its graphic gives the Dundee format used on
  the site: Thursdays 8pm online, Saturdays 12pm in person, £110 per person.
- Autumn registration / link-in-bio post: https://www.instagram.com/p/DctI9KMo7oE/.
- Course prices £100–£110 range: task brief (as published). The site states the range only,
  plus the £110 figure exactly as shown in the school's own Dundee graphic.
- Venues named: Space café St Andrews, East Neuk Centre Anstruther, Dundee (task brief + posts).
- Bio link is only a Google Form (forms.gle), no website: task brief. The site therefore says
  "the enrolment form linked in the school's Instagram bio" and fabricates no URL.
- NOT invented: no email, phone, street address, course length, reviews, ratings, student
  numbers or extra course levels. Enrolment CTA links to https://www.instagram.com/eastneukitalian/.

## Photo harvest log (public oEmbed, 25 Oct 2026)
Method: `curl -A "Mozilla/5.0 (iPhone; CPU iPhone OS 17_0 like Mac OS X)"
"https://www.instagram.com/api/v1/oembed/?url=https://www.instagram.com/p/<ID>/"`,
then download of `thumbnail_url` with a browser Referer/UA. All 5 posts returned
`author_name: eastneukitalian` — match verified for every photo. No login used.

| Post | Result |
|---|---|
| De6YsYroxN1 | ✅ 640×839, taster graphic over Venice lion statue |
| DeW1_kxCMwi | ✅ 640×853, classroom screen "Presentiamoci! Lesson 1 – Italian for Beginners" |
| DeHVqXgo-5q | ✅ 640×439, hand-drawn "Italian for Beginners" poster (text graphic — used as such, captioned honestly) |
| Dd4E-slCOkY | ✅ 640×360, Dundee graphic (text graphic — used as such, captioned honestly) |
| DctI9KMo7oE | ✅ 640×853, autumn registration graphic over Venice lion statue |

Photo shortfall: **none** — 5 of 5 posts yielded usable photos. No stock or AI photos used.

## Verification (before finishing)
- `index.html` present ✅
- Every `images/*.webp` reference resolves to an existing file (5/5) ✅
- 0 base64 strings ✅
- 0 absolute asset paths ✅
- `BUILD-NOTES.md` present ✅

## DM draft (for the parent agent — do not send from this task)
> Hi! I came across East Neuk Italian and loved the hand-drawn beginners poster — the one drawn
> with your toddler instead of an AI poster really stood out. I noticed your bio link goes to a
> Google Form, so course details and prices only live in your captions — anyone finding you
> outside Instagram can't see what you offer at a glance.
>
> I've put together a preview website for you using your own photos and posts, with your
> classes, venues, prices and the free taster all on one page: [PREVIEW LINK]
>
> Would you like a look, and is a proper website something you'd want for the school?
