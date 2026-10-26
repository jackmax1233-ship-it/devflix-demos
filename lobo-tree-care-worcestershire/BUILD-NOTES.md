# BUILD-NOTES — Lobo Tree Care, Malvern

## Business (verified 26 Oct 2026)
- Name: Lobo Tree Care, handle @lobotreecare. Instagram author_id (instagram-cli): 17841458493230476. Followers: 1,277. Posts: 348.
- Bio: NONE published (empty bio, no website, no bio links). Services and location therefore come from captions only.
- Location: Malvern evidenced in a caption ("hedge job completed a while ago in Malvern"). Wider Worcestershire area (Droitwich/MyBuilder, Yell Worcester listing) is directory-sourced only and is NOT claimed in the site copy, which says "Malvern area".
- Gap: NO website, NO bio links. Web search found no own site for Lobo Tree Care — only directory listings (Yell, MyBuilder) and other firms (e.g. Broadleaf Tree Care, a different business).
- Activity: latest post 18 Oct 2026 (8 days before build), then 19/18/16 Sep, 23 Jul. Engagement 8–32 likes on photo posts, up to 6 comments; reels higher.
- Dedupe: grep of both trackers for "lobotreecare" / "Lobo Tree" — zero matches.

## Design
- Identity: warm cream + bark charcoal + rust accent. Fonts: Archivo (sans) + Source Serif 4 (display), Google Fonts display=swap. No gradients, no glassmorphism.
- Layout: split hero, 2-col services, 3-col square gallery, dark band. Mobile-first; stacks at ≤820px / ≤520px; max-width containers, images max-width 100%.
- Hero height: square frame, max-height 520px (under 560px cap). Gallery squares are ≤340px tall at desktop grid widths.

## Contrast table (WCAG AA, computed)
| Pair | Ratio | Verdict |
|---|---|---|
| Ink #23281E on cream #FAF6EE | 13.98:1 | PASS |
| Cream #FAF6EE on bark #2A2E22 | 12.88:1 | PASS |
| Rust #9C3D1E on cream #FAF6EE | 6.28:1 | PASS |
| White #FFFFFF on rust #9C3D1E (buttons) | 6.77:1 | PASS |
| Dark rust #7E2F16 on cream | 8.45:1 | PASS |

## Image-fit audit (FULL VIEW)
All photos are the business's own Instagram thumbnails (640px ceiling, WebP q78, separate files, no base64). All six are 640×640 square; every gallery frame is 1:1, so cover crops nothing.
| File | Post | Frame |
|---|---|---|
| hedge-malvern.webp (hero) | 18 Oct 2026, Malvern hedge job | 1:1, max-h 520px |
| chestnut.webp | 19 Sep 2026, horse chestnut top reduction | 1:1 |
| silver-maple.webp | 18 Sep 2026, 20% reduction & thin | 1:1 |
| birch-pruning.webp | 16 Sep 2026, birch reduction to historic cuts | 1:1 |
| birch-two.webp | 23 Jul 2026, two birches reduced | 1:1 |
| birch-conservatory.webp | 20 Nov 2025, silver birch over conservatory | 1:1 |
Hero visually checked: four-view hedge collage, fully in frame.

## Fact sources (post links)
- https://www.instagram.com/p/Depjq8wRTez/ — 18 Oct 2026, Malvern hedge job (hero)
- https://www.instagram.com/p/Ddd4ZGSMst4/ — 19 Sep 2026, horse chestnut top reduction
- https://www.instagram.com/p/Ddb0PNhs170/ — 18 Sep 2026, silver maple 20% reduction & thin
- https://www.instagram.com/p/DdW8q8KR_pD/ — 16 Sep 2026, birch pruning/reduction
- https://www.instagram.com/p/DbJYDDFxf1a/ — 23 Jul 2026, two birches reduced
- https://www.instagram.com/p/DRR-juLjMZU/ — 20 Nov 2025, silver birch over conservatory

## Photo-harvest log
Method: public oEmbed with iPhone UA, author_name verified = lobotreecare for every post. NOTE: two shortcodes were first tried truncated (DdW8q8KR_p, DbJYDDFxf1) and returned "No Media Match" — re-fetched with the full shortcodes above and both verified. One post in the CLI list (DWL-jMIjEqr, "Iron Man in that tree") oEmbeds to a DIFFERENT author (tohillgerard) and was deliberately NOT used — it is not Lobo's photo. All 6 used downloads succeeded, author match 6/6.

## DM draft
Hi! That Malvern hedge job of yours caught my eye — four views of it looking properly sharp. At the moment anyone searching for a tree surgeon around Malvern only finds your Instagram, so I built you a simple preview site with your hedge work, reductions and pruning in one place: https://jackmax1233-ship-it.github.io/devflix-demos/lobo-tree-care-worcestershire/ — would a site like that be handy for you?

## Honest flags
- Empty bio: no services list, phone, hours or prices published — site copy is caption-only, and services are limited to jobs actually posted.
- No tree removals claimed: captions used show reductions/pruning/hedge work, not removals.
- No live-browser responsive verification was possible from this subagent; layout verified by code audit only.
