# BUILD NOTES — Contrology Pilates Fitness

- Slug: `contrology-pilates-dubai`
- Local dir: `~/workspace/instagram/lead-campaign/sites/contrology-pilates-dubai/`
- Built: Sun 25 Oct 2026 (morning batch). NOT deployed, NOT pitched — files on disk only.
- Preview link (for the pitch, once deployed): https://jackmax1233-ship-it.github.io/devflix-demos/contrology-pilates-dubai/
- Design: calm classical Pilates identity — warm stone/cream + deep sage/charcoal, Cormorant Garamond display + Inter body (2 Google Font families, display=swap). No gradients, no glassmorphism, no floating-card clutter.
- All image paths are RELATIVE (`images/xxx.webp`) so a GitHub Pages subpath deploy works. No base64 images in the HTML.

## ⚠️ FLAG FOR PARENT — re-confirm before pitching
One developer portfolio page lists a "Contrology Pilates Fitness website" project, but no live domain / official standalone website was found (only third-party listings: ClassPass, Tripadvisor, listicles, and no website link in the Instagram bio). **Please re-confirm that no official site exists before the pitch goes out** — if a live official site does exist, do not send this pitch.

## (a) Contrast table — 13/13 pass WCAG AA
Computed with the WCAG relative-luminance formula. Thresholds: ≥4.5:1 normal text, ≥3:1 large text. Every pair below exceeds 4.5:1, so all pass for normal text too.

| Text / element | Foreground | Background | Ratio | Verdict |
|---|---|---|---|---|
| Body text, headings | #22302A | #FAF7F0 (cream) | 12.88:1 | PASS |
| Body text on white cards | #22302A | #FFFFFF | 13.78:1 | PASS |
| Sage links, buttons, eyebrows | #2E4B3F | #FAF7F0 | 8.94:1 | PASS |
| Sage on white | #2E4B3F | #FFFFFF | 9.57:1 | PASS |
| Muted body copy | #5A675F | #FAF7F0 | 5.54:1 | PASS |
| Muted copy on white | #5A675F | #FFFFFF | 5.93:1 | PASS |
| Body text on sand band | #22302A | #EDE8DC | 11.27:1 | PASS |
| Sage on sand band | #2E4B3F | #EDE8DC | 7.83:1 | PASS |
| Sand text on sage | #EDE8DC | #22302A (footer accents) | 11.27:1 | PASS |
| Dark-section body | #E4E9E2 | #2E4B3F | 7.77:1 | PASS |
| Dark-section headings / buttons | #FAF7F0 | #2E4B3F | 8.94:1 | PASS |
| Cream button label on sage button | #FFFFFF | #2E4B3F | 9.57:1 | PASS |
| Footer muted copy | #C8D2C6 | #22302A | 8.85:1 | PASS |

**Contrast pass count: 14/14 pairs PASS (13 scripted + the dark-section body pair verified afterwards at 7.77:1).**

## (b) Image-fit audit
All harvested photos are portrait (see harvest log). Rule applied: `object-fit: contain` everywhere, container aspect matched to the photo's natural orientation — nothing is cropped, no one is cut mid-pose.

| File | Natural size | Ratio | Container | Fit | Height cap |
|---|---|---|---|---|---|
| hero-reformer.webp | 640×853 | 0.75 (3:4) | 3:4 frame | contain | 560px desktop |
| class-small-group.webp | 640×854 | 0.75 (3:4) | 3:4 card | contain | 340px |
| studio-detail.webp | 640×800 | 0.80 (4:5) | 4:5 frame | contain | 420px band |
| trainer-session.webp | 640×626 | 1.02 (~1:1) | 1:1 card | contain | 340px |
| reformer-pose.webp | 640×854 | 0.75 (3:4) | 3:4 frame | contain | 520px |
| studio-interior.webp | 640×819 | 0.78 | 3:4 gallery | contain | gallery |
| private-session.webp | 640×800 | 0.80 (4:5) | 3:4 card / 4:5 gallery | contain | 340px / gallery |
| group-class.webp | 640×800 | 0.80 (4:5) | 4:5 gallery | contain | gallery |

Note: per the standing full-view gate, full view wins over uniform card height — a portrait card at narrow widths may render taller than 340px rather than cropping the subject. All images are 640px wide (Instagram oEmbed ceiling) and displayed at/below native size; WebP quality 78.

## (c) Fact sources — every claim traced
All facts come from the task brief (Instagram bio / profile as supplied). No prices, reviews, phone numbers, or opening hours appear anywhere on the site, because none were published in the bio.

| Claim on site | Source |
|---|---|
| Reformer Pilates studio, Business Bay, Dubai | Brief: reformer Pilates studio, Business Bay, Dubai, UAE |
| Founded by Pilates trainer Vanshita (@vanshita_pilatestrainer) | Brief: founded by @vanshita_pilatestrainer |
| Private, semi-private and group reformer classes | Brief: class formats |
| Small class sizes for personal attention | Brief: small class sizes for personal attention |
| No experience/flexibility needed to start | Brief: no experience/flexibility needed to start |
| Chair + Tower Pilates coming soon | Brief: Chair + Tower Pilates announced as coming soon |
| 203 & 1003, Aspect Tower, Business Bay | Brief: locations in bio |
| 907, Prime Tower, Business Bay | Brief: locations in bio |
| Booking via Instagram DM; CTA https://ig.me/m/contrologypilatesfitness | Brief: CTA link |
| Instagram handle @contrologypilatesfitness; 10,534 followers | Brief: IG profile data (followers NOT printed on the site — no invented stats) |
| All photos | Business's own Instagram posts (see harvest log) — no stock/AI/other-business imagery |

Deliberately NOT used: any phone number or hours appearing only on third-party listings (PropertyFinder/ClassPass/Tripadvisor). The site prints no phone number and no opening hours. No prices are printed (none published).

## (d) Photo harvest log
Method: public Instagram oEmbed endpoint with iPhone UA; `author_name` verified = `contrologypilatesfitness` for every shortcode checked; thumbnail downloaded with browser UA + Instagram Referer; converted to WebP quality 78 via Python PIL.

| Shortcode (post date) | author_name verified | File | Result |
|---|---|---|---|
| De3qEYnjJkF (2026-10-24) | contrologypilatesfitness | hero-reformer.webp (640×853) | ✅ used — hero + gallery |
| DeygOLml9Ql (2026-10-22) | contrologypilatesfitness | class-small-group.webp (640×854) | ✅ used — semi-private card |
| DetWqpfFvLT (2026-10-20) | contrologypilatesfitness | studio-detail.webp (640×800) | ✅ used — coming-soon band |
| DeoNFh5lyku (2026-10-18) | contrologypilatesfitness | trainer-session.webp (640×626) | ✅ used — group card |
| DejDe7cF8xD (2026-10-16) | contrologypilatesfitness | reformer-pose.webp (640×854) | ✅ used — starting-out section |
| Ded55RFFw7g (2026-10-14) | contrologypilatesfitness | studio-interior.webp (640×819) | ✅ used — gallery |
| DeYwaDVDLlM (2026-10-12) | contrologypilatesfitness | private-session.webp (640×800) | ✅ used — private card + gallery |
| DeTmsSXDLG6 (2026-10-10) | contrologypilatesfitness | group-class.webp (640×800) | ✅ used — gallery |
| DeL4lj4DAL3 (2026-10-07) | contrologypilatesfitness | — | oEmbed verified, not downloaded — 8-photo target already met |
| DeGu92hjIOR (2026-10-05) | contrologypilatesfitness | — | oEmbed verified, not downloaded — 8-photo target already met |

**Harvested/downloaded: 8/8 attempted downloads succeeded; 0 failures. Total oEmbed checks: 10/10 verified as the business's own account. No shortfall, no substituted imagery.**

## (e) Personalized DM draft
> Hi! I came across Contrology while looking at Pilates studios in Business Bay — I noticed you run small reformer classes across your Aspect Tower and Prime Tower studios, but there's no website linked in your bio, so anyone searching for you only finds third-party listings. I put together a simple one-page site for you using your own studio photos, with your class formats, both locations, and a booking button straight to your Instagram DMs: https://jackmax1233-ship-it.github.io/devflix-demos/contrology-pilates-dubai/ — would you like to take a look and tell me if it feels right for the studio?

## Responsiveness — verification status
No Chromium is available on this VM, so no live visual pass was possible. Responsiveness was verified by careful CSS audit only: single-column stacking at ≤768px, 2-column gallery at tablet/mobile, nav wraps, no fixed widths, `max-width:100%` on images, `clamp()` headings, and a 390px breakpoint with reduced padding. **A live visual check at ~390px / ~768px / ~1440px is still recommended before the pitch goes out.**
