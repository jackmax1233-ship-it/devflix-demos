# BUILD NOTES — Fix Stop (Dublin) preview site
Built 2026-10-22 ~11:00 PKT · site folder: ~/workspace/instagram/lead-campaign/sites/fix-stop-dublin/

## Facts used (sources)
All facts from the business's own Instagram (@info.fixstop, 646 followers) and the research
handoff (~/workspace/instagram/lead-campaign/research/batch-morning-22oct-UKIE-part2.json),
verified 2026-10-22 via social.search post_url lookups:
- Name: Fix Stop · IG: https://www.instagram.com/info.fixstop/ · author_id 17841407031454229
- Location: Dublin, Ireland — NOT India (geography gate passed)
- Address (published in captions): 352 North Circular Road, Phibsborough, Dublin 7 (D07 F44C)
- Phone (published in captions): +353 863697222
- Services (bio + captions): screen repair — any phone, any model; charging port repair — any phone;
  brands iPhone, Samsung, Huawei, Xiaomi, tablets; also sells accessories & screen protection
- Hours: NOT published — site says "Opening hours aren't listed online" (absent marked, nothing invented)
- Website: absent (bio link is only a Facebook page — treated as no website per task rules)
- Opportunity: no website; enquiries via phone/DM only; Google can't land customers anywhere
- Nothing invented: no reviews, no ratings, no prices, no turnaround claims in site copy.
  The repair-promo image is their own posted offer graphic; caption says "our own offer, posted on our page".

## Images (all from their own IG posts, fresh CDN signatures re-fetched 2026-10-22 ~11:00 PKT)
Source posts: reel/DefSnwosKq_ (2026-10-14) · p/DeLu54GMAJe (2026-10-06) ·
reel/Dd8g_N7sNFS (2026-10-01) · reel/DT-G6NIDEfW (2026-01-26) · reel/DV3Sd8ejPga (2026-03-14)

| Asset | Source post | Natural size → shipped | Fit decision |
|---|---|---|---|
| hero-cracked-screen.webp | reel DefSnwosKq_ (cover frame) | 1284×2283 → letterbox cropped → 1200×1528 | Portrait kept portrait; full cracked phone visible, nothing cut; displayed at min(520px,64vh) height, width auto — never cropped |
| before-after.webp | reel Dd8g_N7sNFS (cover frame) | 1284×2283 → black bands cropped → 1100×608 | Landscape band kept landscape; both phones + Before/After labels fully in frame |
| charging-fix.webp | p/DeLu54GMAJe | 1280×720 → 1100×619 | Natural 16:9 kept, full graphic visible |
| repair-promo.webp | reel DV3Sd8ejPga (cover frame) | 640×1136 → 640×1020 | Portrait kept portrait, full promo in frame |
| img4 (reel DT-G6NIDEfW cover) | — | REJECTED — blurry cover frame, low quality, subject not clearly visible | not used |

All WebP quality 78, separate files, no base64. Hero eager + fetchpriority; rest lazy.
Letterbox crops remove only pure-black bars (brightness scan), never the subject.

## Contrast table (WCAG, computed — all ≥ 4.5:1 for normal text)
| Pair | Ratio | Used for |
|---|---|---|
| #F6F5F0 paper / #10201C ink | 15.45 | body text on light |
| #FFFFFF card / #10201C ink | 16.86 | headings on cards |
| #FFFFFF card / #2E3B38 body | 11.67 | body copy on cards |
| #F6F5F0 / #0E4D3F teal | 8.94 | kickers, links on light |
| #F6F5F0 / #9A5B00 amber | 4.97 | amber text on light |
| #0C2620 deep / #FFFFFF | 15.98 | hero/footer text |
| #0C2620 deep / #37D67A green | 8.42 | eyebrow, green text on dark |
| #0C2620 deep / #FFB020 amber | 8.74 | badge text on dark |
| #37D67A green btn / #0B3D2E text | 6.43 | primary call button |
| #0C2E27 dark btn / #FFFFFF | 14.63 | dark button |
| focus outline #FFB020 on dark/light | ≥3:1 | focus-visible ring |

No text over photos except the hero badge (amber #FFB020 on #1d1500 chip — 8.7:1) and figcaptions on
paper cards. No dark-text-on-dark-image anywhere.

## Responsive / full-view audit (static review — parent to verify live)
- Mobile-first; single-column grids collapse via min-width media queries; no fixed widths > 100%.
- Nav links hidden <760px (call button remains); hero stacks, image height min(520px,64vh) width auto.
- Hero ≤560px tall on desktop (capped 520px). Content images ≤480px tall naturally at their shipped widths.
- No horizontal overflow sources: wrap max-width + padding, images max-width:100%, flex-wrap on CTAs/pills.
- Reveal animation gated behind .js class (content visible without JS); prefers-reduced-motion disables it.
- Fonts: Space Grotesk (display) + Inter (body), Google Fonts with display=swap, 2 families max.
- No gradients/glow/glassmorphism/floating cards; business-specific tech-craft identity.

## DM draft (for parent — DO NOT send myself; [PREVIEW LINK] placeholder)
> Hi — I came across Fix Stop while looking for repair shops in Phibsborough and noticed you don't have a website yet, so anyone Googling "phone repair Dublin 7" can't actually find you — they'd have to already know your Instagram.
>
> I mocked up what a simple site for the shop could look like, using your own photos: [PREVIEW LINK]
>
> Would something like that be useful for getting walk-ins from Google, or are phone and Instagram DMs working fine for you as-is?

## Deliverables
- index.html + assets/ (4 WebP) in fix-stop-dublin/
- ZIP: ~/workspace/instagram/lead-campaign/sites/fix-stop-dublin.zip (created, 147 KB, verified contents)
- Parent handles: Cloudflare Pages deploy + DM send + tracker logging.
