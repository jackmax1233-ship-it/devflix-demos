# BUILD NOTES — Victoria Manor Haunted House preview site
Built: 2026-10-23 ~01:30 PKT (night outreach batch, 22 Oct). Folder: `~/workspace/instagram/lead-campaign/sites/victoria-manor-haunted-house/`
Zip: `~/workspace/instagram/lead-campaign/sites/victoria-manor-haunted-house.zip` (index.html + img/ at top level, all relative paths — deploys as https://the-cut-co.pages.dev/victoria-manor-haunted-house/)
author_id: 17841403840326111

## Design
Horror-show identity built for a seasonal haunted attraction: near-black, pumpkin orange, blood red, bone. Fonts: Creepster (display, horror accents/large headings only) + Inter (body), Google Fonts display=swap. Hero carries an original hand-coded SVG horror scene (manor silhouette, full moon, bats, twisted trees, jack-o'-lanterns, drifting fog) — a graphic element, never presented as a photo. Scroll-reveal via IntersectionObserver gated on `.js` (content fully visible without JS), `prefers-reduced-motion` respected (all animation disabled). Mobile-first responsive; sticky header collapses to a working Menu button under 760px. No base64, no external images. Preview link goes nowhere yet — deploy step belongs to the parent batch run.

## Business facts (sources — nothing invented)
- Name: Victoria Manor Haunted House · handle @victoriamanorhauntedhouse (author_id 17841403840326111), 513 followers — their IG profile via instagram-cli (task brief + research JSON).
- Bio: "Voted Top 5 Haunted House of the Inland Empire/ High Desert. Located at 9976 Joshua Rd Apple Valley Ca 92308" — quoted verbatim from their bio (instagram-cli author_bio). Site presents the Top-5 claim as their own billing.
- Address: 9976 Joshua Rd, Apple Valley, CA 92308 — their bio; directions link = Google Maps search for that address.
- Seasonal haunted attraction, open select nights through Oct 31 — batch research (verified_facts: "Halloween season, select nights through Oct 31 (third-party guides)" — haunting.net / westcoaster.net / Daily Press coverage; no official website, no ticketing page).
- Location tag: "High Desert Haunted House" — their IG profile metadata.
- DELIBERATELY OMITTED (not published as current): ticket prices, dates, hours, themed-night lineups, scare/actor details, reviews. Their Oct 16 "Gore Night" flyer ($15, Oct 22, doors 8 PM) is a past event — not used. The visit section states honestly that dates/hours/tickets are announced night-by-night on Instagram and there is no ticket website yet.
- Contact channel on site: Instagram DM (https://www.instagram.com/victoriamanorhauntedhouse/) + Maps. No phone number shown (not re-verified from a live source by this builder).

## Photo harvest — what happened (honest account)
Every path to their real Instagram photos is blocked:
- instagram-cli `posts` / `post` return the compact social_posts_v1 collection with NO media URLs (only profile_picture_url, 150×150 scontent CDN).
- instagram.com oEmbed endpoint now returns a login-wall HTML page (no oEmbed JSON, no thumbnail_url).
- Fetching the post page / embed URL (5 URLs from research) returns the login wall; no og:image, no scontent post media, no display_url in the embed HTML.
- browser.open of a post URL returns a normalized text summary (no image URLs). Its summary confirmed post content (e.g. the Oct 16 "Gore Night" flyer) but provides no downloadable media.
- image-search for "Victoria Manor Haunted House Apple Valley" returned zero images attributable to this business (only unrelated Victorian-mansion articles and unrelated attraction sites).
- DECISION: zero photos shipped — no stock, no AI imagery, nothing invented. The hero uses the original SVG horror scene (clearly graphic, never presented as a photo). img/ holds only favicon.svg. When the business shares real haunt photos, they slot into the gallery positions the design already reserves (below).
- No third-party press photos were used: they are not the business's own photos and rights are unclear.

## Reserved photo slots (add with business's own IG photos when available)
1. Hero scene panel (640×460 SVG frame) — replace/extend with their strongest real haunt photo; keep frame, match container ratio to the photo's natural orientation or use object-fit: contain on the dark panel so the full subject shows.
2. New "Haunt nights" gallery (insert after the cards section): up to 6 photos, per-image frame matched to each photo's natural orientation (portrait→portrait, landscape→landscape), object-fit: contain or ratio-matched cover, never crop faces/scare actors; cards ≤ ~340px tall (full-view wins over uniformity per AGENTS.md).
3. All photos: export WebP ≤1100w q78, separate files under img/, lazy-load below the fold, width/height attributes set, descriptive alt text.

## Palette & type
- Near-black #0b0605 (bg) · Deep #050302 (footer/header) · Panel #140d08 / #1a100a · Bone #f5ead8 · Muted #c9b79e · Pumpkin #ff8c1a · Blood #e5383b
- Creepster (display) + Inter (body), Google Fonts with display=swap.

## Contrast audit (computed relative-luminance ratios)
| # | Text / element | fg | bg | ratio | gate | result |
|---|---|---|---|---:|---|---|
| 1 | Body text, headings | #f5ead8 | #0b0605 | 16.92 | 4.5 | PASS |
| 2 | Muted text (sub-copy, card body, footer) | #c9b79e | #0b0605 | 10.31 | 4.5 | PASS |
| 3 | Muted on cards | #c9b79e | #140d08 | 9.86 | 4.5 | PASS |
| 4 | Creepster H1 / section titles / card titles (large, incl. blood span) | #ff8c1a / #e5383b | #0b0605 | 8.65 / 4.76 | 3.0 | PASS |
| 5 | Pumpkin small text (lede strong, eyebrows, kicker, footer link) | #ff8c1a | #0b0605 | 8.65 | 4.5 | PASS |
| 6 | Card link on panel | #ff8c1a | #140d08 | 8.27 | 4.5 | PASS |
| 7 | Primary button label (dark on pumpkin) | #1a0d02 | #ff8c1a | 8.18 | 4.5 | PASS |
| 8 | Primary button hover | #1a0d02 | #ffa245 | >8 | 4.5 | PASS |
| 9 | Ghost button label | #f5ead8 | #0b0605 | 16.92 | 4.5 | PASS |
| 10 | Ghost button hover (pumpkin border/text) | #ff8c1a | #0b0605 | 8.65 | 4.5 | PASS |
| 11 | Nav links default / hover | #f5ead8 / #ff8c1a | rgba(5,3,2) | 17.25 / 8.84 | 4.5 | PASS |
| 12 | Footer text | #c9b79e | #050302 | 10.54 | 4.5 | PASS |
| 13 | Season strip text | #c9b79e / #ff8c1a | #1a0e05 | 9.69 / 8.03 | 4.5 | PASS |
Blood red is used ONLY for large display text/decoration (never small text, where it would fail 4.5). Text over the SVG illustration: the SVG is aria-hidden decorative; no text sits over it except none — all copy is in DOM text.

## Image-fit audit
No photographic images shipped (see Photo harvest). img/favicon.svg is a 64×64 vector icon — no fit issues. Hero SVG uses viewBox 640×460 with preserveAspectRatio default (contain) inside a fluid frame — full illustration always visible at any width; verified visually at 390 and 1440. No covers/crops anywhere on the page.

## Responsive verification (Playwright, headless Chromium)
- 390px: 0px horizontal overflow; menu button toggles nav; hero stacks (copy → scene); CTAs go full-width; cards single column; no overlap/clipping.
- 768px: 0px horizontal overflow; 2-column cards; visit grid stacks.
- 1440px: 0px horizontal overflow; hero two-column, hero block capped ≤ ~560px tall; cards 3-up.
- Scroll-reveal verified live: all 11 `.reveal` elements gain `.in` on scroll; no JS = content fully visible (opacity hiding only under `.js`).

## DM draft (~80 words)
Hi! I'm from Devflix — I run a software studio and I was looking at Victoria Manor's page. Peak season with Halloween 8 days out and no website at all stood out — right now anyone who wants dates, tickets or directions has to ask by DM, which must cost you visitors. I mocked up a one-page site for you (tickets/dates section, directions to 9976 Joshua Rd) so you can see it: [PREVIEW LINK]. Would something like this help this season? Happy to build it out for real if you like the direction.
