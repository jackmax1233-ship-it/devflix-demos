# Balloons by Ange — Preview Site Build Notes

Built: 30 Oct 2026 (night batch) · Builder: site-builder subagent · NOT sent, NOT deployed — folder only, for the parent agent to deploy + DM.

## Fact sources (verified only — nothing else used)

- Business: Balloons by Ange (Balloon Garlands Auckland), West Auckland, New Zealand.
  Instagram @balloonsbyange, 675 followers, 218 posts (per task brief).
- Bio (per brief): balloon garlands, backdrops and decals; based in West Auckland;
  booking via "DM or Email to book". No email address is published in the bio, so
  the site links DM only (https://ig.me/m/balloonsbyange) — no email invented.
- No own website, no bio link at all (per brief) — that is the pitch gap.
- Post captions verified via the public Instagram oEmbed endpoint (author_name
  "balloonsbyange" on all five posts):
  - https://www.instagram.com/p/Depj-L8zwYe/ — "Let's talk about your December
    events"; its image itself reads "OCTOBER & NOVEMBER 2026 FULLY BOOKED /
    PLEASE GET IN TOUCH NOW FOR DECEMBER EVENTS / Allow a minimum of 3 weeks'
    notice / @Balloonsbyange". (Latest post, 18 Oct 2026, per brief.)
  - https://www.instagram.com/p/DdDFaXcmNLQ/ — "A closer look at one of our
    biggest corporate installs to date: A 3m × 3m statement arch, two 3m
    freestanding pillars + 20 custom branded tablescape pieces."
  - https://www.instagram.com/p/Dcr1RremBEG/ — behind-the-scenes process post:
    "From the first idea to the final setup… I love keeping my clients in the
    loop… they can simply show up and enjoy."
  - https://www.instagram.com/p/DcpA_0eE1nN/ — tropical install "created for
    Georgia's 7th, featuring tropical foliage, bubble balloons, custom signage";
    palette published in the caption: Caribbean Blue • Purple Orchid • Raspberry
    • Goldenrod • Coral • Romey.
  - https://www.instagram.com/p/DckRTs0mJqv/ — "3m x 3m custom balloon arch /
    Three freestanding balloon pillars / Custom branded details throughout /
    Designed, built and installed for @thewarehousenz".
- Deliberately NOT used on the site: the child's first name from the tropical
  caption (gallery caption says only "a 7th birthday"); no prices (the
  behind-the-scenes post mentions a price breakdown but no figures are quoted
  anywhere on the site); no address, phone, hours, packages, reviews or ratings
  — none published by the business. Palette swatch hex values are approximate
  renderings of the business's published palette *names*, not published hex codes.

## Photos (5 harvested, 0 failed, 0 stock/AI)

All via public oEmbed thumbnail_url (640 px max), downloaded with a browser
Referer/UA, converted to WebP quality 78. No post failed.

| File | Source post | Natural size | Used as | Size |
|---|---|---|---|---|
| img/tropical-garland.webp | DcpA_0eE1nN | 640×853 portrait | Hero + gallery tile | 66 KB |
| img/corporate-arch.webp | DdDFaXcmNLQ | 640×427 landscape | Gallery wide tile | 44 KB |
| img/warehouse-arch.webp | DckRTs0mJqv | 640×853 portrait | Gallery tile + corporate section | 71 KB |
| img/behind-scenes.webp | Dcr1RremBEG | 640×853 portrait | Process section | 77 KB |
| img/december-events.webp | Depj-L8zwYe | 640×640 square | December section | 15 KB |

Total images: ~273 KB. All `<img>` tags carry width/height attributes;
below-the-fold images carry loading="lazy"; hero uses fetchpriority="high".
No base64 anywhere in the HTML (verified by scan).

## Per-image fit / focal notes (FULL-VIEW rule)

Every frame's aspect ratio matches the photo's natural ratio, so `object-fit:
cover` crops nothing in practice; the December graphic (which carries text)
uses `object-fit: contain` on a white field so no letter is cut:
- tropical-garland (3/4 frame, object-position 50% 50%): full install visible —
  garland spans the frame edge to edge, backdrop centred, character cutout at
  bottom-right fully in frame. Checked visually.
- corporate-arch (3/2 frame): full arch, starbursts, entrance and red carpet
  visible; nothing clipped at the edges. Checked visually.
- warehouse-arch (3/4 frame): full arch + pillars + red carpet visible.
  Checked visually.
- behind-scenes (3/4, contain): overlay text "HOW WE BROUGHT THIS TO LIFE"
  fully legible, install fully visible below it. Checked visually.
- december-events (1/1, contain): all text fully legible, nothing cut.
  Checked visually.
- Hero capped at max-height 560 px; gallery wide tile capped at 340 px;
  content images capped at 480 px (per AGENTS.md size discipline).

## Design

Own festive identity, not a copy of the aussie-tan reference (which was used
only for structure: sticky nav, hero, gallery, feature, CTA, footer).
Palette: cream #FFFBF4, deep plum #33182B, coral #D93A2B / deep coral #B92E22,
teal #0E6B6A, sunny #F2A93B, blush #FBE3D8. No gradients, no glassmorphism.
Fonts (2): Fraunces (display serif) + Nunito Sans (body). Decoration is flat
CSS confetti dots, not images. Scroll-reveal gated behind a `.js` class
(content visible without JS); respects prefers-reduced-motion.

## Per-section contrast results (computed, WCAG AA)

| Pair | Ratio | Verdict |
|---|---|---|
| Ink #33182B on cream #FFFBF4 (body/headings) | 15.58:1 | Pass |
| Muted #6E4A52 on cream (body secondary) | 7.36:1 | Pass |
| Deep coral #B92E22 on cream (eyebrows, links) | 5.86:1 | Pass |
| Teal #0E6B6A on cream (ghost links) | 6.11:1 | Pass |
| White on deep coral #B92E22 (buttons, strip) | 6.04:1 | Pass |
| White on teal #0E6B6A (CTA band) | 6.31:1 | Pass (CTA button itself is cream on plum, 15.58:1) |
| Cream on deep plum #33182B (footer note, process, badges) | 15.58:1 | Pass |
| Ink on blush #FBE3D8 (service cards) | 13.08:1 | Pass |
| Process secondary #E8D9DE on plum | ~12:1 class | Pass (light text on near-black) |
| Palette swatch labels | — | Each swatch pairs a dark label with a light swatch or white label with a dark swatch; Goldenrod/Romey swatches use dark plum text on light fills. |

Note: bright coral #D93A2B (white-on = 4.57:1) is used only as a decorative
dot/accent colour, never for text or buttons — all text/buttons use the
darker #B92E22. No text sits over a photo except the hero badge (cream on
plum, solid background) and gallery captions (ink on solid cream, below the
image, not overlaid).

## Responsive check — method and honest result

- I did NOT perform a live-browser check: as a subagent I have no live-browser
  control, and no live render at 390/768/1440 px was run. Do not claim one.
- What WAS checked: (1) HTML parsed programmatically — tags balanced, all 7
  `<img>` references resolve to existing files; (2) CSS audited — layout is
  mobile-first single-column stacking to 2 columns ≥640 px and 3 columns
  ≥900 px; all widths are %, rem or max-width (the only px widths found are
  media-query breakpoints); `overflow-x:hidden` on body; nav links hide on
  mobile leaving brand + CTA; hero badge repositioned inside the figure on
  mobile; no fixed-height text containers that could clip copy.
- Residual risk: the brand + CTA row at ~390 px is close to full width
  (estimated ~360 px of 390 px) — worth one live look at 390 px before sending,
  plus a normal visual pass at 768/1440 px when the parent deploys.
- Deploy step is the parent's: upload this folder and verify the live URL
  renders with photos + no overflow before DMing (per the batch workflow).

## Personalized DM draft (DO NOT SEND — for parent approval)

> Hi Ange! I came across Balloons by Ange and loved your tropical 7th-birthday
> install — the colour mix and the way the garland frames the whole backdrop is
> gorgeous. I noticed you don't have a website yet and bookings come through DM
> or email, so I put together a little preview site for you with your recent
> installs, your corporate work and a December-events section, since October
> and November are fully booked: [PREVIEW LINK]. Would something like that be
> useful for taking December enquiries? No pressure at all — just thought it
> might help. 😊
