# BUILD-NOTES — R.J Property Maintenance, Birmingham (reserve re-verified)

## Business (re-verified 26 Oct 2026; originally held as a reserve 22 Oct 2026, NOT contacted, NOT built until now)
- Name: R.J Property Maintenance (RJDoesItAll), handle @rj.doesitall. Instagram author_id (instagram-cli): 17841475260751496. Followers: 88 (was 89 on 22 Oct). Posts: 61.
- Bio: "Handyman Services | RJDoesItAll — Fixing homes, one project at a time — DM for quotes | West Midlands". Bio links: none. Website: none.
- Location: Birmingham (posts geotagged Birmingham; captions "Birmingham Based", "birminghamhandyman"). West Midlands per bio.
- Gap: NO website, NO bio links. Web search 26 Oct found no own site for this business (other Birmingham property-maintenance firms found are different businesses).
- Activity: latest post 10 Oct 2026 (16 days before build — within ~30 days), then 10 Oct, 30 Sep, 29 Sep. Engagement 2–12 likes, 0–2 comments — modest but real and consistent.
- Dedupe: appears in the master tracker ONLY as a held reserve ("verified, NOT built, NOT contacted") — no DM, no prior site. Grep of the hotel tracker: zero matches. Reuse approved by the 26 Oct morning brief, conditional on today's re-verification — all checks passed.

## Design
- Identity: brick red + warm off-white + slate. Fonts: Bitter (display serif) + Work Sans (body), Google Fonts display=swap. No gradients, no glassmorphism.
- Layout: split hero, 2-col services, 3-col portrait gallery, dark band. Mobile-first; stacks at ≤820px / ≤520px; max-width containers, images max-width 100%.
- Hero height: portrait frame, max-height 540px (under 560px cap). Gallery portraits are ≤340px tall at desktop grid widths.

## Contrast table (WCAG AA, computed)
| Pair | Ratio | Verdict |
|---|---|---|
| White #FFFFFF on brick #8C3B2E (buttons) | 7.55:1 | PASS |
| Brick #8C3B2E on off-white #F8F4EC | 6.89:1 | PASS |
| Slate #2E3338 on off-white #F8F4EC | 11.62:1 | PASS |
| Off-white #F8F4EC on slate #2E3338 | 11.62:1 | PASS |
| Dark brick #6E2B20 on off-white | 9.43:1 | PASS |

## Image-fit audit (FULL VIEW)
All photos are the business's own Instagram thumbnails (640px ceiling, WebP q78, separate files, no base64). All six are portrait (640×853, except lean-to 480×640); every frame is 3:4, matching the photos' ratio, so cover crops nothing.
| File | Post | Frame |
|---|---|---|
| driveway-cleanup.webp (hero) | 10 Oct 2026, driveway clean-up | 3:4, max-h 540px |
| driveway-renewal.webp | 10 Oct 2026, driveway renewal | 3:4 |
| garden.webp | 30 Sep 2026, garden post | 3:4 |
| lean-to.webp | 11 May 2026, lean-to roof build | 3:4 |
| transformation.webp | 11 May 2026, transformation | 3:4 |
| flooring.webp | 7 May 2026, flooring | 3:4 |
Hero visually checked: block-paved driveway, fully in frame.

## Fact sources (post links)
- https://www.instagram.com/p/DeVYmfoCD9e/ — 10 Oct 2026, driveway clean-up, "Message me for a free quote"
- https://www.instagram.com/p/DeVJ9NuDqCH/ — 10 Oct 2026, driveway renewal, "Free quote"
- https://www.instagram.com/p/Dd6ou6DDqeN/ — 30 Sep 2026, garden post
- https://www.instagram.com/p/DYMnzxkDY6_/ — 11 May 2026, lean-to roof ("Designed and built this lean-to roof myself")
- https://www.instagram.com/p/DYNEtTcjEAS/ — 11 May 2026, transformation
- https://www.instagram.com/p/DYDdnbmDRxq/ — 7 May 2026, flooring
- Other evidenced services (captions, not all pictured): wallpaper changes, subfloor replacement, plug socket changes, flat-pack assembly, bespoke office built to customer specs.

## Photo-harvest log
Method: public oEmbed with iPhone UA, author_name verified = rj.doesitall for every post, CDN thumbnails downloaded with browser Referer/UA, converted with PIL to WebP q78. All 6 downloads succeeded, author match 6/6.

## DM draft
Hi! Your driveway clean-up and renewal posts caught my eye — "get your drive looking brand new" is exactly the kind of before-and-after people in Birmingham search for. Right now they can only find you on Instagram, so I built you a simple preview site putting your driveways, garden work and home fixes in one place: https://jackmax1233-ship-it.github.io/devflix-demos/rj-property-maintenance-birmingham/ — would a site like that be useful for you?

## Honest flags
- Smallest account in this slice (88 followers, 2–12 likes/post) — real but modest engagement; flagged, not padded.
- The business is a general handyman, not a driveway-only firm; the site frames driveways/gardens first because those are its most recent posts, and home fixes second.
- No phone number, hours or prices published — none shown. The caption phrase "Guaranteed Results" was NOT repeated as a site promise; only "free quote" (evidenced twice) is used.
- No live-browser responsive verification was possible from this subagent; layout verified by code audit only.
