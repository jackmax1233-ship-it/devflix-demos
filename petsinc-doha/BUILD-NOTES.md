# BUILD NOTES — petsinc-doha (PetsInc, Doha Qatar)
Preview URL: https://the-cut-co.pages.dev/petsinc-doha/
Built: 23 Oct 2026 (morning batch)

## Photos (8/8 real Instagram CDN thumbnails, all verified)
Source: research JSON batch-morning-23oct-PKGULF.json → oEmbed for @petsinc.qatar (author_name verified for every post).
- 4 URLs from the JSON downloaded first try (photos 1, 2, 4, 7).
- 4 JSON URLs expired mid-build ("URL signature mismatch", 22-byte error body). Re-harvested fresh signed URLs via the public oEmbed endpoint for the SAME 4 post URLs (reels DebzSH1jZ9g, DerOcf2t5yQ, DewaZfIAHJH; post Dd57oN0DWUU) — author_name re-verified "petsinc.qatar" on each. All 8 then downloaded OK with the Instagram Referer + iPhone UA.
- NO stock or AI photos used. All converted to WebP q78 via PIL, kept at native 640px width.

| file | native px | post | visible content | where used |
|---|---|---|---|---|
| photo-1.webp | 640×1138 | reel/DeEhWz3N__B | Shopper with cart browsing the cat-toy wall | gallery — "The toy wall" |
| photo-2.webp | 640×853 | p/DdjA2WpDWkF | PetsInc storefront + orange cat; "QAR 500 voucher for whoever finds Rex" overlay | HERO (max-height 480, full view) |
| photo-3.webp | 640×1138 | reel/DebzSH1jZ9g | Team member in yellow PetsInc polo in mall | gallery — "Our team" |
| photo-4.webp | 640×1138 | reel/DeeKKHdNnmX | In-store presenter ("Things in our pet store…") | (spare — not placed; kept in assets) |
| photo-5.webp | 640×1138 | reel/DerOcf2t5yQ | Team member at counter presenting a smart pet product, food shelves behind | gallery — "At the counter" |
| photo-6.webp | 640×800 | p/Dd57oN0DWUU | "PetsInc Podcast" promo graphic, cartoon pets + mic | gallery — podcast card |
| photo-7.webp | 640×800 | p/DeMIKgLjUOe | "FOR THE PINK RIBBON" graphic — dog + kitten with pink ribbon | community — charity campaign |
| photo-8.webp | 640×1138 | reel/DewaZfIAHJH | Leash/collar/accessory display wall; "800-PETS" overlay | gallery — "Leashes & collars" |

photo-4.webp not placed on the page (spare asset in folder, harmless).

## Image-fit audit (ALL PASS)
Rule: full view of every subject, display at/below native 640px, no stretch, cover never used on photos.
- Every `<img>` has width/height attributes matching native px; CSS `img{max-width:100%;height:auto}` + per-case `object-fit:contain`.
- Hero: 3:4 image at natural aspect, `max-height:480px` desktop / 420px / 380px — full view, cap respected.
- Gallery: natural heights in a 12-col asymmetric grid (`width:100%;height:auto`) — zero cropping by construction.
- Community photo-7: natural 4:5, max-height 480 full view.
- Lazy-load on all below-fold images; hero eager.
- Captions describe only what's visible in the frame (no invented claims).

## Contrast table (computed, ALL PASS — WCAG AA)
| Pair | Ratio | Needed | Result |
|---|---|---|---|
| ink #122A3F on cream #FBF6EC (body) | 13.65 | ≥4.5 | PASS |
| terra-dark #9E3A1F on cream (accent text) | 6.33 | ≥4.5 | PASS |
| muted #4E5D6C on cream (secondary) | 6.28 | ≥4.5 | PASS |
| white on terra #C4502E (buttons) | 4.63 | ≥4.5 | PASS |
| white on ink #122A3F (buttons on terra band) | 14.70 | ≥4.5 | PASS |
| ink on card #F3EAD7 | 12.29 | ≥4.5 | PASS |
| ink on yellow #F5B301 (tags, callout) | 7.93 | ≥4.5 | PASS |
| yellow #F5B301 headings on ink #122A3F (community) | 7.93 | ≥4.5 | PASS |
| white on ink (community body) | 14.70 | ≥4.5 | PASS |
Note: lighter terracotta #C4502E (4.30 on cream) is NOT used for normal text — only as button background (4.63 with white) and never for small text.

## Fact sources (nothing invented)
All copy from research JSON facts_for_site / published captions:
- "Pawsitively Yours!" + "Your furry friend's needs in one place" — brand tagline + IG bio.
- Stores: "Lulu Mall – The Pearl" and "Lulu Mall – Gharaffa" — as published. No hours/directions invented.
- Categories: pet food, toys, accessories, reptile and aquarium supplies — as published.
- "800-PETS" — published phone word. Shown as TEXT ONLY, no tel: link (letter-mapping is an inference; safe route chosen per brief).
- Community: charity pink-product campaign ("For the Pink Ribbon" — matches their graphic); lost-pet posts with reward offers ("QAR 500 voucher for whoever finds Rex" — from their post overlay).
- RETAIL ONLY — no grooming, no vet content anywhere.
- CTAs point to https://www.instagram.com/petsinc.qatar/ (Instagram DM route).
- Honest note (NOT on site): engagement modest for ~10.2K followers (8–71 likes/post) — outreach honest-weakness flag.

## Responsive check (CSS audit — no headless Chromium on this VM)
- 1440px: hero 2-col, hero img height-capped 480 → hero ≤560px total. Gallery 12-col asymmetric, no cropping.
- 768px: hero stacks (≤860px breakpoint), gallery spans 6-col, community stacks (≤900px), categories 2-col (≤900px).
- 390px: single column everywhere; gallery spans full width; `.locale` hidden in topbar; `overflow-x:hidden` guard; all images fluid.
- No fixed widths/heights on containers; type scales with clamp(); buttons wrap. PASSED by audit; live-browser check recommended at parent level before sending the DM.

## Design
Palette: warm cream + terracotta/coral + deep navy ink, brand-yellow accents (matches their storefront/polo yellow). Fonts: Baloo 2 (display) + Nunito Sans (body), ≤2 families, display=swap. Reveal animations gated behind `.js` (visible without JS), prefers-reduced-motion respected. Single self-contained page, relative paths only. Deploys as subfolder of the-cut-co project (assets/ relative).

## DM DRAFT (for parent — do not send without approval)
> Hi! I came across PetsInc while looking at pet brands in Doha — two stores in Lulu Mall (The Pearl and Gharaffa) plus the community work you're doing, like the pink-ribbon campaign and the lost-pet posts with reward offers, really stood out.
>
> Right now the only link on your profile is a Linktree, so shoppers can't browse categories or find store info in one place. I built a quick concept of what a proper PetsInc site could look like — store info, your categories, and the community stories, using your own Instagram photos:
> https://the-cut-co.pages.dev/petsinc-doha/
>
> Would you be open to a short chat about getting something like this live for PetsInc?
