# BUILD NOTES — Wardh Henna (wardh-henna-qatar)

## Business (all facts from the business's own Instagram)
- Business: Qatar Henna Artist / Wardh Henna — @wardh_al_henna, Qatar.
- Followers: 26,784 (verified via instagram-cli profile, 26 Oct 2026). 667 posts.
- Positioning (bio): "Qatar Henna artist — Selling Fresh Organic henna cones, Nail cones, Hair henna — Book your henna appointment".
- Gap evidence: NO website. Bio links = WhatsApp group + Facebook only. Bookings via WhatsApp/DM; no searchable site to land on.
- Latest post checked: 2026-10-14 (appointment post) — 12 days before this batch.

## Design
- Identity: henna warmth. Deep henna brown #3D1F0E + cream #FBF3E4 + dark gold-brown #6B4A1F.
- Fonts (2, Google Fonts, display=swap): Cormorant Garamond (display serif) + Karla (body).
- Layout: split hero, services cards, cones section, square photo gallery, dark home-service band, booking section. No gradients, no glassmorphism, no floating cards.
- No prices on the site: the business publishes no prices in the checked posts/captions.

## Contrast table (WCAG AA, computed)
| Pair | Ratio | Pass |
|---|---|---|
| White on #3D1F0E (buttons, dark band) | 14.99:1 | AA normal |
| #3D1F0E on #FBF3E4 (body/headings) | 13.59:1 | AA normal |
| #6B4A1F on #FBF3E4 (eyebrow accent) | 7.26:1 | AA normal |
| #5A4A3A on #FBF3E4 (captions/footer) | 7.69:1 | AA normal |
| #E8E0D2 on #3D1F0E (dark-band muted text) | 11.44:1 | AA normal |

## Image-fit audit (FULL VIEW gate)
- All 6 photos are the business's own Instagram photos, harvested via public oEmbed (640px ceiling).
- Natural size: 640×640 (square), hero 640×655. Containers use aspect-ratio 1/1 with object-fit: contain — nothing cropped, hands/designs fully visible.
- Hero max height 540px (under the 560px cap). Gallery frames max 340px tall.
- Files are separate WebP (quality 78) in images/. No base64. No stock/AI imagery.
- The artist's henna designs are the product: square frames were chosen specifically so no hand or design edge is cut.

## Fact sources (post links / IDs)
- Profile: @wardh_al_henna, user_id 17841410042881384, country QA, bio as above, bio_links = WhatsApp + Facebook, business website = none.
- https://www.instagram.com/p/DefLkuANAvp/ — 2026-10-14, 34 likes, 1 comment, appointment/home-service post.
- https://www.instagram.com/p/DdyZwL3sqET/ — 2026-09-27, "Simple wedding henna", home service available.
- https://www.instagram.com/p/Db1NDDkjLPO/ — "Bride Habiba", 172 likes.
- Gallery posts: DcIP2GUMhji, DbSwBmVDHXw ("henna step by step"), DbOjJe6sz7F — all author-verified via oEmbed author_name = wardh_al_henna.

## Photo-harvest log
- Method: curl iPhone UA to oEmbed; author_name checked = wardh_al_henna for every image used; CDN thumbnail downloaded with browser Referer + iPhone UA; converted to WebP q78 with PIL (native 640px, no upscaling).

## DM draft
> Hi — I came across your recent henna work in Qatar, including the simple wedding henna and bridal designs, and noticed bookings run through WhatsApp with no website to show the work on. I made you a preview site with your services, home-service offer and recent designs in one place: https://jackmax1233-ship-it.github.io/devflix-demos/wardh-henna-qatar/ — would a page like that help brides and event clients book with you?

## Honest flags
- Largest account in this slice (26,784 followers); photo-post likes are modest (21–440) relative to follower count, but comments are real and posting is consistent (Oct 14 latest). Not presented as a small account.
- No specific Qatari city is claimed (bio says Qatar only); no phone number is printed (booking goes via the WhatsApp link in bio, as the business routes it).
- The business also sells cones in Kerala per its bio line — noted here only; the site claims Qatar only, per bio location and country QA. This is NOT an India-based business (base, posts and account country are Qatar).
- Responsive audit is CSS-based (mobile-first, stacks at 768px/480px). A live visual pass at 390/768/1440px is still needed before sending — this subagent has no live browser.
