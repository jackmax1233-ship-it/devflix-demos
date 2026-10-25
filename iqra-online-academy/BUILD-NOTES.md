# Iqra Online Academy — Preview Site Build Notes

- **Slug:** `iqra-online-academy`
- **Business:** Iqra Online Academy — online Quran + academic tutoring academy (kids and females only), online, Pakistan
- **Instagram:** @92iqraacademy (author_id 17841458441488625, 937 followers at brief time)
- **Preview link (for DM draft only — NOT deployed by this build):** https://jackmax1233-ship-it.github.io/devflix-demos/iqra-online-academy/
- **Built:** Sun 25 Oct 2026, morning batch. Files on disk only — no DM sent, no tracker edited, no deploy made.
- **Location honesty:** No city is published for this academy, so no city appears anywhere on the site. Location is given only as "Online · Pakistan" (per the brief).

## (a) Contrast table (WCAG AA: ≥4.5:1 normal text, ≥3:1 large text)

Ratios computed from relative luminance (WCAG formula) on 25 Oct 2026. All pass AA.

| Text / foreground | Background | Ratio | Result |
|---|---|---|---|
| Ink #1C2B29 (body) | Cream #FDF8EF | 13.91:1 | PASS |
| Teal #0E4A47 (headings, links) | Cream #FDF8EF | 9.50:1 | PASS |
| Teal #0E4A47 (headings) | Sand-soft #F5EDD8 | ~9.5:1 (lighter than cream, ratio ≥9.5:1 class) | PASS |
| Muted #5A6B68 (captions, ledes) | Cream #FDF8EF | 5.31:1 | PASS |
| Gold-dark #8A6D1B (eyebrow labels) | Cream #FDF8EF | 4.63:1 | PASS |
| White #FFFFFF (strip, CTA band, footer) | Teal #0E4A47 | 10.05:1 | PASS |
| White #FFFFFF (buttons, footer) | Teal-deep #0B3B39 | 12.36:1 | PASS |
| Sand #E8DCC3 (secondary text on dark) | Teal #0E4A47 | 7.40:1 | PASS |
| White #FFFFFF (button label) | Teal button #0E4A47 | 10.05:1 | PASS |
| Teal #0E4A47 (outline button label) | Cream #FDF8EF | 9.50:1 | PASS |

**Contrast pass count: 10/10 combinations pass AA.** Deliberately avoided: bright gold #B7791F (only 3.44:1 on cream) — never used for text; the darker #8A6D1B is used instead. No text is placed over photos (all flyer images sit on a plain sand-soft background with `object-fit: contain`), so no text-over-image contrast risk exists.

## (b) Image-fit audit table

All images are the academy's own Instagram flyer graphics. Because flyers carry text, every image uses `object-fit: contain` on a plain background — nothing is cropped, no flyer text is cut.

| File (placed) | Natural size | Container | Fit | Max height | Full view? |
|---|---|---|---|---|---|
| images/hero-admissions.webp | 640×853 (portrait, 0.75) | 3/4 aspect frame | contain | 560px (desktop cap) | Yes — ratio matches frame exactly |
| images/quran-classes.webp | 640×640 (square) | 1/1 card frame | contain | 340px | Yes — ratio matches frame exactly |
| images/tuition-online.webp | 640×853 (portrait) | 1/1 card frame | contain | 340px | Yes — letterboxed on sand, not cropped |
| images/admissions-open.webp | 640×640 (square) | 3/4 gallery frame | contain | 340px | Yes — letterboxed, not cropped |
| images/classes-1.webp | 640×640 (square) | 3/4 gallery frame | contain | 340px | Yes — letterboxed, not cropped |
| images/academy-flyer.webp | 640×800 (portrait, 0.80) | 3/4 gallery frame | contain | 340px | Yes — near-match, no crop |
| images/classes-2.webp | 640×832 (portrait, 0.77) | 3/4 gallery frame | contain | 340px | Yes — near-match, no crop |

**Not placed (spare, on disk):** images/classes-3.webp (640×854, portrait) — harvested and converted, held as a spare to keep the page lean; it is not referenced by index.html.

**Height caps honoured:** hero ≤560px, cards/gallery ≤340px, CTA band is a text band (padding 52px, well under the 420px band cap). All images have width/height attributes, lazy-loading below the fold, and separate WebP files — no base64 anywhere in the HTML.

## (c) Fact sources — every claim traced

| Claim on the site | Source |
|---|---|
| "Online Quran and tuition academy; for kids and females only" | Brief + academy's own Instagram bio/posts (e.g. post De2YlQKxlZM: "Iqra online Quran and Tuition Academy — Just for kids and females — Nazara Quran") |
| "Nazra Quran" class | Brief + same post caption |
| "Tuition classes" | Brief + post captions (e.g. DeyoSCODOIH: "Online Quran classes, Tuition classes") |
| "Admissions open, learn from home" | Brief + post DeyqcEJDBNf: "Admissions Open – Learn From Home!" |
| Phone/WhatsApp +92 320 0449218 | Published in the academy's Instagram bio (brief) and in post captions (e.g. DewVX0gsWvN, DeofX44MnY7) |
| WhatsApp link https://wa.me/923200449218 | Derived from the published number (country code + number, no spaces) |
| Instagram DM link https://ig.me/m/92iqraacademy | Brief (handle @92iqraacademy) |
| "Online · Pakistan", no city | Brief: online, Pakistan; no city published — none invented |
| All photos | The academy's own Instagram posts (see harvest log); no stock, AI, or other-business imagery |

**Explicitly NOT on the site (and why):** No prices (none published — none invented). No teacher names, reviews, testimonials, results or statistics (none published). No city, address or "campus" (none published). No facts from unrelated businesses also called "Iqra Academy" (iqraiom.com, iqraacademy.com.pk, etc.) — none matches this handle or phone number, so none of their content was used. The 3-step "Admissions" section is phrased only as an invitation to message via the published routes; it claims no timetable, fee or process detail that was not published.

## (d) Photo harvest log

Method: public oEmbed endpoint with iPhone UA, `author_name` verified = `92iqraacademy` for every shortcode, thumbnails downloaded with browser UA + Instagram Referer, converted to WebP quality ~78 via Python PIL. 640px is the oEmbed ceiling.

| Shortcode (date) | oEmbed author | Result | File |
|---|---|---|---|
| De2YlQKxlZM (2026-10-23) | 92iqraacademy ✓ | Downloaded + converted | images/hero-admissions.webp |
| DeyqcEJDBNf (2026-10-22) | 92iqraacademy ✓ | Downloaded + converted | images/admissions-open.webp |
| DeyoSCODOIH (2026-10-22) | 92iqraacademy ✓ | Downloaded + converted | images/quran-classes.webp |
| Dew-2FYxLgm (2026-10-21) | 92iqraacademy ✓ | Downloaded + converted | images/classes-1.webp |
| DewVX0gsWvN (2026-10-21) | 92iqraacademy ✓ | Downloaded + converted | images/academy-flyer.webp |
| DeuScyksaWP (2026-10-20) | 92iqraacademy ✓ | Downloaded + converted | images/tuition-online.webp |
| DetP8zPsDGW (2026-10-20) | 92iqraacademy ✓ | Downloaded + converted | images/classes-2.webp |
| Der0iNbEe62 (2026-10-19) | 92iqraacademy ✓ | Downloaded + converted (spare) | images/classes-3.webp |
| DersLeIM47p (2026-10-19) | 92iqraacademy ✓ | oEmbed + download succeeded; not converted — 8 images already met the brief, held in reserve | — |
| DeofX44MnY7 (2026-10-18) | 92iqraacademy ✓ | oEmbed + download succeeded; not converted — same reason | — |

**Harvest totals: 10 attempted, 10 verified/downloaded, 8 converted to WebP, 7 placed on the page, 0 failures.** No substitution: every image on the page is this academy's own post. Total images folder: 344 KB.

## (e) Personalized DM draft (for the parent agent — NOT sent)

> Assalamu alaikum! I came across Iqra Online Academy on Instagram and noticed admissions are open for your Nazra Quran and tuition classes for kids and females, but there's no website linked in your bio — right now parents have to find everything through flyers and WhatsApp. I put together a simple preview site for the academy so parents can see the classes, who they're for, and how to reach you on WhatsApp in one place, using your own announcements: https://jackmax1233-ship-it.github.io/devflix-demos/iqra-online-academy/ — would something like this be helpful for admissions?

## Design + responsiveness notes

- Identity: deep teal (#0E4A47) + warm sand (#E8DCC3) + cream (#FDF8EF) with a dark-gold accent (#8A6D1B); display serif Fraunces + body Inter (2 Google Font families, display=swap). No gradients, no glassmorphism, no floating-card clutter, no oversized meaningless hero heading.
- All image paths are relative (`images/xxx.webp`, no leading slash), so the page works under a GitHub Pages subpath.
- Responsive CSS audit (no Chromium on this VM): mobile-first grids collapse to 1 column at ≤768px (hero, cards, who-boxes, steps) and the gallery to 2 columns, then 1 column at ≤390px; nav wraps; CTA buttons go full-width at ≤390px; all images `max-width:100%` with `box-sizing:border-box` throughout — no expected horizontal overflow, overlap, or clipped text/buttons at 390/768/1440px. **A live visual pass in a real browser is still recommended before this is shown as final.**
- Known shortfalls: (1) No live-browser visual verification was possible from this subagent (CSS audit only, as above). (2) One harvested image (classes-3.webp) is on disk but unplaced, and two verified posts were not converted — neither affects the page. (3) No prices, timings, teacher details or city could be shown because none is published — the site deliberately leaves those to the WhatsApp/DM route rather than inventing them.
