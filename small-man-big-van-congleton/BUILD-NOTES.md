# BUILD NOTES — A Small Man with a Big Van (Congleton, Cheshire)

- Slug: `small-man-big-van-congleton`
- Local dir: `~/workspace/instagram/lead-campaign/sites/small-man-big-van-congleton/`
- Intended preview link (NOT deployed by this build): https://jackmax1233-ship-it.github.io/devflix-demos/small-man-big-van-congleton/
- Built: Sun 25 Oct 2026, morning batch. No DM sent, no tracker edited, nothing deployed — files on disk only.
- Design: warm cream + deep green + brick-red accent, Barlow Condensed (headings) + Barlow (body), max 2 Google Font families, `display=swap`. No gradients, no glassmorphism, no floating-card clutter, no oversized meaningless hero heading — the hero line is the business's own name concept.
- Images: separate WebP files in `images/`, relative paths only, never base64. Total images folder: 360 KB.

## CAVEAT — owner must confirm before the pitch goes out

The brief states the sister furniture shop has its own website/shop and the sister removal firm is separately listed, and nothing was found for THIS brand name itself. This build therefore treats "A Small Man with a Big Van" as having no website of its own, but **the owner should confirm this brand has no site of its own before the pitch is sent**. If it does, do not pitch it as "you have no website".

## (a) Contrast table (WCAG AA: ≥4.5:1 normal text, ≥3:1 large text)

Computed with the standard WCAG relative-luminance formula (Python, same method as the build check). All pairs below pass AA for normal text, so they also pass for large text.

| Text / element | Foreground | Background | Ratio | Verdict |
|---|---|---|---|---|
| Body text | #4A4238 | #FAF5E9 cream | 9.07:1 | PASS |
| Headings | #17382E deep green | #FAF5E9 cream | 11.76:1 | PASS |
| Headings on white/paper | #17382E | #FFFDF6 / #FFFFFF | 12.79:1 | PASS |
| Eyebrow / accent text | #B3402A brick | #FAF5E9 cream | 5.24:1 | PASS |
| Dark button label | #FFFFFF | #17382E deep green | 12.79:1 | PASS |
| Brick button label | #FFFFFF | #B3402A brick | 5.70:1 | PASS |
| Brick button hover label | #FFFFFF | #8A2F1E dark brick | 8.38:1 | PASS |
| Dark section body | #EDEBE2 / #FAF5E9 | #17382E deep green | 11.76:1 | PASS |
| Dark section eyebrow | #E8C9A8 pale peach | #17382E deep green | 8.13:1 | PASS |
| Muted captions | #5C5347 | #FAF5E9 cream | 6.93:1 | PASS |
| Text on sand band | #17382E | #EDE6D2 sand | 10.26:1 | PASS |
| Text on sage band | #17382E | #DCE5DC sage | 9.92:1 | PASS |
| Topbar text | #FAF5E9 | #17382E | 11.76:1 | PASS |
| Footer text | #D9D5C8 | #17382E | 8.71:1 | PASS |

Text is never placed over a photograph — captions sit on plain paper below the image, so photo contrast never gates readability.

Contrast pass count: **14 rows checked, 14 pass AA for normal text, each ratio computed exactly** (lowest passing pair: brick #B3402A on cream at 5.24:1).

## (b) Image-fit audit (FULL VIEW — no cropping of vans, crews or furniture)

All source thumbnails are 640 px wide (the oEmbed ceiling). Every `<img>` uses `object-fit: contain` with `width:100%; height:auto` and a container aspect ratio matched to the source, so the whole photo shows at every width.

| File (images/) | Source size | Container aspect | Desktop height* | Mobile behaviour | Cut? |
|---|---|---|---|---|---|
| house-move-congleton.webp (hero) | 640×480 (4:3) | 4:3 | ~375 px at ~500 px wide (≤560 cap) | Scales down, full frame | No |
| move-biddulph-congleton.webp | 640×480 (4:3) | 4:3 | ~262 px in 3-col card (≤340 cap) | Full width, full frame | No |
| office-move-knutsford.webp | 640×480 (4:3) | 4:3 | ~262 px | Full width, full frame | No |
| shed-collection.webp | 640×480 (4:3) | 4:3 | ~262 px | Full width, full frame | No |
| storage-run-congleton.webp | 640×564 (~8:7) | 640/564 (exact) | ~308 px (≤340 cap) | Full width, full frame | No |
| event-job-birmingham.webp | 640×480 (4:3) | 4:3 | ~262 px | Full width, full frame | No |
| removal-congleton.webp | 640×480 (4:3) | 4:3 | ~262 px | Full width, full frame | No |
| furniture-delivery.webp | 640×480 (4:3) | 4:3 | ~262 px | Full width, full frame | No |

\* Heights are computed from the CSS grid widths (max content width 1120 px), not measured in a live browser — see responsive note below. No full-bleed photo bands are used, so the ≤420 px band cap is not engaged. No `object-fit: cover` is used anywhere.

## (c) Fact sources — every claim traced

Only the brief's published facts and the captions returned by the oEmbed endpoint were used. Nothing else was invented.

| Claim on the site | Source |
|---|---|
| Fully insured man & van service, based Congleton, Cheshire | Brief (bio: "Congleton, Cheshire based. Fully insured man & van service") |
| No website/link/phone/email published for this brand; bio lists only the bio text plus sister accounts | Brief GAP statement; therefore no phone/email is printed anywhere on the site, and the "Good to know" panel says so plainly |
| CTA https://ig.me/m/asmallmanwithabigvan (IG DM) | Brief CTA |
| House moves incl. sale & purchase | Post DepivKDjiy0 (18 Oct 2026): "sale and purchase house move between 2 Congleton properties"; DefJ8jjjqah (14 Oct): "3man 2van removal between 2 Congleton properties, sale and purchase" |
| Small/office moves; returning customer | Post DeutykdDtqd (20 Oct 2026): "small move for a returning customer… office equipment out of a business premises in the middle of Knutsford to a temporary storage in Congleton" |
| Single-item / furniture collections & deliveries | Post DeQ6WN4DitI (8 Oct): shed collection, auction collection, small move to storage; DeNGdxEjsVo (7 Oct): delivery for Congleton Furniture, items Whitegate → Congleton |
| Storage runs (incl. Apex Self Storage, Congleton) | Post DejkeryDrMM (16 Oct): "move out of @apex_self_storage Congleton to a property within Congleton" |
| Event logistics (2-day job) | Post DesHwQ4jq3u (19 Oct): 2-day event job, Congleton → Birmingham, set up at a cinema, back to Congleton |
| Multi-day pack-and-move jobs | Post DexRpbrDr0m (21 Oct): 3-man/2-van team; DeaHCaMDhf_ (12 Oct): 3-day move with the sister team, packing the full house, beds built on arrival (the Dea photo itself was harvested but not placed — see harvest log) |
| 3pm key release / completion-day delays | Posts DexRpbrDr0m ("3pm key release") and DepivKDjiy0 ("held up waiting for a company to empty the purchase property… still managed to fit in an extra collection") |
| Works alongside sister businesses | Brief: sister removal company @savillandson and sister furniture shop @congletonfurniture. Site wording is deliberately "works alongside" only — no shared services claimed. Display names "Savill & Son" / "Congleton Furniture" are plain readings of those handles, not verified legal names |
| Places named (Biddulph, Knutsford, Middlewich, Northwich, Whitegate, Birmingham) | Only where the corresponding post names them |
| Recent-work dates (21 / 20 / 7 Oct 2026) | Post dates supplied in the brief, matched to shortcodes above |

NOT claimed: no prices, no hours, no phone, no email, no reviews, no ratings, no testimonials, no customer counts, no "years of experience", no service area beyond places named in posts.

## (d) Photo harvest log

Method: public oEmbed endpoint with iPhone UA, `author_name` checked for every shortcode; thumbnails downloaded with browser UA + Instagram Referer; converted to WebP quality ~78 via Python PIL.

| Shortcode | Date (brief) | author_name | Result | File used |
|---|---|---|---|---|
| DexRpbrDr0m | 2026-10-21 | asmallmanwithabigvan | OK, 640×480 | images/move-biddulph-congleton.webp |
| DeutykdDtqd | 2026-10-20 | asmallmanwithabigvan | OK, 640×480 | images/office-move-knutsford.webp |
| DesHwQ4jq3u | 2026-10-19 | asmallmanwithabigvan | OK, 640×480 | images/event-job-birmingham.webp |
| DepivKDjiy0 | 2026-10-18 | asmallmanwithabigvan | OK, 640×480 | images/house-move-congleton.webp (hero) |
| DejkeryDrMM | 2026-10-16 | asmallmanwithabigvan | OK, 640×564 | images/storage-run-congleton.webp |
| DefJ8jjjqah | 2026-10-14 | asmallmanwithabigvan | OK, 640×480 | images/removal-congleton.webp |
| DeaHCaMDhf_ | 2026-10-12 | asmallmanwithabigvan | OK, 640×480 — harvested but NOT placed (8-image layout already covers the same multi-day job type; kept as spare, no substitution) | — (spare, not in images/) |
| DeQ6WN4DitI | 2026-10-08 | asmallmanwithabigvan | OK, 640×480 | images/shed-collection.webp |
| DeNGdxEjsVo | 2026-10-07 | asmallmanwithabigvan | OK, 640×480 | images/furniture-delivery.webp |
| DeXWvyxkeAA | 2026-10-11 | **savillandsonremovals** (sister account, NOT this brand) | EXCLUDED on the author check — not this business's own post, so not used even though the brief listed it | — |

Totals: **10 attempted, 9 harvested from @asmallmanwithabigvan, 8 placed on the site, 1 excluded (wrong author), 1 harvested spare unused.** No stock, AI or other-business imagery was substituted anywhere. Honest shortfall: none in coverage — the 8 placed photos cover every service named on the site; the only gap is the deliberate exclusion above, which is a correctness decision, not a missing photo.

## Responsive audit (CSS audit — live visual pass still recommended)

- No Chromium is available on this VM, so no live screenshots were taken. The audit below is a careful CSS audit, and **a live visual pass at ~390 / ~768 / ~1440 px is still recommended before the pitch goes out**.
- Layout: mobile-first stacking — hero, band and two-column sections collapse to one column ≤820 px; service/work grids go 3 → 2 → 1 column; nav stacks vertically ≤560 px; hero CTA buttons go full-width ≤560 px.
- Overflow guards: `box-sizing:border-box` globally, `max-width:100%` on images, grid columns in `fr` units, no fixed pixel widths on text containers, `flex-wrap` on the topbar/nav/trust chips.
- Text/buttons: no clipped text or buttons by construction — all containers size to content, buttons wrap or go full-width on narrow screens, headings use `clamp()` sizing.
- Images: `height:auto` + matched aspect ratios at every breakpoint, so nothing is cut or stretched on mobile either.

## (e) Personalized DM draft (for the parent agent to send — NOT sent by this build)

> Hi — I came across your page and the Biddulph to Congleton move from this week stood out, the 3-man, 2-van job working around a 3pm key release. It's clear you do a lot of proper house moves, not just single-item runs, but right now someone searching for you in Congleton would only find your Instagram — there's no website to explain the range, from sale-and-purchase moves to storage runs and event jobs.
>
> I put together a quick preview of what a site for you could look like, using your own photos and nothing made up: https://jackmax1233-ship-it.github.io/devflix-demos/small-man-big-van-congleton/
>
> Would something like that be useful for you, or is Instagram doing the job for now?

Notes on the draft: one genuine observation (the 21 Oct Biddulph→Congleton 3-man/2-van job with the 3pm key release, from that post's own caption); no fake compliments, no invented stats, no claimed audit; the preview link is the brief's GitHub Pages URL (the site itself is not yet deployed — the link will only work once the parent deploys this folder); one low-pressure question at the end. Before sending, confirm the caveat at the top of these notes (that this brand has no site of its own).
