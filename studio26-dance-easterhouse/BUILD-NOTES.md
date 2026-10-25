# Studio 26 Dance Company — Preview Site Build Notes

## Business
Studio 26 Dance Company — Instagram @studio26dancecompany, 165 followers, Easterhouse, Glasgow, UK. Dance studio.

## Fact sources (verified facts only — nothing else invented)
- Styles: lyrical, commercial/hip-hop, freestyle (task brief).
- New competition team launched Aug 2026 (task brief).
- Based at Phoenix Community Centre, Easterhouse (task brief).
- Latest posts: 11 Oct 2026 ("Limited spaces available… come join our dance family! We are based in Easterhouse", 12 likes), 2 Oct (10 likes), 1 Oct (12 likes, 2 comments) (task brief).
- Gap: no website and no bio link at all — joining is by IG message only (task brief).
- Engagement described only as modest (6–17 likes) and proportionate at 165 followers — not inflated anywhere on the site.
- No class times, prices, ages, teachers, reviews, ratings or contact details beyond the above were invented. Where the site lacks them, it says so explicitly ("No class times or prices are listed here yet").
- Join CTA links to https://www.instagram.com/studio26dancecompany/

## Photo harvest log (public Instagram oEmbed, 25 Oct 2026)
All six oEmbed responses returned author_name `studio26dancecompany`, matching the business handle. Thumbnails downloaded with a browser Referer/UA (640px ceiling), converted to WebP quality 78 with Pillow. No stock or AI photos used.

| Post URL | File | Source size | WebP | Use |
|---|---|---|---|---|
| https://www.instagram.com/p/DeWTublMWBI/ | images/hero.webp | 640×853 (portrait) | ~108 KB | Hero |
| https://www.instagram.com/p/Dd_LGQbsN9d/ | images/lyrical.webp | 640×853 (portrait) | ~87 KB | Gallery — open lyrical class (caption-verified) |
| https://www.instagram.com/p/Dd9vdkpDNrn/ | images/class.webp | 480×640 (portrait) | ~13 KB | Gallery — dancers learning a routine |
| https://www.instagram.com/p/DdWz4Hus9Aj/ | images/bestie.webp | 640×853 (portrait) | ~103 KB | Gallery — bring-a-bestie night |
| https://www.instagram.com/p/DcMZ7zVMZFK/ | images/group.webp | 640×640 (square) | ~26 KB | Gallery — busy class night |
| https://www.instagram.com/p/DcB4PjDM-6C/ | images/friends.webp | 640×853 (portrait) | ~95 KB | Gallery — dancing with friends |

Photo shortfall: NONE — all 6 requested posts yielded a usable photo.

## Design
Youthful editorial dance-company identity, distinct from a generic template: cream paper background, deep coral-red accent, mustard highlight, ink text, Fraunces display serif + DM Sans body (2 font families). No purple/blue/pink gradients, no glassmorphism, no decorative icon clutter.

## Contrast table (WCAG AA — computed by relative luminance; all pass)
| Text / foreground | Background | Ratio | Requirement | Result |
|---|---|---|---|---|
| #1C1A17 ink on #FFF6E9 cream | #FFF6E9 | 16.21:1 | 4.5:1 normal | Pass |
| #FFF6E9 cream on #1C1A17 ink | #1C1A17 | 16.21:1 | 4.5:1 normal | Pass |
| #33302B body on #FFF6E9 cream | #FFF6E9 | 12.27:1 | 4.5:1 normal | Pass |
| #5A5348 muted caption on #FFF6E9 cream | #FFF6E9 | 7.09:1 | 4.5:1 normal | Pass |
| #A82315 coral heading/accent on #FFF6E9 cream | #FFF6E9 | 6.72:1 | 4.5:1 normal / 3:1 large | Pass |
| #FFFFFF white on #A82315 coral button | #A82315 | 7.20:1 | 4.5:1 normal | Pass |
| #FFFFFF white on #7A1A10 coral hover | #7A1A10 | 10.59:1 | 4.5:1 normal | Pass |
| #1C1A17 ink on #F2C14E mustard | #F2C14E | 10.35:1 | 4.5:1 normal | Pass |
| #FFF6E9 cream on #7A1A10 deep coral (team text block context) | — | 9.89:1 | 4.5:1 normal | Pass |

Buttons, nav links, hover/focus states, footer and text over colour blocks all use pairs from this table. No text sits over a photo.

## Image-fit audit (per image — full view, no dancer cut)
| Image | Natural ratio | Container | Fit | Check |
|---|---|---|---|---|
| hero.webp | 3:4 portrait | aspect-ratio 3/4, max-height 560px | object-fit: contain | Frame matches natural ratio; full dancer visible, no crop |
| lyrical.webp | 3:4 portrait | aspect-ratio 3/4, max-height 340px | object-fit: contain | Frame matches; full view |
| class.webp | 3:4 portrait (480×640) | aspect-ratio 3/4, max-height 340px | object-fit: contain | Frame matches; full view |
| bestie.webp | 3:4 portrait | aspect-ratio 3/4, max-height 340px | object-fit: contain | Frame matches; full view |
| group.webp | 1:1 square | aspect-ratio 1/1, max-height 340px | object-fit: contain | Frame matches; full view |
| friends.webp | 3:4 portrait | aspect-ratio 3/4, max-height 340px | object-fit: contain | Frame matches; full view |

object-fit: cover is NOT used for any business photo. Hero is capped at 560px tall; gallery images at 340px tall.

## Responsive audit (CSS audit — no live browser available to this subagent)
- Mobile-first fluid layout: `box-sizing: border-box`, all images `max-width: 100%`, wrappers `max-width: 1100px`.
- Hero grid 2-column → 1-column at ≤768px; gallery 3 → 2 columns at ≤768px → 1 column at ≤480px; class rows narrow at ≤768px.
- Buttons go full-width at ≤480px so no clipped text/buttons; nav wraps; `clamp()` headings scale from ~390px to 1440px.
- No fixed pixel widths on content blocks, no horizontal-scroll risk from full-width elements. Parent agent: please verify live at ~390px / ~768px / ~1440px before the DM goes out, as this subagent cannot operate the live browser.

## Structure
Hero (name, Easterhouse, limited spaces, join CTA) → styles strip → Classes (lyrical, commercial/hip-hop, freestyle) → Competition team (new, Aug 2026) → Gallery (business's own photos) → Location (Phoenix Community Centre, Easterhouse) → Join (Instagram message) → Footer disclaimer: preview concept made by Devflix, final site subject to the business's approval.

## Relative paths / no base64
All image references are relative (`images/*.webp`), no leading `/`, no absolute paths, no base64. External links only: Google Fonts stylesheet and the Instagram profile.

## DM draft (for the parent agent — DO NOT SEND from here)
> Hi Studio 26! I came across your page and loved seeing your dancers learning routines in class and your bring-a-bestie nights — it really comes across as a close dance family in Easterhouse. I noticed you don't have a website or a link in your bio yet, so anyone wanting to join has to message you first to find anything out. I made you a quick preview website with your own photos, your classes, the new competition team and your Phoenix Community Centre base, so new dancers can see what you offer before they message: [PREVIEW LINK]
>
> Would you like a look and tell me what you'd change?

Notes on the draft: one genuine observation (class/bestie-night posts, dance-family feel), why a website helps them specifically (no website/bio link → discovery and joining friction), the preview link placeholder, one low-pressure question, no fake compliments, no invented stats, no prices or claims.
