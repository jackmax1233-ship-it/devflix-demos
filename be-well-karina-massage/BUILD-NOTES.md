# Be Well with Karina — preview site build notes

Author ID (for DM): **17841425020460438** · IG: @bewellwithkarina · Karina Meidell, RMT · Etobicoke / Toronto's west end, ON · 46 followers
Built: 2026-10-23 ~01:30 PKT. Deploys as subpath https://the-cut-co.pages.dev/be-well-karina-massage/ (all asset paths relative).

## Photos (her own Instagram photos, harvested via instagram-cli post + hatch-zeitgeist thumbnail URLs)
| file | source post | size | content check |
|---|---|---|---|
| img/treatment.webp (1080×1440, 45 KB; -640 variant 23 KB) | https://www.instagram.com/p/DeffgK-mNtG/ (2026-10-14) | hands-on massage photo with her "What are we working on today?" overlay |
| img/october-special.webp (1080×1440, 68 KB; -640 variant 36 KB) | https://www.instagram.com/p/Dd_zYZkkSGD/ (2026-10-02) | her "October Special — $20 off your first visit" branded graphic |
| img/intro.webp (1080×1440, 78 KB; -640 variant 41 KB) | https://www.instagram.com/p/DdwLtEbkR47/ (2026-09-26) | her "Hi, I'm Karina!" intro graphic with portrait |
All WebP q78, ≤1100w, separate files (no base64). Hero `fetchpriority="high"`, below-fold images `loading="lazy"` with `srcset` 640/1080w and width/height attrs.
No blockers — no stock/AI photos used.

## Contrast audit (WCAG AA, computed luminance ratios — all pass ≥4.5:1)
| pair | ratio |
|---|---|
| ink #2A2F2C on cream #FAF6ED | 12.63 ✓ |
| pine #2F4A3E on cream | 8.97 ✓ |
| muted #5B645E on cream (body small text) | 5.68 ✓ |
| rust #8F5326 on cream (eyebrows, links) | 5.67 ✓ |
| cream text on rust #8F5326 (buttons) | 5.67 ✓ |
| cream on slate #3C4A5E (offer band) | 8.34 ✓ |
| offer body #EFE7D4 on slate | 7.31 ✓ |
| offer fine #CFC6B2 on slate | 5.30 ✓ |
| eyebrow #F0C896 on slate | 5.75 ✓ |
| footer text #E7DFCB on pine | 7.29 ✓ |
| footer fine #B9C4B5 on pine | 5.36 ✓ |
| offer button #2A2118 on gold #E8B44C | 8.32 ✓ |
| pine on white (steps) | 9.68 ✓ |
No failures; no fixes needed. Visible `:focus-visible` outline on links/buttons. `prefers-reduced-motion` respected; `.reveal` gating only applies when JS runs (`.js` class).

## Image-fit audit (full-view gate)
All photos are 4:5 portrait; every frame uses `aspect-ratio:3/4` with `object-fit:contain` — full subject always visible, zero cropping. Hero arch frame ≤560px tall (467/520/560 measured at 390/768/1440); card frames ≤480px. Verified in headless Chromium at 390/768/1440: no horizontal overflow, no overlap, no clipped text, nav collapses cleanly on mobile. All `.reveal` elements confirmed visible after scroll (0 still hidden); 0 JS errors. Screenshots: /tmp/shot-m390b.png, /tmp/shot-t768b.png, /tmp/shot-d1440b.png.

## Fact sources (only published facts used)
- Name "Karina Meidell, RMT", bio "Registered Massage Therapist / Etobicoke, ON", Toronto west end, booking via link-in-bio / kingswaywellnessclinic.com — from instagram-cli `post` records for the 3 posts + research JSON (batch-night-22oct-CA.json).
- October $20-off first treatment (first-time patients, October 2026) — her 2026-10-02 caption + October Special graphic.
- Approach copy ("inclusive and safe space where you feel heard and supported", "personalized, evidence-informed approach", "own journey with chronic pain", "injury recovery, pain management, overall well-being") — her 2026-09-26 intro caption.
- Care-list items (regular maintenance, pain relief, mobility & flexibility, everyday aches & tension, improving circulation, relaxing & resetting, joint mobility) — her 2026-10-14 caption + treatment-post graphic bullets, rephrased in her words.
- NOT invented: no prices beyond the published $20 offer, no hours, no clinic address, no phone, no reviews, no modalities she didn't name.

## DM draft (~80 words)
Hi Karina — loved your October posts, especially the intro about how your own journey with chronic pain shaped the way you care for clients. That's exactly the kind of story that deserves more than a Linktree. I built you a quick one-page preview site using your own posts and your October $20-off offer: [PREVIEW LINK]. If you like it, we could turn it into a real booking-ready website for your Etobicoke practice — would you like me to walk you through it?

Channel: Instagram Messages → author_id 17841425020460438.
