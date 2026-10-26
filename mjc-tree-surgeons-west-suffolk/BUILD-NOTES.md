# BUILD-NOTES — MJC Tree Surgeons, West Suffolk

## Business (verified 26 Oct 2026)
- Name as shown on Instagram: MJC tree surgeons (handle @mjc.arb, no display name published).
- Instagram author_id (instagram-cli): 17841408477898406. Followers: 391. Posts: 138.
- Location: West Suffolk (bio); Bury St Edmunds evidenced in captions ("burystedmunds", "butter market").
- Bio (verbatim sense): "A bunch of tree surgeons smashing it out across West Suffolk fuelled by scratch cards, red bull, custard creams, coffee and bacon rolls..."
- Gap: NO website, NO bio links at all. Web search for this West Suffolk business found no own site — the other "MJC" tree firms surfaced (Huntingdon mjctreecare.co.uk; Hampshire mjc-treesurgeons.co.uk) are different businesses in different places, not this one.
- Activity: latest post 21 Oct 2026 (5 days before build), then 1 Oct, 28 Sep, 15 Sep, 14 Sep — all within 30 days. Engagement 9–46 likes, up to 7 comments.
- Dedupe: grep of ~/workspace/instagram/lead-campaign/tracker.md and ~/workspace/hotel-outreach/tracker.md for "mjc.arb" / "MJC" — zero matches (RJ reserve line is the only "MJC" neighbour, unrelated).

## Design
- Identity: deep forest green + warm cream + dark amber accent. Fonts: Fraunces (display serif) + Inter (body), Google Fonts display=swap. No gradients, no glassmorphism, no floating cards.
- Layout: editorial split hero, 3-col services, 3-col gallery, dark band for recent work. Mobile-first; grids stack to 2-col at ≤820px and 1-col at ≤520px; containers are max-width, images max-width 100% — no horizontal overflow by construction. Verified by code audit at 390/768/1440 logic (no live-browser check available to this subagent; parent to verify live if desired).
- Hero height: square frame, max-height 520px (under the 560px cap). Gallery frames ≤340px at desktop grid widths.

## Contrast table (WCAG AA, computed)
| Pair | Ratio | Verdict |
|---|---|---|
| Cream #F7F3E8 on forest #1E3D2A | 10.79:1 | PASS |
| Forest #1E3D2A on cream #F7F3E8 | 10.79:1 | PASS |
| White #FFFFFF on forest #1E3D2A | 11.96:1 | PASS |
| Ink #22301F on cream #F7F3E8 | 12.54:1 | PASS |
| Dark amber #8A5A00 on cream (eyebrow, large/bold) | 5.35:1 | PASS |
| Amber button text #1E3D2A on #E8C87A | ~9:1 (dark on light) | PASS |

## Image-fit audit (FULL VIEW)
All photos are the business's own Instagram thumbnails (640px ceiling, converted to WebP q78, separate files, no base64).
| File | Natural | Frame | Fit |
|---|---|---|---|
| hero.webp (pole rescue, 21 Oct) | 640×643 (~1:1) | 1:1, max-h 520px | cover in a matching-ratio frame — no subject cropped |
| felling.webp | 640×853 (3:4) | 3:4 | matched — no crop |
| pruning-market.webp | 640×480 (4:3) | 4:3 | matched — no crop |
| pollarding.webp | 640×480 (4:3) | 4:3 | matched — no crop |
| crown-lift.webp | 640×480 (4:3) | 4:3 | matched — no crop |
| reserve-felling.webp | 640×480 (4:3) | 4:3 | matched — no crop |
Hero visually checked: two climbers high in the tree, fully in frame.

## Fact sources (post links)
- https://www.instagram.com/p/Dewwe71oP_g/ — 21 Oct 2026, pole rescue practice (hero)
- https://www.instagram.com/p/Dd9Qi4CoFx8/ — 1 Oct 2026, felling ("Ava's first dogs tooth")
- https://www.instagram.com/p/Dd9QDPnI2i4/ — 1 Oct 2026, Ram Meadow poplar felling
- https://www.instagram.com/p/Dd1UxxUCFTG/ — 28 Sep 2026, Butter Market London planes
- https://www.instagram.com/p/DdT82cxiAcl/ — 15 Sep 2026, re-pollarding/reducing/thinning/crown lifting
- https://www.instagram.com/p/DdRWF66iBMT/ — 14 Sep 2026, crown lifting a London plane, Bury St Edmunds

## Photo-harvest log
Method: public oEmbed with iPhone UA, author_name verified = mjc.arb for every post, CDN thumbnails downloaded with browser Referer/UA, converted with PIL to WebP q78. All 6 downloads succeeded, author match 6/6.

## DM draft
Hi! I came across your Butter Market London plane work — three days pruning those planes in Bury St Edmunds really stood out. Right now anyone searching for a West Suffolk tree surgeon finds only your Instagram, so I built you a simple preview site with your services and recent jobs (felling, pruning, pollarding, crown work) in one place: https://jackmax1233-ship-it.github.io/devflix-demos/mjc-tree-surgeons-west-suffolk/ — would a site like that be useful for you?

## Honest flags
- No display name, phone number, email, hours or prices are published by the business — none are shown.
- "Aerial rescue practice" appears in a caption but is internal training, not a customer service — deliberately NOT listed as a service.
- No live-browser responsive verification was possible from this subagent; layout verified by code audit only.
