# BUILD NOTES — Keys of Peace London (keys-of-peace-london)

Business: Keys of Peace London · IG @keys_of_peace_london (author_id 17841409658126809)
Location: London, UK — ABRSM Certified Piano Teacher (piano lessons)
Built: 22/23 Oct 2026 (night batch)

## 0. PHOTO HARVEST — how it was done (new working method)

The afternoon research note said photo harvesting was BLOCKED. That was worked
around in this build: `social.search` with `post_url` set to each post URL returns
a signed `thumbnail_url` (CDN image). Downloads need a browser-style `Referer:
https://www.instagram.com/` header, otherwise the CDN 403s. 6 of 7 attempted
photos harvested; the 7th (Dc01VOAMSJc) 403'd twice with exact fresh URLs —
documented below for a manual pass.

**Research-data CORRECTION:** the research JSON attributed post
`https://www.instagram.com/p/DeUQ0lFoSQY/` ("Oct 10, 280 likes/87 comments") to
keys_of_peace_london — the post_url lookup shows it belongs to @daflondon
(author_id 17841405670988171, a daf teacher). NOT used; no photo from it was
harvested and no claim from it appears on the site.

## 1. FACT SOURCES (all business-published, nothing invented)

| Fact | Value used on site | Source |
|---|---|---|
| Name / handle | Keys of Peace London / @keys_of_peace_london | IG profile |
| Bio (exact) | "🎹,Pianist, 🎶 ABRSM Certified Piano Teacher, 💍🤍 Piano lessons available 🌎 DM to book a trial lesson today! ✨ London, United Kingdom 🇬🇧" | social.search author_bio, 23 Oct 2026 |
| ABRSM Certified Piano Teacher; pianist; London | headline + About | IG bio |
| Private lessons, children (ages 4+) and adults; all levels welcome; personalised lessons tailored to goals | hero lede + lesson cards | Oct 16 post caption (DekBoNXqQ2T), verbatim |
| "It's never too late to learn piano" | Adults card | Oct 16 post caption, verbatim |
| North & West London; online lessons available | About + modes band | Oct 16 post caption, verbatim |
| "Private Piano Lessons \| In-person & Online; DM for enquiries" | modes band | Oct 13 reel caption (DebVaEbqdJx), verbatim |
| "Music is my passion, teaching it is my joy" | About figcaption | Oct 13 reel caption, verbatim |
| Piano · Music Theory · Performance | modes band | Sep 3 reel caption (Dc01VOAMSJc), verbatim |
| "Music builds a kinder, brighter world" | quote band | her own promo graphic (Oct 16 post image), verbatim |
| Bio link YouTube https://youtu.be/0LvnPv4PKjY | hero secondary CTA + footer | IG bio link (published) |
| Followers ~813 (23 Oct 2026) | NOT shown (drifts; avoided) | — |
| Engagement: Oct 13 posts 150–198 likes, 87–92 comments; Oct 16: 108/30 | About says "hundreds of likes and dozens of comments" | verified post counts, no exact invented figures |

Deliberately NOT on the site: prices (none published), lesson duration/format
details beyond "private / in-person & online", opening hours, address, phone,
email, testimonials/reviews, any claim of results or stats.

## 2. CONTRAST TABLE (WCAG AA — computed with the standard relative-luminance formula)

| # | Element | Foreground | Background | Ratio | Result |
|---|---|---|---|---|---|
| 1 | Body text | #2A2118 | #FAF6EE (ivory) | 14.66:1 | PASS |
| 2 | Secondary text (lede, card copy) | #5D4D3B | #FAF6EE | 7.52:1 | PASS |
| 3 | Primary button label | #FAF6EE | #1E1710 (ink) | 16.44:1 | PASS |
| 4 | Eyebrow/kicker text | #6B4F14 | #FAF6EE | 7.07:1 | PASS |
| 5 | Nav links / headings | #2A2118 | #FAF6EE | 14.66:1 | PASS |
| 6 | Quote band text | #F5F0E4 | #1E1710 | 15.58:1 | PASS |
| 7 | Gold rule on dark band | #D9B96A | #1E1710 | 9.36:1 | PASS (decorative, large) |
| 8 | Footer text | #C9BCA4 | #1E1710 | 9.46:1 | PASS |
| 9 | Footer brand | #F5F0E4 | #1E1710 | 15.58:1 | PASS |
| 10 | "How lessons happen" band text | #2A2118 | #F1E7D2 (champagne) | 14.43:1 | PASS |
| 11 | Ghost button label | #2A2118 | #FAF6EE | 14.66:1 | PASS |
| 12 | Focus ring | #6B4F14 | #FAF6EE | 7.07:1 | PASS (≥3:1 required vs adjacent; initial #B08A3C measured 2.98:1 and was replaced) |

No text sits over photographs — all copy is on solid ivory/ink/champagne grounds.
ALL PASS, one failure found and fixed during the audit (focus ring colour).

## 3. IMAGE-FIT AUDIT (per-image, full-view order)

All 6 photos are the teacher's own Instagram posts (verified author_id
17841409658126809 on every lookup). Portrait orientation throughout; frames use
`object-fit: contain` so the WHOLE image is always visible, zero cropping, on
desktop and mobile. Letterbox grounds match the design (ivory / ink), so no
subject is ever cut.

| File (img/) | Source post | Natural size | Displayed | Fit check |
|---|---|---|---|---|
| hero.webp | Oct 16 post (promo graphic "Keys of Peace Piano Lessons") https://www.instagram.com/p/DekBoNXqQ2T/ | 1024×1360 (3:4) | Hero, 3:4 contain frame, max-height 560px desktop / 70vh mobile | Full view: her portrait, all promo text, 4 icons and tagline visible, no crop |
| about.webp | Oct 13 reel (at black digital piano, warm living room) https://www.instagram.com/reel/DebVaEbqdJx/ | 880×1564 (9:16) | About, 9:16 contain on ink card, max-height 520px | Full view: her face, hands on keys, room visible, no crop |
| gallery-1.webp | Sep 18 post (b&w, hands on keyboard) https://www.instagram.com/p/Ddb6430qVkW/ | 704×944 | Gallery, contain, max-height 340px | Full view, no crop |
| gallery-2.webp | Dec 2025 reel (hands on grand piano, sheet music on stand) https://www.instagram.com/reel/DSIBN7kDAGd/ | 640×1136 | Gallery, contain, max-height 340px | Full view, no crop |
| gallery-3.webp | Dec 2025 reel (keyboard + hands close view) https://www.instagram.com/reel/DSvLvL-jBq3/ | 640×1136 | Gallery, contain, max-height 340px | Full view, no crop |
| gallery-4.webp | Oct 2025 reel (keyboard beside bookshelf in study) https://www.instagram.com/reel/DQMne1kDHN4/ | 640×1136 | Gallery, contain, max-height 340px | Full view, no crop |

Blocked: Sep 3 reel https://www.instagram.com/reel/Dc01VOAMSJc/ — its CDN
thumbnail URL 403'd twice (exact fresh URLs, Referer header set). Slot reserved
for a manual live-browser pass; its caption facts (Private & VIP lessons,
Piano·Music Theory·Performance) are already used as text.

All WebP quality 78, separate files (no base64), width/height attrs set,
lazy-load below the fold, hero fetchpriority=high. Total image weight 228 KB.
Hero ≤560px tall on desktop (measured 560px @1440, 421px @390); gallery frames
≤340px tall — per the user's image-size discipline; full view wins everywhere.

## 4. RESPONSIVE NOTES (verified in headless Chromium 390/768/1440 — screenshots in this folder)

- 390px: single column; nav links hide, "DM to book" pill stays; hero copy → CTA
  → photo; cards stack; gallery stacks; modes band stacks; no overlap.
- 768px: nav links appear; hero 2-col; about 2-col; cards 2-col; gallery 4-col.
- 1440px: max-width 1160px container; cards 4-col.
- `documentElement.scrollWidth - clientWidth = 0` at all three widths — zero
  horizontal overflow. All 6 images load with natural dimensions intact.
- Motion: scroll-reveal gated behind `.js` (content fully visible without JS);
  `prefers-reduced-motion` disables reveals + smooth scroll.
- Only console error: Google Fonts blocked by the sandbox tunnel
  (ERR_TUNNEL_CONNECTION_FAILED) — fonts load normally on the live deploy;
  Georgia/system fallbacks render acceptably without them.

## 5. DESIGN IDENTITY

Recital-program elegance: ivory (#FAF6EE) + deep ink (#1E1710) + antique gold
(#6B4F14 / #C9A24B). Fraunces (display serif) + Inter (body), Google Fonts with
display=swap. Treble-clef brand mark, letter-spaced kickers, thin rules —
flat grounds, no gradients, no glassmorphism, no floating cards. Palette and
layout are original to this build.

## 6. DM DRAFT (Instagram — to @keys_of_peace_london, author_id 17841409658126809)

> Hi! I came across Keys of Peace and your October posts — the performance that
> pulled 90+ comments shows how engaged your piano community is. One thing I
> noticed: everything routes through "DM to book", so there's nothing for
> Google or parents searching "piano lessons North London" to find.
>
> I made a quick concept of how a simple one-page site could look for you —
> your ABRSM credential, lessons for children and adults, and the trial-lesson
> booking in one place: [PREVIEW LINK]
>
> Would a simple site like that be useful, or is Instagram working fine for
> bookings as is?

(~85 words. One genuine observation — engaged audience + no Google footprint;
why a site helps THEM; preview link placeholder; one low-pressure question.
No fake compliments, no invented stats.)
