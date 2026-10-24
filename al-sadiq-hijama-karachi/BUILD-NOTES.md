# BUILD-NOTES — al-sadiq-hijama-karachi

**Lead:** Al-Sadiq Hijama Clinic · ig_handle `alsadiqhijama` · Karachi, Pakistan · hijama/cupping clinic · ~456 followers
**Built:** 23 Oct 2026 (morning batch, Devflix outreach campaign)
**Preview URL (after deploy):** https://the-cut-co.pages.dev/al-sadiq-hijama-karachi/
**Slug:** al-sadiq-hijama-karachi
**Religious framing:** "Sunnah Hijama Therapy" is the clinic's own wording — used respectfully throughout.

---

## 1. Fact sources (every on-site fact → JSON source)

Source file: `~/workspace/instagram/lead-campaign/research/batch-morning-23oct-PKGULF.json`
(lead object `ig_handle == "alsadiqhijama"`, field `facts_for_site` + `engagement_facts` + `post_urls_verified`)

| # | Fact as shown on site | JSON source |
|---|---|---|
| 1 | "Sunnah Hijama Therapy", "Natural healing & Detox", "Pain relief \| Better circulation \| Immunity boost" | facts_for_site[0] (their bio) |
| 2 | Shop M 38, Mezzanine, Centrum Mall, near Lucky One Mall, Karachi | facts_for_site[1] (Shop #38, Mezzanine, Centrum Mall, Karachi — reel caption); their own schedule graphic (photo-1) reads "Shop M 38, Centrum Mall, near Lucky One Mall, Karachi" — wording merged, nothing invented |
| 3 | Phone 0319-4909958, tel:03194909958 | facts_for_site[2] (published in bio) |
| 4 | Sunnah schedule: evening 28 Oct (Wed), 30 Oct (Fri), 1 Nov (Sun); morning 29 Oct (Thu), 31 Oct (Sat), 2 Nov (Mon) 2026 | facts_for_site[3] (their live schedule post, Oct 2026); weekday names verified independently with `TZ=Asia/Karachi date -d` — all 6 correct |
| 5 | Benefit list (pain relief / alleviates pain & stiffness; better circulation; immunity boost; flushes out toxins / natural detox; fresh energy & vitality / better health & mood) | facts_for_site[0] (bio) + their own published before/after infographic (photo-2), reworded only, no new claims |
| 6 | "Patient testimonial reels" / "Another happy patient sharing their experience" | facts_for_site[4]; engagement_facts: reel `/reel/DbOaBjNIlOZ/` (12 likes, patient testimonial) linked from photo-7; reel `/reel/DanZsk9IFZy/` (16 likes) linked from photo-8 |
| 7 | Instagram link https://www.instagram.com/alsadiqhijama/ | ig_handle — standard profile URL |
| 8 | Skin-concerns post note ("hijama therapy for skin concerns such as acne", Urdu post, "Natural · Safe · Effective") | photo-5 content (their published ad) — described, not quoted beyond visible text |
| 9 | "Hijama Sunnah Dates \| October 2026" content cadence note | facts_for_site[4] |

**Deliberately NOT on the site:** engagement numbers (2–6 likes/post — modest, normal for a 456-follower local clinic; recorded here only), the second phone number seen only inside a graphic (03462793074 — task authorized the bio phone only), hours/opening times, prices, practitioner names, any medical claims beyond the clinic's own published words.

---

## 2. Photo harvest log — 8/8 downloaded, all verified real images

Downloaded from the 8 verified `thumbnail_url`s in `post_urls_verified` (author_name verified `alsadiqhijama`) with
`curl -A "Mozilla/5.0 (iPhone; CPU iPhone OS 17_0 like Mac OS X)" -e "https://www.instagram.com/"` — **zero 403s, no substitutions.**

| File | Native size | WebP (q78) | Source post | Content | Placement |
|---|---|---|---|---|---|
| photo-1.webp | 640×640 | 47.7 KB | /p/DesFuZ-IcCl/ | Their Sunnah-dates schedule graphic (28 Oct–2 Nov) | Sunnah Dates section, full view |
| photo-2.webp | 640×640 | 66.6 KB | /p/DeeXKyaI3o2/ | Before/after hijama infographic | Benefits section, full view |
| photo-4.webp | 640×640 | 66.5 KB | /p/Ddrv_rMIna3/ | Jummah Islamic greeting artwork | Hero, full view |
| photo-5.webp | 640×640 | 49.6 KB | /p/DdnxFsQIlre/ | Urdu ad: hijama therapy for skin concerns/acne | "On their page" spotlight, full view |
| photo-7.webp | 640×1136 | 14.4 KB | /p/DbOaBjNIlOZ/ | Patient testimonial reel still (portrait) | Patients section, linked to the reel, full view |
| photo-8.webp | 480×853 | 20.6 KB | /p/DanZsk9IFZy/ | "Patient Review" reel still (portrait) | Patients section, linked to the reel, full view |
| (photo-3) | 640×640 | — | /p/Dd14rjhIspf/ | **Omitted:** its dates (17/19/21 Rabi al-Thani = 30 Sep / 2 Oct / 4 Oct 2026) have passed; showing it could mislead. |
| (photo-6) | 640×640 | — | /p/DbpD0QkMjPK/ | **Omitted:** contains the broad claim "It can cure all of the following diseases" — a site should not repeat/amplify that claim. |

Converted with PIL (no cwebp/magick on VM) → WebP q78, kept at/below native size. Display widths never exceed native (max 480px for squares, ~250px for portraits).

---

## 3. Contrast table — ALL rows PASS (WCAG AA, ratios computed from real hex values)

| # | Text → Background | Ratio | Need | Verdict |
|---|---|---|---|---|
| 1 | Ink `#1C1A16` → Cream `#F7F1E5` (body, headings, nav) | 15.44:1 | 4.5 | **PASS** |
| 2 | Deep green `#1E4534` → Cream (eyebrow, links, ghost CTAs) | 9.54:1 | 4.5 | **PASS** |
| 3 | Muted `#5A554B` → Cream (lede, figcaptions) | 6.58:1 | 4.5 | **PASS** |
| 4 | Bronze `#7C5210` → Cream (section numbers) | 6.08:1 | 4.5 | **PASS** |
| 5 | Cream → Deep green (dates H2, buttons, schedule copy) | 9.54:1 | 4.5 | **PASS** |
| 6 | Pale `#DCE8DD` → Deep green (dates lede, eyebrow, secnum) | 8.50:1 | 4.5 | **PASS** |
| 7 | Pale → Green-deep `#173A2C` (dates figcaption) | 9.91:1 | 4.5 | **PASS** |
| 8 | Cream → Green-deep (primary button hover) | 11.13:1 | 4.5 | **PASS** |
| 9 | Green → Sand `#EFE4CE` (benefit headings) | 8.52:1 | 4.5 | **PASS** |
| 10 | Ink → Sand (benefit card titles) | 13.78:1 | 4.5 | **PASS** |
| 11 | Muted → Sand (benefit card subtext) | 5.87:1 | 4.5 | **PASS** |
| 12 | Bronze → Sand (secnum in sand band) | 5.42:1 | 4.5 | **PASS** |
| 13 | Pale → Ink `#1C1A16` (footer text) | 13.76:1 | 4.5 | **PASS** |
| 14 | `#9DB3A4` → Ink (footer credit line) | 7.79:1 | 4.5 | **PASS** |

Gold `#B98A2E` is used **only** for non-text decoration (eyebrow rule bars, small SVG icon fills). It never sets text at normal size — its 2.77:1 on cream fails AA, so text use was rejected in audit. The 4.5:1 design pair (gold/cream) was replaced by Bronze `#7C5210` for section numbers (6.08:1 PASS). No text over images anywhere (captions sit on solid backgrounds).

---

## 4. Image-fit audit

- **FULL VIEW everywhere:** no `object-fit: cover`, no forced crops. Each figure's container matches the image's natural ratio (squares in square frames, portraits in portrait frames); images scale by width only (`max-width:100%; height:auto`).
- **Display ≤ native:** squares capped at 440–480px display width (native 640px); portraits capped at max-height 440px (≈248px wide, natives 640×1136 / 480×853). No upscaling, no stretch, no distortion.
- **Per-image alt** describing visible content; decorative SVG icons carry `aria-hidden`.
- `width`/`height` attributes on all 6 `<img>`s (no layout shift); `loading="lazy"` on all below-fold images; hero image eager + `fetchpriority="high"`.
- SIZES: hero image ≈420px tall on desktop (≤560 cap ✓); content images ≤480px tall ✓.

---

## 5. Responsive check (390 / 768 / 1440px)

**No headless Chromium on this VM** (`which chromium google-chrome` → nothing), so a careful CSS audit was done instead:

- 1440px: two-column grids (hero 1.08fr/.92fr; benefits .9fr/1.1fr; dates 1.05fr/.95fr; visit 1.1fr/.9fr) — all content widths bounded by `max-width:1160px`; no fixed widths; no overflow sources (`img{max-width:100%}`, flex rows all `flex-wrap`, `.date-row` wraps).
- ≤920px breakpoint: all grids collapse to single column; figures `justify-self:start` with max-widths; nav links hide (brand + call button remain); patients grid max-width 640px.
- ≤560px breakpoint: `body` 16px, H1 2.35rem, CTA buttons stack full-width (`flex:1 1 100%`), patients stack single column centered (max 300px), date rows keep wrapping, phone number shrinks to 1.6rem.
- Overflow kill list: no `position:absolute` for layout, no negative margins, no `vw`-width elements, sticky header content wraps; `text-wrap:balance` only affects headings.
- Reveal animations: gated behind `.js` (content fully visible without JS); `prefers-reduced-motion: reduce` disables all motion; focus-visible outlines on all interactive elements.

---

## 6. Honest caveats (recorded here, NOT on the site)

1. **Engagement is modest** (2–6 likes, 0–1 comments/post) — normal for a 456-follower local clinic, but a real weakness. The DM draft below acknowledges strength (operating clinic, published schedule, testimonial reels), not engagement.
2. **Two photos deliberately omitted** — photo-3 (superseded Sep/Oct dates could mislead) and photo-6 (broad "cure all diseases" claim the site shouldn't amplify). See §2.
3. **Second phone number** (03462793074) appears inside one graphic but not in the bio — not used; only the published bio number 0319-4909958 is on the site.
4. **Address merges two published wordings** — research: "Shop #38, Mezzanine, Centrum Mall"; their own graphic: "Shop M 38, Centrum Mall, near Lucky One Mall, Karachi". Site shows "Shop M 38, Mezzanine, Centrum Mall, near Lucky One Mall, Karachi" — all elements published by them.
5. **No live-browser verification** — this subagent cannot open a live browser; responsive correctness rests on the CSS audit above (no Chromium on VM). Parent should eyeball the preview link once deployed.
6. **Schedule is time-sensitive** — Sunnah dates (28 Oct–2 Nov 2026) pass within ~10 days of the DM; if the DM goes out later, the section may need a "past dates" touch-up.

---

## 7. DM draft (for parent to send from @devfl_ix)

> Assalam-o-Alaikum! I came across Al-Sadiq Hijama Clinic's page — a real, operating clinic with a published Sunnah-session calendar and patient testimonial reels is rare to see done this consistently. 👏
>
> One honest observation: right now bookings live entirely on DM and phone, and the clinic doesn't show up anywhere on Google when someone searches "hijama Karachi" — that's patients you never meet.
>
> I put together a small preview of what a proper site could look like for you — your address, Sunnah dates, and a tap-to-call button, all from your own posts: https://the-cut-co.pages.dev/al-sadiq-hijama-karachi/
>
> If something like this would help, would you be open to a quick chat about it? No pressure at all either way.

(Short, one genuine observation, the gap, the real preview link, one low-pressure question. No invented stats, no fake compliments.)

---

## 8. Deliverables

1. `~/workspace/instagram/lead-campaign/sites/al-sadiq-hijama-karachi/index.html` — single self-contained page, relative paths only, Google Fonts (Fraunces + Inter) with display=swap, inline CSS/JS.
2. `~/workspace/instagram/lead-campaign/sites/al-sadiq-hijama-karachi/assets/` — 6 WebP images (photo-1,2,4,5,7,8) + `_urls.txt` harvest manifest + `photo-N.bin` originals (build artifacts, small).
3. This BUILD-NOTES.md.
4. ZIP: `~/workspace/instagram/lead-campaign/sites/al-sadiq-hijama-karachi.zip` (index.html at zip root, assets/ alongside).

Design: deep green `#1E4534` + warm cream/sand + ink, Fraunces/Inter pairing, editorial asymmetric layout, calm natural-healing feel. No purple/blue gradients, no glassmorphism, no floating-card clutter. NOT deployed — parent handles the merged-subpath deploy to the-cut-co (relative paths are deploy-ready; do not redeploy over other demos).
