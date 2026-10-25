# BUILD NOTES — Rapid Fighter Self Defense Academy (rapid-fighter-sharjah)

Built: Sun 25 Oct 2026, Devflix outreach morning batch. NOT deployed, NOT sent, tracker NOT edited — files on disk only.
Local dir: `~/workspace/instagram/lead-campaign/sites/rapid-fighter-sharjah/`
Intended preview link (for the DM draft only, not yet live): https://jackmax1233-ship-it.github.io/devflix-demos/rapid-fighter-sharjah/

## Design
Dark charcoal + bold red + gold accent; Oswald (condensed display) + Inter (body) via Google Fonts, display=swap. No gradients, no glassmorphism, no floating cards. All paths relative (`images/xxx.webp`) so a GitHub Pages subpath deploy works.

## (a) Contrast table (computed, WCAG AA: ≥4.5:1 normal, ≥3:1 large)

| Foreground | Background | Ratio | Passes |
|---|---|---|---|
| #FFFFFF | #141414 (header, hero, dark sections) | 18.42:1 | AA normal ✓ |
| #141414 | #F5F1E8 (page background) | 16.34:1 | AA normal ✓ |
| #141414 | #FFFFFF (discipline cards) | 18.42:1 | AA normal ✓ |
| #E8E8E8 (body text) | #141414 | 15.04:1 | AA normal ✓ |
| #D9D9D9 (captions/footer) | #141414 | 13.05:1 | AA normal ✓ |
| #FFFFFF (button label) | #C8102E (red button / visit band) | 5.88:1 | AA normal ✓ |
| #FFFFFF (button label, hover) | #A8121F | 7.58:1 | AA normal ✓ |
| #141414 (light button label) | #FFFFFF | 18.42:1 | AA normal ✓ |
| #FFC94D (eyebrow, step numbers, gold headings) | #141414 | 12.03:1 | AA normal ✓ (also large text) |
| #C8102E (red rule/border only) | #F5F1E8 / #141414 | decorative only, no text | n/a |

Contrast pass: 10/10 text combinations pass AA. Red (#C8102E) is never used for small body text — only buttons (white text on red), rules and borders.

## (b) Image-fit audit (full-view gate)

Images are shown at their natural aspect ratio with `width:100%; height:auto` — no cropping, no `object-fit: cover` anywhere, so nobody is cut mid-action.

| File | Natural size | Aspect | Placement | Max displayed height |
|---|---|---|---|---|
| hero-class.webp | 640×480 | 4:3 landscape | Hero, right column (~490px wide desktop) | ~368px desktop, ~263px at 390px wide — under 560px cap ✓ |
| class-2.webp | 640×640 | 1:1 square | Gallery | ~340px at 3-col desktop ✓ |
| class-3.webp | 640×640 | 1:1 square | Gallery | ~340px ✓ |
| class-4.webp | 640×500 | 1.28:1 landscape | Gallery | ~265px ✓ |
| class-5.webp | 640×480 | 4:3 landscape | Gallery | ~255px ✓ |
| class-6.webp | 640×712 | ~0.90:1 portrait | Gallery (portrait frame matches its own ratio) | ~380px at gallery column width; full poster visible, not cropped ✓ |

All `width`/`height` attributes match the real files. Hero image is reused once in the gallery so all 6 harvested files appear; no other imagery is used.

## (c) Fact sources — every claim traced

| Claim on site | Source |
|---|---|
| Business name, Muwaileh, Sharjah, UAE | Task brief / Instagram profile context |
| Okinawa Shorin Ryu Karate Do; karate, kickboxing, Muay Thai, Zumba, personal training | Task brief (published facts) |
| Phone +971 50 927 7897 (shown + tel:+971509277897) | Business's own published bio number — brief explicitly allows showing it |
| Address: kay4 building, shop no. 2, Muwaileh, Sharjah | Business's own published bio address |
| CTA: Instagram DM via https://ig.me/m/rapidfighterselfdefenseacademy | Brief |
| Classes for children and adults | EVIDENCED BY PHOTOS, not invented: class-2/class-3/class-5 show young students; hero-class/class-4 show adult students. Site copy says only this, no age splits. |
| "Enrolment is by phone or Instagram message, as the academy currently offers" / "no online booking on this preview" | Brief's gap statement (no website found; enrolment evidently via phone/DM) |
| Gallery captions ("students with certificates", etc.) | Direct description of what each harvested photo shows |
| NOT claimed anywhere | No prices, no class times, no age-group splits, no reviews, no trial/free-class offer, no federation/approval claims. (Wall text visible inside the photos — e.g. association names — was deliberately NOT copied into site copy, since it was not in the brief's fact list.) |

## (d) Photo harvest log — 6/6 harvested, 0 failed

Method: public Instagram oEmbed endpoint with iPhone UA; `author_name` verified = `rapidfighterselfdefenseacademy` for every post before download; downloaded with browser UA + Instagram Referer; converted to WebP quality 78 via Python PIL.

| Shortcode (post date per brief) | author_name verified | File | Size |
|---|---|---|---|
| De1f9VoREqy (2026-10-23) | rapidfighterselfdefenseacademy ✓ | images/hero-class.webp | 640×480, 63 KB |
| Dei6GyQx8NF (2026-10-15) | rapidfighterselfdefenseacademy ✓ | images/class-2.webp | 640×640, 64 KB |
| DeGuVrTxx6z (2026-10-05) | rapidfighterselfdefenseacademy ✓ | images/class-3.webp | 640×640, 57 KB |
| Dd50C0uxNVS (2026-09-30) | rapidfighterselfdefenseacademy ✓ | images/class-4.webp | 640×500, 52 KB |
| DdDvDayRJVX (2026-09-09) | rapidfighterselfdefenseacademy ✓ | images/class-5.webp | 640×480, 53 KB |
| DcdLN28xe9z (2026-08-25) | rapidfighterselfdefenseacademy ✓ | images/class-6.webp | 640×712, 64 KB |

No shortfalls in harvest. No stock, AI or other-business imagery used. Note: class-6 is the academy's own promotional poster graphic (child in gi with "Focus / Discipline / Champion" text), not a plain class photo — shown as-is, captioned accordingly.

## Responsive audit (CSS audit only — no Chromium on this VM)
- Breakpoints: 768px (hero stacks, grids 2-col, steps/who stack) and 480px (all grids 1-col, smaller headings).
- No fixed widths, no horizontal overflow sources (all grids use `1fr`, images `max-width` via `width:100%`, nav wraps).
- Live visual pass at 390/768/1440px is still recommended before the link is sent.

## (e) DM draft (personalised, for the parent to send — NOT sent by this build)

> Hi! I came across Rapid Fighter Self Defense Academy in Muwaileh — your class photos really show the range you teach, from karate for the younger students to kickboxing and Muay Thai for adults. I noticed you don't have a website yet, so anyone searching in Sharjah only finds your Instagram and has to call or DM to ask about classes. I made you a simple one-page preview using your own photos — your disciplines, how to join, and your number and address in one place: https://jackmax1233-ship-it.github.io/devflix-demos/rapid-fighter-sharjah/ — would you like me to set it up properly for the academy, or change anything on it?
