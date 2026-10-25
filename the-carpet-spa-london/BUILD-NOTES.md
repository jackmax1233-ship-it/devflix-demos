# BUILD NOTES — The Carpet Spa (Wimbledon Chase, South London)

## Gap re-verification (done FIRST, before building) — GAP CONFIRMED, no official site found
- Web search "The Carpet Spa Wimbledon carpet cleaning" (25 Oct 2026) returned NO official website for this business.
  - `thecarpetspa.com` is a different business: Carpet Spa, Falls Creek, Pennsylvania, USA (800 Chan Rd, Falls Creek, PA). Not this business.
  - `thecarpetspauae` is a different business: The Carpet Spa, Abu Dhabi, UAE (handle @thecarpetspauae). Not this business.
  - Other Wimbledon results are unrelated local cleaning firms (Fantastic Services, Cleaner Wimbledon, etc.).
- Photo check: all four harvested thumbnails were inspected visually. They are plain photographs with NO printed domain, phone number, logo or text overlay of any kind. (Caveat: oEmbed returns the first frame of each post only; later carousel frames were not individually inspectable via this route, and no domain/phone appears in any caption text returned.)
- Bio gap as briefed (no bio links, "DM to book") is consistent with the contact route used on this site (Instagram DM only). No phone, email or website is shown on the site because none was verified for THIS business.
- Note on author_id: the brief gave author_id 17841431508388095; oEmbed returned author_id 31584762279 with author_name `the_carpet_spa` on all four posts. The handle match was verified on every post; the numeric difference is recorded here, not treated as a mismatch of business.

## Fact sources (only these facts are used on the site)
- Instagram @the_carpet_spa, 432 followers, South London / Wimbledon Chase (per brief).
- Latest post 23 Oct 2026: before/after bedroom steam-clean carousel, location Wimbledon Chase (per brief; the hero photo is the first frame of post De2A2SuAG58).
- Fully insured; residential + commercial; deep-clean positioning; bio says "DM to book" (per brief).
- Post captions (from oEmbed titles):
  - De2A2SuAG58: "Emergency call from a friend who needed a fresh start on there new home — All room treated and steam cleaned."
  - De18thPgNOX: "Get your sofa cleaned up by @the_carpet_spa and we aim for best results. Same day cleans available."
  - DeoL2GIAObR: "Another care home clean up giving the kids a clean space and clear thoughts. 'Where dirt ends, comfort begins.'"
  - DefM0tRAIbg: "Few different cleans today at a children's care home — Making sure the kids have a clean space to live is important."
- NOT claimed anywhere on the site: prices, reviews, ratings, star scores, phone numbers, email addresses, or a website address for the business. Engagement (likes/follower counts) is not mentioned on the site.

## Photo harvest log (public oEmbed, 25 Oct 2026)
All four posts returned author_name `the_carpet_spa` (verified match) and a 640px thumbnail. Downloaded with browser Referer/UA, converted to WebP quality 78. No photo shortfall — 4 of 4 usable.

| Post | File | Natural size | WebP size | Subject |
|---|---|---|---|---|
| https://www.instagram.com/p/De2A2SuAG58/ | images/bedroom-steam-clean.webp | 640×853 (3:4 portrait) | 79,528 bytes | Freshly steam-cleaned bedroom carpet, white furniture |
| https://www.instagram.com/p/De18thPgNOX/ | images/sofa-clean.webp | 640×853 (3:4 portrait) | 47,988 bytes | Fabric sofa during cleaning |
| https://www.instagram.com/p/DeoL2GIAObR/ | images/care-home-carpet.webp | 640×853 (3:4 portrait) | 170,706 bytes | Cleaned grey care-home carpet |
| https://www.instagram.com/p/DefM0tRAIbg/ | images/childrens-room-carpet.webp | 640×853 (3:4 portrait) | 149,149 bytes | Children's-room carpet, care home |

## Design
- Palette (deliberately distinct from navy/cream and deep pine green): warm paper `#FBF7F1`, deep paper `#F3E9DC`, charcoal ink `#26201C`, terracotta rust `#8C3B1E`, dark rust-brown `#5C3A24`. Editorial split hero, Fraunces serif display + Inter body.
- No gradients, no glassmorphism, no decorative icons.

## Contrast table (WCAG AA: 4.5:1 normal text, 3:1 large text — all pairs pass)
| Foreground on background | Ratio | Verdict |
|---|---|---|
| `#26201C` ink on `#FBF7F1` paper (body, headings, nav) | 15.07:1 | Pass AA |
| `#5C5148` muted on `#FBF7F1` paper (secondary text, captions) | 7.22:1 | Pass AA |
| `#8C3B1E` rust on `#FBF7F1` paper (eyebrow, links, accents) | 7.13:1 | Pass AA |
| `#FFFFFF` on `#8C3B1E` rust (primary buttons) | 7.61:1 | Pass AA |
| `#FFFFFF` on `#26201C` ink (contact section headings) | 16.08:1 | Pass AA |
| `#F3E9DC` paper-deep on `#26201C` ink (contact body text) | 13.40:1 | Pass AA |
| `#FFFFFF` on `#5C3A24` dark rust (button hover) | 10.07:1 | Pass AA |
| `#FFFFFF` on `#8C3B1E` rust (quote section, large serif text) | 7.61:1 | Pass AA (also passes large-text 3:1) |

## Image-fit audit (per image — full view, no cropping)
- All four source photos are exactly 3:4 portrait (640×853). Every container that shows them uses `aspect-ratio: 3/4` with `object-fit: cover` at the SAME ratio, so cover crops nothing and the full subject is visible.
- Hero: figure capped at 420px wide → image renders at most 560px tall on desktop (420 × 4/3 = 560), meeting the hero cap. Width/height attributes (640/853) set on every `<img>`.
- Gallery: 4 columns desktop (each ≈250px wide → ≈333px tall, under the ~340px cap), 2 columns at ≤900px, 1 column at ≤560px (capped 420px wide). No fixed heights, no stretching.
- Below-fold images use `loading="lazy"`; hero image uses `fetchpriority="high"`. No base64 images anywhere; all paths relative (`images/*.webp`, no leading `/`).
- Honesty note: oEmbed supplies only the first frame of each carousel, so the gallery is captioned as "recent work" with per-job captions rather than claiming paired before/after shots. The 23 Oct bedroom post is described in the brief as a before/after carousel, but only its first frame is shown here.

## Responsive audit (CSS review, not a live-browser check)
- Mobile-first fluid layout: `.wrap` max-width 1100px with side padding; all images `max-width: 100%`; grids collapse 4→2→1 columns and 3→2→1 cards at 900px/560px breakpoints; nav and CTAs wrap with flex-wrap; no fixed-width elements, no horizontal-scroll risk from declared widths. Live-browser verification at 390/768/1440px was NOT possible from this subagent (no live browser) — the parent should spot-check the deployed page at those widths before the DM goes out.

## DM draft (for the parent to send — do not send from here)
> Hi, I came across The Carpet Spa while looking at local carpet cleaners around Wimbledon Chase — the bedroom steam clean you posted recently really shows the difference a proper deep clean makes, especially the whole-home jobs and the care-home cleans.
>
> I noticed you don't have a website yet and bookings come through DM, so I put together a quick preview site for you using your own photos — it shows your recent work, the residential and commercial side, and that you're fully insured, with a button straight to your Instagram.
>
> Here's the preview: [PREVIEW LINK]
>
> Would something like that be useful for you, or is DM working fine as it is?
