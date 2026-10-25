# BUILD NOTES — SLM Window & Eaves Cleaning (Toronto & GTA)

## What was built
One preview website: `index.html` + 8 WebP images. No deployment, no tracker edits, no contact made.

## Facts used (only what the business itself published)
- Business: SLM Windows & Eaves Cleaning — Instagram @slmwindowseaves.
- Bio (verified three ways: anonymous profile meta, instagram-cli author_bio, post captions): "Professional Window & Eaves Cleaning — Window Cleaning • Eaves Cleaning — Toronto & GTA — (437) 784-5030 — Book your FREE quote".
- Services: window cleaning, eavestrough cleaning, leaf removal / fall yard cleanup (captions); plus eavestrough repairs, gutter guard installation, pressure washing, "fully insured" (all printed on SLM's own flyer, visible in post DeKgldjow1 — zoom-checked).
- Contact: phone (437) 784-5030 (bio + every caption + flyer, so included); email slmwindoweaves@gmail.com (printed on the same flyer, zoom-verified, so included).
- Seasonal messaging (captions, paraphrased): clear leaves/debris → proper drainage → prepare home for winter; regular cleaning helps prevent buildup, blockages and water damage; fall services now booking, limited availability as the season ends.
- Follower count 735 (instagram-cli, Oct 2026 posts); latest post 2026-10-23.
- NOT claimed: no prices (business offers free per-job quotes, so the site says exactly that), no hours, no street address, no reviews/ratings, no service-area list beyond "Toronto & GTA".

## Gap re-verification (done by this builder, 25 Oct 2026)
1. **Web search** — "SLM window eavestrough cleaning Toronto" and "slmwindoweaves Toronto window eaves": returned only OTHER Toronto firms (Silverlight, SUDS, Shine, Perfect, Mark's, etc.). No website for SLM itself appeared in either search.
2. **Bio link check** — the anonymous profile fetch returned bio text but not the bio-link URL (that JSON is login-walled from this VM), so the exact bio-link destination could NOT be re-read independently here. Per the parent brief it is a WhatsApp message link, not a website or booking system — and nothing found contradicts that: no domain appears in the bio text, in any caption, or in any post graphic (see below).
3. **Post graphics / domain check** — all 8 harvested images were viewed individually. They contain only: work photos, SLM branding footers ("SLM Windows & Eaves · Toronto & The GTA"), the flyer (phone + email + @slmwindowseaves handle), and short slogans. No website domain, no booking URL, no directory listing for SLM was found.
4. **Conclusion: gap stands.** A Toronto/GTA searcher cannot find a site with SLM's services, areas, or a quote route — only Instagram posts and a chat link. Build proceeded.
5. **India / age check** — business is Toronto & GTA, Ontario, Canada (not India-based). Nothing states or suggests the operator is under 18; it is a professional trade-services account.

## Photo harvest log (oEmbed route, iPhone UA)
All 8 posts returned `author_name: slmwindowseaves` (match verified). Thumbnails downloaded with browser Referer/UA, converted to WebP q78 (source ceiling 640w, so no upscaling).

| Post | Use in site | Natural size | Notes |
|---|---|---|---|
| Dest5Tli34O (2026-10-23) | Hero — before/after eaves | 640×794 | Split before/after with baked-in "BEFORE / AFTER" labels and SLM footer — these are the business's own graphic labels, not a video play button |
| Destl4Dikqb | Fall section image | 640×787 | "Fall is here. So are the leaves." graphic footer |
| DestN-fC9FQ | Gallery — window cleaning day | 640×794 | Ladder against Toronto house; SLM footer |
| Det5lILl0KM | Gallery — eaves full of leaves | 640×800 | Plain work photo, no overlay |
| DeHb6IZjicb | Gallery — brick house windows | 640×853 | Plain work photo, no overlay |
| DeRo4vXDnvp | Gallery — roofline leaves | 640×640 | Plain work photo, no overlay |
| DePDgsZji6a | Gallery — autumn gutter | 640×640 | Plain work photo, no overlay |
| DecKgldjow1 | Gallery — SLM flyer | 640×853 | Flyer photo; source of repairs/gutter-guard/pressure-washing/insured/email facts |

**Reel / play-button disclosure:** none of the 8 thumbnails carries a baked-in video play button. Three carry the business's own text footers/labels (noted above); those are SLM's own graphics and are shown as-is, captioned as such.
**Shortfall:** none — 8/8 usable photos, above the 4-photo minimum. No stock or AI photos used anywhere.

## Design
Trade-specific, not a generic template: deep navy taken from SLM's own post footers, warm autumn-leaf amber, warm paper background, Barlow Condensed headings + Barlow body. No gradients, no glassmorphism, no glowing borders, no decorative icons (the only marks are text checkmarks in the benefits list).

## Contrast table (WCAG AA, normal text needs ≥ 4.5:1 — all pass)
| Foreground on background | Ratio | Result |
|---|---|---|
| #1E2A36 body on #F7F5F0 paper | 13.39:1 | PASS |
| #FFFFFF on #12263A navy (top bar, strip, buttons, footer) | 15.40:1 | PASS |
| #D8DEE4 muted light on #12263A navy | 11.35:1 | PASS |
| #F2B84B amber eyebrow on #12263A navy | 8.60:1* | PASS (large/bold eyebrow; also passes as normal text vs navy at 8.60) |
| #12263A navy text on #F2B84B amber button | 8.60:1 | PASS |
| #5C3D00 dark brown on #F2B84B amber | 5.53:1 | PASS |
| #4A5866 muted on #F7F5F0 paper | 6.69:1 | PASS |
| #4A5866 muted on #FFFFFF cards | 7.29:1 | PASS |
| #4A5866 muted on #E9E2D4 tint section | 5.66:1 | PASS |
| #1E2A36 on #E9E2D4 tint section | 11.32:1 | PASS |
| #8A4B00 eyebrow on #F7F5F0 paper | 6.24:1 | PASS |
| #FFFFFF on #243A4E button hover | 11.73:1 | PASS |
| #FFFFFF on #1E5A3C checkmarks | 8.13:1 | PASS (checkmarks are decorative; adjacent text passes independently) |

*Amber eyebrow ratio computed as #F2B84B on #12263A = 8.60:1.

## Image-fit audit (full view)
Every image is rendered with `width:100%; height:auto` at its natural aspect ratio — nothing is cropped, stretched, or forced into a uniform frame. Hero image (640×794 portrait) sits in a max-450px column, so its rendered height is ≈ 558px on desktop — inside the ~560px hero cap — and ≈ 484px at 390px width. Gallery images keep their own ratios (portrait, square, and flyer all shown whole). No `object-fit: cover` is used anywhere, so no subject is cut at any width.

## Responsive audit — CSS-audit only
No live viewport check was possible from this subagent (no live-browser tooling), so this is a CSS audit, not a live check: mobile-first single column under 560px, two columns under 900px, three columns above; flex-wrap on header/top bar/nav/buttons; `max-width:100%` on all images; no fixed-width containers. No horizontal-overflow or overlap risks were found in the CSS, but the parent should still do a live 390/768/1440 check before sending the DM.

## Technical checks
- HTML parsed balanced (no unclosed/stray tags).
- Zero base64 images; all images are separate `images/*.webp` files (44–151 KB each, 820 KB total).
- Relative paths only for internal links/images. Only external links: Google Fonts CDN, `tel:`, `mailto:`, and the business's own Instagram profile.
- No invented booking system: the quote section links only to the business's real phone, email, and Instagram DM route.

## DM draft (for parent to send — do not send from here)
> Hi! I came across your before-and-after eaves post from this week — the gutter packed with fall leaves next to the clean one says it all about why this season matters. I noticed someone searching in Toronto or the GTA can't really find your services or request a quote anywhere except Instagram, so I put together a quick preview website using your own photos and fall-cleanup posts: https://jackmax1233-ship-it.github.io/devflix-demos/slm-window-eaves-cleaning-toronto/
>
> It pulls your window and eaves services, the before-and-after, and your free-quote contact into one page. Would something like that be useful for the fall rush, or is Instagram working fine for bookings as it is?
>
> — Devflix

## Opportunity + why a good prospect
On-season timing (fall eaves rush, "now booking fall services" in their own words) plus a clean, evidenced gap: strong, consistent, genuinely useful Instagram proof — especially the before/after — with nowhere for a Google searcher to land, compare services, or request a quote. Small-but-real following (735), consistent posting, and a trade where a quote page converts directly into jobs. The preview is built entirely from their own photos and words, so the pitch is honest and easy for them to say yes to.

## Author ID notes
- **instagram-cli numeric author ID: 17841460100305509** (returned as `author_id` for every SLM post; also the first fbid in the posts response).
- **oEmbed author ID: 60124075343** (legacy IGID shown by the oEmbed endpoint for all 8 posts).
- They differ because they are two ID systems for the same account (@slmwindowseaves — both endpoints agree on the handle, bio, phone, and follower count).
- **Parent should use 17841460100305509** (the instagram-cli author ID) for any CLI/DM lookup, and the handle @slmwindowseaves for the DM itself.
