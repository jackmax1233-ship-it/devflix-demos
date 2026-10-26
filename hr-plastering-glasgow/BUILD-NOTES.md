# BUILD-NOTES — HR Plastering (Glasgow)
## Business
- Name: HR Plastering | Handle: @hrplastering2 | Author ID (instagram-cli): 17841459808318564
- Location: Glasgow and surrounding areas (IG bio) | Country: GB (profile country field)
- Followers: 164 | Posts: 99 (profile) | Industry: Plastering
- Gap evidence: IG profile website = null, bio_links = [] (instagram-cli profile, 26 Oct 2026). Bio gives only call/WhatsApp + email — no website, no booking page, nothing searchable to land on. Web search found no own site.
- Activity: latest verified post 6 Oct 2026 (instagram-cli post 17939246814369758, "Overboard of ceiling and bedroom skim" shortcode DeJZ-WJohmU) — within 30 days of 26 Oct 2026. Likes on sampled posts 5–13, 0 comments sampled — small but real, consistent with a 164-follower trade account; no bought-engagement signals claimed.
## Design
- Identity: warm plaster-white background, charcoal ink, dark ochre accent. Fonts: Fraunces (display) + Inter (body), Google Fonts display=swap.
- Layout: mobile-first; hero is text + full-view image (contain), never a cropped full-bleed photo. Services, recent-work gallery, dark contact band, footer.
## Contrast table (WCAG AA, computed)
| Pair | Ratio | Verdict |
|---|---|---|
| Ink #1E1B16 on bg #F7F3EB | 15.51:1 | PASS |
| White #FFFFFF on ink #1E1B16 | 17.16:1 | PASS |
| Ochre-dark #8A5A12 on bg #F7F3EB | 5.34:1 | PASS |
| White #FFFFFF on ochre #8A5A12 (buttons) | 5.91:1 | PASS |
## Image-fit audit
- All 6 photos are the business's own IG photos, 640x640 square. Hero max-height 540px, object-fit: contain; gallery max-height 340px, object-fit: contain. Full subject visible at all widths; nothing cropped. Width/height attributes set; gallery images lazy-loaded.
## Fact sources (business's own IG only)
- Bio: "Clean tidy professional service / Glasgow and surrounding areas / No job to small / Call or WhatsApp 07878052637 / hrplastering@mail.com" — phone + email shown on site because the business itself publishes them in its bio.
- Posts: https://www.instagram.com/p/DeJZ-WJohmU/ (ceiling overboard + bedroom skim, 6 Oct 2026); https://www.instagram.com/p/DeBss5CiPQB/ (ceiling/bedroom skim); https://www.instagram.com/p/DdvseQbiHzl/; https://www.instagram.com/p/Dc1E96LCAaR/ (small patch job after a leak); https://www.instagram.com/p/DapMZv_CLj1/ (kitchen revamp); https://www.instagram.com/p/DYXK47LCPrV/.
- NOT claimed: prices, hours, address, reviews, qualifications — none published by the business in bio/captions checked.
## Photo-harvest log (oEmbed, iPhone UA, 26 Oct 2026)
- All 6 shortcodes returned author_name = hrplastering2 (match). Thumbnails downloaded with browser Referer/UA, converted to WebP quality 78, 640px, separate files in images/ (no base64, no stock/AI).
## DM draft
Hi — I came across your Glasgow plastering work, especially that ceiling overboard and bedroom skim you posted recently. Right now someone searching for a plasterer in Glasgow only finds your Instagram, with no page showing your work and how to book. I built a quick concept site from your own photos so people can see the work and contact you in one place: https://jackmax1233-ship-it.github.io/devflix-demos/hr-plastering-glasgow/ — would it be useful to have something like that live for HR Plastering?
## Honest flags
- Engagement is modest (5–13 likes, few comments) — normal for a 164-follower trade account; not padded.
- Only 6 photos used; oEmbed gives the first frame/thumbnail for carousels, so gallery shows one frame per post.
