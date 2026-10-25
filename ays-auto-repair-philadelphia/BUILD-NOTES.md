# BUILD-NOTES — At Your Service Auto Repair, Philadelphia PA

## Business (as published by the business itself)
- Name: At Your Service Auto Repair (Instagram display name: "At your service auto repair")
- Instagram: @aysmobleautorepair — handle spelling copied exactly, including "moble"
- Location: Philadelphia & surrounding areas, USA (mobile service; no shop address published, so none is shown on the site)
- Contact: call/text (215) 520-1100, or Instagram DM. No email, website, or booking page published.
- Followers at check (25 Oct 2026, via instagram-cli profile): 439. Following 28, posts 75.
- Bio (summarised): "We Come To You! Mobile Mechanic — Diagnostics, Brakes, No Starts, Suspension — Call/Text (215) 520-1100"
- Services (from the business's own captions/graphics, summarised — not copied verbatim): most cars & light trucks; brake pads & rotors; oil changes; starters & alternators; batteries; suspension / tie rods / control arms; diagnostics; no-starts; tune-ups; A/C service; fuel pumps; radiators; wheel bearings / hub assemblies; serpentine belts; thermostats (in their service graphic); discounted parts; junk cars bought.
- Other published facts used: same-day service available; credit cards accepted (Visa, Mastercard, American Express, Discover); "we come to you" — home, job, or roadside; "save the tow, skip the shop wait" (paraphrased on the site).
- Deliberately NOT claimed: no hours, no street address, no reviews, no ratings, no years in business, no certifications — none were published in the sources checked.

## Gap re-verification (done 25 Oct 2026, before building)
1. **Bio link — checked twice, no link exists.** instagram-cli profile for @aysmobleautorepair returned `bio_links: []` and `website: null`. The bio contains only the service line and the phone number.
2. **Web search — no own site for THIS business.** Search "At Your Service mobile mechanic Philadelphia 215-520-1100 website" returned only different businesses: aysmms.com (Rutledge, TN, phone +1 423-438-7214), mobilemechanicsatyourservice.site (Markham, ON, Canada, phone +1 647-363-6692), at-your-service.co.uk (UK), plus unrelated Philadelphia competitors. None matches the Philadelphia phone number, handle, or branding. A second search for the exact handle returned no website for this business.
3. **Graphics/domain check — no domain printed in any post graphic used.** The three graphics harvested show only the business name, services, prices, and the phone number (215) 520-1100. No URL, QR code, or booking domain appears in them.
4. **Conclusion: gap confirmed — the full service menu and prices live only in Instagram captions/graphics; booking is call/text/DM only. Site built.**
5. **Not India-based:** instagram-cli profile country = US; all posts place the business in Philadelphia, PA. **Age:** profile `birthday` = null and no age is stated anywhere in the sources checked — there is no statement that the operator is under 18.

## Published prices (re-verified in captions by the builder, not just taken from the brief)
- **$140 front brake pads** — parts + installation included, most cars. Confirmed in the latest reel (DeuD3OoKo_2, 20 Oct 2026), in DbWAgYIlhb0, and printed in the DbxzLYaFoeO graphic.
- **$100 oil change** — oil + filter included, most cars. Confirmed in the same three sources.
- Both prices are labelled on the site as "as published" and "most cars". No other prices are shown.

## ⚠️ Phone-number discrepancy — read before sending the DM
- The reel DeuD3OoKo_2 caption (via oEmbed) prints **215-502-0110**, while the bio, the other four verified posts, and all three graphics print **215-520-1100**.
- The site uses **(215) 520-1100** everywhere, as it is the overwhelmingly consistent number (bio + 4 posts + graphics). The single 502-0110 reading looks like a caption typo, but it is flagged here so the parent can confirm the correct number before any DM that quotes a phone number. The DM draft below does not quote a phone number, so it is unaffected.

## Photo harvest log (oEmbed route, iPhone UA, browser Referer/UA for download)
All thumbnails verified: oEmbed `author_name` = aysmobleautorepair for the five posts below.

| File | Source post | Natural size | What it shows |
|---|---|---|---|
| images/hero-brake-job.webp | reel DeuD3OoKo_2 (20 Oct 2026) | 640 × 1136 (portrait) | Real on-site brake job: SUV raised, wheel off, tools on the ground |
| images/specials-brakes-oil.webp | post DbxzLYaFoeO | 640 × 640 (square) | Business specials graphic: $140 brakes / $100 oil change |
| images/specials-brakes-oil-alt.webp | post DbWAgYIlhb0 | 640 × 640 (square) | Near-identical variant of the same specials graphic |
| images/mobile-mechanic-flyer.webp | posts DTIaaGsDaYB and DS-MyZbjV0R | 640 × 828 (portrait) | Business flyer: mechanic at work, brakes/rotors/suspension list |

- **Reel poster frame:** inspected visually — **no baked-in play button** is visible in the DeuD3OoKo_2 thumbnail. It is a clean work photo, used as the hero.
- **Duplicate thumbnail:** DTIaaGsDaYB and DS-MyZbjV0R return the byte-identical thumbnail (same MD5), so they yield one image, not two. Distinct images used: **4** (from 5 verified posts).
- **Excluded post — DKPjYjoN9Uk:** oEmbed and instagram-cli both show this post belongs to **@modern_languagephilly** (author "Kashif"), NOT to @aysmobleautorepair, even though it mentions the same phone number and other handles. Its photo and its $40/$20 prices were **not used** and are **not on the site**. If the parent wants that post investigated, it needs separate verification that it is the same operator.
- **No stock/AI photos used.** Every image is the business's own Instagram thumbnail, converted to WebP at quality 78. Source files were only 640 px wide (Instagram's oEmbed ceiling), so no upscaling was done; displayed sizes are at/below native width.
- **Shortfall disclosure:** the gallery is thin (4 distinct images, two of them near-identical specials graphics) because that is all the verified own-account material yielded. This is disclosed honestly here; the site does not pad it with stock imagery.

## Contrast table (WCAG AA, normal text needs 4.5:1 — all pass)
Ratios computed from the exact hex values used in index.html.

| Text | Background | Ratio | Pass? |
|---|---|---|---|
| #1C1C1C body text | #F5F1E8 page | 15.12:1 | Yes |
| #4A4A44 secondary text | #F5F1E8 page | 7.91:1 | Yes |
| #1C1C1C text | #FFFFFF cards | 17.04:1 | Yes |
| #4A4A44 secondary text | #FFFFFF cards | 8.92:1 | Yes |
| #FFFFFF text | #161616 header/topbar/dark sections | 18.10:1 | Yes |
| #F5F1E8 text | #161616 dark sections | 16.05:1 | Yes |
| #D8D2C4 muted text | #161616 dark sections | 12.01:1 | Yes |
| #FFFFFF button text | #A81E1E red button | 7.32:1 | Yes |
| #FFFFFF text | #8F1D1D "Why mobile" section | 8.89:1 | Yes |
| #161616 text | #F2C200 yellow badge | 10.76:1 | Yes |

No purple/blue gradients, no glassmorphism, no glowing borders, no decorative icons. Palette is garage-inspired: charcoal, paper-white, workshop red, hazard yellow.

## Image-fit audit
- Hero: container aspect-ratio 640/1136 matches the photo exactly; `object-fit: contain`; max-width 300 px → displayed height ≈ 533 px, under the ~560 px desktop hero cap. Full subject visible (car, wheel, tools) — nothing cropped.
- Square graphics: container aspect-ratio 1/1 matches the 640 × 640 files; `object-fit: contain` on a #161616 background. Full graphic visible, including prices and phone number.
- Flyer: container aspect-ratio 640/828 matches the file; `object-fit: contain`. Full flyer visible.
- `object-fit: cover` is not used anywhere. No image is stretched or distorted.

## Responsive / verification status
- **CSS-audit only — no live viewport check was possible.** This subagent cannot operate a live browser, so the site was NOT opened at 390/768/1440 px in a real browser. What was verified by code audit: mobile-first single column under 768 px; hero stacks; grids switch to 2 columns at 768 px and 3 (services) at 1100 px; all images use `max-width: 100%` with matching aspect ratios; no fixed widths wider than the viewport; nav wraps. **Parent should do a live viewport check before pitching, or note this caveat to the business.**
- No base64 images in the HTML. All internal images/links are relative (`images/*.webp`, `#anchors`). External links are only Google Fonts (allowed) and the business's own Instagram profile. No pages.dev / Netlify / GitHub URLs appear inside the site.

## Files
- `index.html`
- `images/hero-brake-job.webp` (89 KB, 640 × 1136)
- `images/specials-brakes-oil.webp` (90 KB, 640 × 640)
- `images/specials-brakes-oil-alt.webp` (93 KB, 640 × 640)
- `images/mobile-mechanic-flyer.webp` (102 KB, 640 × 828)
- `BUILD-NOTES.md` (this file)

## DM draft (short, natural, personalised — for the parent to send, not sent by the builder)
> Hi! I came across At Your Service on Instagram — I liked how clear your page is that you come to the customer instead of making them come to a shop. Right now though, someone who needs brakes or an oil change has to dig through your posts to find the full list of what you do and your $140 brakes / $100 oil change specials, and there's nowhere to send them except a DM or a call.
>
> I made you a simple one-page website that puts all of that in one place — your services, the specials, and a big call/text button: https://jackmax1233-ship-it.github.io/devflix-demos/ays-auto-repair-philadelphia/
>
> Would you like me to send you a version with your details on it so you can have a look?
>
> — Devflix

## Why a good prospect
- Real, active business (75 posts, latest reel 20 Oct 2026) with a genuinely useful service and clear published prices — but zero web presence: no site, no booking page, not even a link in bio. Every customer currently has to DM or call blind.
- The preview writes itself from their own material (services, specials, photos all already published), so the pitch is concrete, not generic.
- Small account (439 followers) in a competitive local trade — a one-page site that captures "mobile mechanic Philadelphia" searches and lets customers see prices before calling is a direct, low-cost win for them.

## author_id notes (for the parent's DM targeting)
- **oEmbed author_id for @aysmobleautorepair: 48980877411** (returned identically for all five verified own-account posts).
- **instagram-cli author_id for @aysmobleautorepair: 17841449122332609** (returned identically for all of the account's posts in the instagram-cli `posts` result; the account's display name there is "At your service auto repair", follower count 439).
- The two IDs differ because they come from two different ID systems (Instagram's public oEmbed user ID vs. the Meta/Graph-scoped ID used by instagram-cli).
- **Parent should use the instagram-cli ID 17841449122332609 for any instagram-cli / DM tooling**, since that is the ID the connected Instagram tooling resolves for this account. The oEmbed ID 48980877411 is recorded here only for cross-reference.
- For contrast, the excluded DKPjYjoN9Uk post resolves to a different account entirely: oEmbed author_id 50650284012 / instagram-cli author_id 17841450760361285, username modern_languagephilly — do not DM that account about this business.
