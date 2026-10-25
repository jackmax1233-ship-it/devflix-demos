# BUILD NOTES — Isai's Gutter Cleaning Service (Concord / Bay Area, CA)

Built: 25 Oct 2026 (PKT). One preview site only. No contact made, nothing deployed, no tracker edited.

## 1. Facts used (only what the business itself published)

- Business: Isai's Gutter Cleaning Service — Instagram @isaiguttercleaning
- Location: Concord / Bay Area, California, USA (bio: "Bay Area Gutter Service"; post caption: "Serving Concord and surrounding areas"; reel caption hashtags include #ConcordCA, #BayArea)
- Bio (via instagram-cli profile, 25 Oct 2026): "Bay Area Gutter Service / Cleaning / DM: Get a Quote! / Quality • Reliable • Professional"
- Services (bio + captions): gutter cleaning, gutter deep cleaning, gutter guard installation. Flow-check wording ("flowing properly", "proper water flow", "water draining fluidly") comes from their own post captions.
- Why-cleaning points (their own flyer wording): removes leaves, dirt & debris; prevents clogs & water damage; protects roof & foundation; "Fast, reliable & affordable" is their reel-caption wording.
- Contact published by them: call or text **925-771-4295** for a **FREE estimate** (latest post caption, 20 Oct 2026, and printed on their own flyer graphic). No email, street address, hours, or prices were published by them, so none appear on the site.
- Followers: 239 (instagram-cli profile, 25 Oct 2026); 16 posts. Latest post 20 Oct 2026 (18 likes on that post per instagram-cli).
- NOT invented: no reviews, ratings, testimonials, prices, hours, address, licences, or service towns beyond "Concord and surrounding areas / Bay Area". The quote section deliberately lists no prices and says every home is different — because the business itself quotes per job ("DM: Get a Quote!", "FREE estimate").

## 2. Gap re-verification (done before building — gap CONFIRMED, build proceeded)

1. **Bio link check (instagram-cli profile, 25 Oct 2026):** the profile's only bio link is a TikTok profile URL (`tiktok.com/@isaiguttercleanin…`). The profile's business-info website field is empty. A TikTok profile is a social profile, not a website, quote form, or booking system. No website, no quote form, no service-area page exists for this business.
2. **Web searches, 25 Oct 2026:** "Isai's Gutter Cleaning Concord Bay Area" and "isaiguttercleaning Concord gutter" returned no website for this business — only unrelated companies (BBB category listings for other Bay Area gutter firms, and Concord gutter firms in Georgia, New Hampshire, North Carolina, and Massachusetts). None is Isai's.
3. **Graphics / domain check:** all 8 harvested thumbnails were inspected visually. The flyer graphic (post DevIriFibY9) prints only the phone number 925-771-4295 — no domain, no URL, no QR-style web address. The job photos print no domain. The two reel poster frames carry only on-screen text ("POV: View", "Spring is here!") — no domain. No hidden website was found in any graphic.
4. **Location / age check:** NOT India-based — US business (instagram-cli country: US; Concord, California; 925 California area code). No statement anywhere puts the operator under 18, and nothing in the profile suggests a minor-run account; it is a business account advertising a trade service. (This is an absence of any under-18 indication, not a verified date of birth — no DOB is published.)

Conclusion: the gap is real. The business takes quotes only by Instagram DM / call / text, with no website of its own.

## 3. Contrast table (WCAG AA, normal text needs 4.5:1 — all PASS)

| Text | On background | Ratio | Where used | Result |
|---|---|---|---|---|
| #1E1E1E | #F7F3EB | 15.06:1 | Body text, headings, nav | PASS |
| #1E1E1E | #FFFFFF | 16.67:1 | Service cards | PASS |
| #FFFFFF | #1E1E1E | 16.67:1 | Dark buttons, strip | PASS |
| #FFFFFF | #9E1B1B | 8.00:1 | Red CTA button, quote headings | PASS |
| #F7F3EB | #9E1B1B | 7.22:1 | Quote section body on red | PASS |
| #FFE9E9 | #9E1B1B | 6.89:1 | Quote-section note on red | PASS |
| #F7F3EB | #1A2119 | 14.88:1 | Top bar, dark section headings | PASS |
| #D8D2C2 | #1A2119 | 10.91:1 | Dark-section body text | PASS |
| #5A5348 | #F7F3EB | 6.86:1 | Secondary/intro text | PASS |
| #FFFFFF | #1A2119 | 16.46:1 | Footer text | PASS |
| #1E1E1E | #EDE6D6 | 13.41:1 | Gallery captions area | PASS |

No purple/blue gradients, no glassmorphism, no glowing borders, no decorative icons. Palette is drawn from the business's own flyer (black / red / white) plus warm paper tones.

## 4. Image-fit audit (FULL-VIEW rule)

- All source photos are portrait: job photos 640×853 (3:4), flyer 640×800 (4:5), reel frame 640×1136 (9:16).
- Hero: flyer shown with `object-fit: contain`, max-height 520px on desktop (under the ~560px cap), so the whole flyer — headline, phone number, footer strip — is visible, never cropped.
- Gallery: each card's aspect ratio matches its photo's natural orientation (3:4 for job photos, 9:16 for the reel frame) and images use `object-fit: contain` on a neutral background, so no gutter, roofline, or worker is cut.
- No `object-fit: cover` anywhere on the site. No stock or AI imagery. No image is stretched or distorted.
- Responsive: mobile-first CSS; single column stacks to 2-column gallery at small widths, 3-column at ≥768px, hero grid at ≥768px. **Verification was CSS-audit only** — no live viewport check at 390/768/1440px was possible from this subagent (no live browser access). Parent should spot-check the deployed preview at those widths before sending, per the standing image-fit/responsive gate.

## 5. Photo harvest log (oEmbed route, iPhone UA)

All 8 posts returned `author_name: isaiguttercleaning` (verified match) and oEmbed `author_id: 75886059426`. Thumbnails downloaded with browser Referer + iPhone UA (640px ceiling, as documented).

| Post | Type | Used as | Notes |
|---|---|---|---|
| DevIriFibY9 | image (flyer graphic) | images/flyer-hero.webp (640×800) | Business's own promo flyer; prints phone + "FREE estimate". Not a job photo — used as hero brand art, full-view. |
| DM8M2FZJ9CR | image | images/work-roof-gutter.webp (640×853) | Roof gutter full of leaves/debris. |
| DM0hG13p1iL | image | images/work-leaf-gutter.webp (640×853) | Gutter packed with dry leaves. |
| DMTbLGyh7Dm | image | images/work-tile-roof.webp (640×853) | Debris along tiled roof/gutter line. |
| DL_F3njSktR | image | images/work-cleaned-gutter.webp (640×853) | Cleaned gutter, water draining. |
| DL0fK6EhKM2 | image | images/work-deep-clean.webp (640×853) | Deep-clean job above a deck. |
| DVxpYXSAgAt | reel poster frame | images/work-reel-gutter-pov.webp (640×1136) | First-person gutter-cleaning frame. **Disclosure: this is a reel poster frame, not a standalone photo.** It carries baked-in on-screen text ("Spring is here!") and a black letterbox bar at the bottom from the reel frame. **No play button is baked into this thumbnail.** Captioned on-site as a still from a reel. |
| DV6nkFGDybz | reel poster frame | NOT USED | Scenic Bay Area hillside view ("POV: View" text, black bars top/bottom). Harvested successfully but excluded: it shows no gutter work, so it would not help sell the service. No play button baked in. |

Result: 7 images on the site (1 flyer + 5 job photos + 1 reel frame) — above the 4-photo minimum, so no shortfall. All converted to WebP quality 78 at native 640px width (source ceiling; no upscaling). Total site ~700 KB.

## 6. What was NOT done

- No DM, email, or message sent. No deployment (parent deploys via the GitHub Pages route). No tracker edited. No prices, reviews, hours, addresses, or extra towns invented. The quote section is call/text/DM only — no fake working form, since the business has no booking backend.

## 7. DM draft (for the parent to send — short, natural, personalized)

> Hi Isai! I came across your page and the Concord gutter jobs you've been posting — the ones where the gutters are packed with leaves and then draining properly after. Really clear before-and-after work.
>
> I noticed you don't have a website yet, so right now anyone who finds you has to DM for a quote — I put together a simple preview site for you using your own photos, with your services, your Concord/Bay Area coverage, and a free-estimate section pointing to your number (925-771-4295).
>
> Here's a look: https://jackmax1233-ship-it.github.io/devflix-demos/isai-gutter-cleaning-concord/
>
> Would you like a proper website like this for your business?
>
> — Devflix

## 8. Opportunity + why a good prospect

- Opportunity: a real, working trade business whose only online presence is Instagram + TikTok, taking quotes by DM. A website with services, real job photos, a service-area page, and a free-estimate call-to-action directly fixes the gap: homeowners searching "gutter cleaning Concord" currently cannot find or vet this business at all.
- Why a good prospect: genuine, evidenced need (no site, DM-only quoting); credible trade with visible completed work (flow-checked jobs, gutter guard installation — not just promises); small but real audience (239 followers, steady posting through 20 Oct 2026); Bay Area homeowner market where a single cleaning job justifies a site; and the preview is built entirely from their own photos and words, so the pitch is honest, not generic.

## 9. Author ID notes (for the DM)

- oEmbed `author_id`: **75886059426** (the media-owner ID returned by Instagram's oEmbed endpoint for all 8 posts).
- instagram-cli profile `user_id`: **17841475942785757** (the profile record returned by the connected account's own tooling).
- They differ because the two systems use different ID namespaces for the same @isaiguttercleaning account.
- **Parent should use the instagram-cli user_id 17841475942785757** (with username @isaiguttercleaning) when addressing/targeting the DM — it is the ID from the account's own profile record. Do NOT use the oEmbed author_id 75886059426 for DM targeting.
