# R.C Window Tinting — Preview Site Build Notes

Built: 30 Oct 2026 (night batch) · Folder: `rc-window-tinting-sylmar/`
Status: **Built only — NOT deployed, NOT sent.** No message was sent to anyone.

## Business (as briefed — do not re-derive from elsewhere)
- R.C Window Tinting, mobile window tinting, Sylmar, California, USA
- Instagram @rc_windowtinting, author_id 17841400367554935, 1,918 followers
- Bio: "GOD FIRST / SYLMAR, CA / 5-star Yelp & Google / MOBILE WINDOW TINTING SPECIALIST / DM FOR A QUOTE"
- Pitch gap: NO own website, NO bio link at all — quotes/bookings entirely by DM.

## Fact sources (only these were used)
1. **Task brief facts** (taken as verified by the parent run): bio text; "DM year, make and model for quotes"; full ceramic work incl. 50% front windshield / 35% windshield + 5% sides+rear examples; 15% dual reflective film for privacy and heat rejection; vehicles incl. Mercedes S580, Escalade, Toyota Corolla; a new ADU fully protected with film; no website / no bio link.
2. **oEmbed responses for the 5 supplied reels** (all returned `author_name: rc_windowtinting`, confirming the photos are theirs). Captions re-confirmed: DM-year/make/model quoting; S580 full ceramic (50% windshield, front 50% / rear 18%); full ceramic all-around (35% windshield, 5% sides+rear); Escalade full ceramic; Corolla full makeover; mobile "we bring the shop to you" setup. Note: the brief's "50% front windshield" S580 figure and the reel caption's "front 50% & rear 18%" differ slightly in scope — the site says "50% front windshield" only, per the brief, and does not repeat the 18% figure.
3. **Deliberately NOT used**: rcwindowfilms.com and any Meta place listing address/phone (brief: different/unconfirmed business). No address, phone, hours, prices, packages, or testimonials appear anywhere on the site. The "5-star Yelp & Google" line is attributed on-page as "per our bio" — it is their bio claim, not an independently verified rating.

## Photos (5, all the business's own reel stills, none skipped)
Harvested via the public oEmbed endpoint with iPhone UA, thumbnails downloaded with browser Referer/UA, converted to WebP quality 78 with PIL. All sources are 640×1138 portrait (9:16).

| File | Source reel | Subject / focal point | Placement |
|---|---|---|---|
| `img/s580.webp` (161 KB) | DfFJd7WgkvK | Black S580, front 3/4, car in lower half of frame | Hero |
| `img/mobile-van.webp` (53 KB) | DfHtwPeg60t | White mobile van + installer beside it, centre-right | Gallery: "The mobile shop" |
| `img/install.webp` (39 KB) | DfDCdGKA3XX | Installer squeegeeing a side window, centre | Gallery: install in progress |
| `img/escalade.webp` (60 KB) | DertzKHuhR7 | Black Escalade, rear 3/4, centre | Gallery |
| `img/corolla.webp` (98 KB) | Dek9srigQUG | White Corolla rear during makeover, centre-lower | Gallery |

Total site: ~424 KB (HTML 16 KB + images ~408 KB). No base64 in HTML (grep-verified: 0 matches). All 5 `img/*.webp` references resolve to existing files. Width/height attributes set (640×1138); lazy-load on all below-fold images; hero uses `fetchpriority="high"`.

### Image-fit notes (full-view rule)
- **Hero**: frame `aspect-ratio: 9/16`, `object-fit: cover`, column capped at 19.6rem wide → 560px tall at the cap. Native ratio is exactly 9:16, so cover crops **nothing** — the full S580 and driveway are in frame.
- **Gallery**: frames `aspect-ratio: 4/5`, `object-fit: contain` on a dark (#14171A) background, captions **below** the image (never overlaid), so no subject is ever cropped or covered. Letterboxing is visible on the dark background by design — full view wins over uniformity.
- **Flags for the sender (not defects, decide before DM)**: (a) the mobile-van still shows "Nxt Level Window Tinting" van branding and a painted phone number — that is their own published reel still (their posts tag @nxtlevelwindowtinting as a collaborator), and the number was NOT transcribed into any copy; (b) the Escalade still shows its license plate, as published in their own reel; (c) all stills carry the reels' baked-in text overlays ("S580 IN CERAMIC", "POV: MOBILE TINTING ESCALADE", etc.) — unavoidable with oEmbed stills, and they read as authentic social proof rather than a flaw.
- No stock or AI images used. No other business's photos used.

## Design (own identity, not a copy of the aussie-tan reference)
- Structural reference only: aussie-tan-uk/index.html (nav / hero / strip / cards / gallery / steps / CTA / footer rhythm, reveal script pattern).
- Own identity: automotive/trade — charcoal #14171A + safety amber #F2A900 on warm paper #F4F2ED, flat colours, no gradients, no glassmorphism. Fonts: Archivo (display, uppercase) + Inter (body) — 2 families. Thin amber rule details; no decorative icons/shapes beyond a small amber bar on section eyebrows.
- Hero capped at 560px tall on desktop; gallery frames moderate (4/5, ~340px tall at desktop column widths).

## Contrast results (computed from hex luminance, WCAG AA: 4.5:1 normal, 3:1 large)
| Pair | Ratio | Verdict |
|---|---|---|
| Ink #14171A on paper #F4F2ED (body, headings) | 16.08:1 | Pass |
| Muted #4F575E on paper #F4F2ED (body secondary) | 6.57:1 | Pass |
| Muted #4F575E on white #FFFFFF (service cards) | 7.35:1 | Pass |
| Paper #F4F2ED on dark #14171A (quote section, footer text) | 16.08:1 | Pass |
| Muted-light #B9C0C6 on dark #14171A (secondary on dark) | 9.78:1 | Pass |
| Amber #F2A900 on dark #14171A (eyebrows/labels on dark) | 8.95:1 | Pass |
| Ink #14171A on amber #F2A900 (buttons, strip text) | 8.95:1 | Pass |
| Ink #14171A on amber-tint #FBEED3 (service tags) | 15.65:1 | Pass |
| White #FFFFFF on dark #14171A | 17.99:1 | Pass |

No text is placed over a photo anywhere on the site — hero caption and gallery captions sit below their images on solid backgrounds. Buttons: amber bg + near-black label (8.95:1), with a visible amber focus outline.

## Responsive check — method and result (honest)
- **No live-browser check was performed**: as a subagent I have no browser control, so I did NOT verify this site in a real browser at any width, and this must not be claimed otherwise.
- What WAS checked: mobile-first CSS audit — single-column base layout stacking to 2-col (gallery) / 3-col (services, steps) / 4-col (gallery) only at ≥768px/≥900px breakpoints; all widths fluid (`width:100%`, `max-width` containers); `overflow-x:hidden` on body; `clamp()` display type; nav secondary links hidden ≤640px so brand + CTA fit a 390px viewport; no fixed pixel widths except the 19.6rem hero column cap and max-width containers (grep-audited). No horizontal-overflow or overlap risk is visible in the code, but **the parent run must verify live at ~390px, ~768px and ~1440px before deploying**, per the AGENTS.md gate.

## Copy honesty notes
- No invented prices, packages, hours, address, phone, reviews, or service claims. Shade percentages and vehicle examples are exactly the brief/caption facts above.
- The quote section's line "Right now, quotes run entirely by DM. This page is a preview of how simple that first step could be" is the site's only meta line — it frames the concept honestly for the business owner viewing the preview without making a customer-facing claim.
- Footer carries the discreet "Preview concept by Devflix" note. No fake testimonials.

## DM draft (NOT SENT — placeholder for the preview link)
> Hey! Came across your page — that S580 in full ceramic came out clean, and I liked that you bring the whole setup to the customer's driveway instead of making them come to a shop. One thing I noticed: right now everything runs through DMs, and there's no link in your bio where someone can see the work and what to send for a quote. I put together a quick preview page for you — your recent jobs, the ceramic/privacy work, and a simple "send year, make and model" quote step, all in one place: [PREVIEW LINK]. No pressure at all — would something like that be useful for you, or are DMs working fine as-is?

## What could NOT be verified
- The brief-supplied facts about the 15% dual reflective film and the ADU job were NOT re-confirmed in the 5 reel captions fetched (those captions cover ceramic shades, the three vehicles, and the mobile setup). They are used exactly as briefed, not embellished.
- No independent check of the bio's "5-star Yelp & Google" claim was made; it is attributed as their bio claim on-page.
- Responsive behaviour is code-audited only (see above) — live verification still owed by the parent run.
