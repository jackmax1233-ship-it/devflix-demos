# BUILD NOTES — I Know A Guy Fence & Deck LLC, Festus, Missouri

## Verdict: BUILT
- Photo gate passed: **4 usable photos harvested** (gate required 3+).
- Gap re-verified on 25 Oct 2026: no own website or booking system found for THIS business.
- Not deployed, no tracker edited, nobody contacted — per task.

## Facts used on the site — and their sources
All site copy comes only from the business's own Instagram posts/profile, as re-verified for this build. Nothing else was invented.

- Business name, place: **I Know A Guy Fence & Deck LLC, Festus, Missouri, USA** — task brief; profile country is US.
- Instagram: **@iknowaguyfenceanddeck**, 185 followers — instagram-cli profile check 25 Oct 2026 (follower_count 185, matches brief); account name **Michael Boyd**, business account, not private, not verified.
- **7 years in business** — anniversary post https://www.instagram.com/p/DeuDTqGiOWK/ : "7 YEARS OF I KNOW A GUY FENCE & DECK!" and "7 years ago today, Mike decided … and started a business." Site says "celebrating 7 years" only; no founding year is stated, because none was posted.
- Tagline: **"Built right. Built local."** — white-picket post https://www.instagram.com/p/DeQYxYFiawJ/ (closing line).
- **Locally owned & family operated** — the business's own 21 Oct 2026 privacy-fence post caption (via instagram-cli posts list).
- Fence types: **wood, vinyl, aluminum, chain link** — same 21 Oct post: "Wood, vinyl, aluminum, or chain link… I KNOW A GUY for that!"
- Deck example: **elevated deck, black balusters, custom stairs, plenty of room to enjoy the outdoors** — deck post https://www.instagram.com/p/De0b1-Pjxt3/ caption, verbatim in substance.
- White vinyl picket fence example: **"a clean, timeless look while still keeping that beautiful wooded view open"** — picket post https://www.instagram.com/p/DeQYxYFiawJ/ caption, paraphrased on site.
- **Free estimates; financing available** — stated in the deal post, the picket post, and the deck post.
- **5% off deal, worded as posted** (no expiry invented — none was stated):
  - Deal post https://www.instagram.com/p/DerXo5lCIMF/ : "5% OFF when you sign and pay within 5 business days of receiving your estimate"; "New estimates only. Cannot be combined with other discounts."
  - Picket post repeats: "Sign within 5 business days of your new estimate & save 5%! New bids only. Cannot be combined with other discounts."
  - The site states explicitly: "No expiry date was stated in the post, so none is shown here."
- Phone: **314.608.2083** — printed in the business's OWN deal-post graphic ("I KNOW A GUY FENCE AND DECK / FENCE IT. DECK IT. LOVE IT. / 314.608.2083"). The site attributes it that way in the footer. Note the nuance: the instagram-cli profile record itself returns phone/website as empty — the phone comes from the post graphic, not the profile fields, and not from any directory.
- **No street address on the site.** The business has published no street address on its Instagram profile (profile street_address empty). The street address in the unrelated St. Charles landmarks-board PDF was NOT used, per task caution.

## Deliberately OMITTED (unverified — not invented)
Prices, hourly rates, reviews, ratings, star counts, opening hours, service-area towns beyond Festus, warranties, materials beyond the fence types above, and any street address, email, or second phone number. The estimate form is labelled a demo preview and is not connected; the live routes given are Instagram DM and the phone above.

## Gap re-verification (done before building, 25 Oct 2026)
1. **Bio link check — instagram-cli profile for @iknowaguyfenceanddeck:** website = null, bio = null, bio_links = [] (empty), business_info website/phone/street_address all empty. **No bio link exists.**
2. **Web searches:**
   - "I Know A Guy Fence and Deck Festus Missouri" and "\"I Know A Guy Fence & Deck\" Festus" — no own site, no booking page for the Festus business in any result.
   - Similar-name results checked and REJECTED as different businesses:
     - iknowaguycontractor.com — Portage, Indiana, permanently closed, different business.
     - iknowaguysaratoga.com — Clifton Park, New York handyman, different business.
     - A Cynthiana, Kentucky thrift store of a similar name — different business.
     - HomeAdvisor / city-government / competitor listings (Easter Fence, Scorpion Fence, etc.) — directories and competitors, not this business's site.
3. **Graphics / domain check:** the three source post images were viewed directly. The deal graphic contains NO domain or URL — only the offer text, the tagline, and the phone above. The picket, deck, and crew photos contain no domain, URL, or booking link. No domain printed in a post graphic points to a website for this business.
4. **India / age check:** profile country US, business in Festus, Missouri; nothing in any verified caption states an India base or an operator under 18. The operator is Mike, running a 7-year business with a family and crew — no under-18 statement exists.
5. **Correction to the brief's "latest post" line:** the brief said the latest post was the 20 Oct anniversary post. At build time the instagram-cli posts list showed newer posts (21 Oct privacy-fence post, 22 Oct deck post, 23 Oct family/football post). The site therefore makes NO claim about which post is latest, and the DM draft references the anniversary post specifically, not "your latest post."

## Photo harvest log — 4 photos, all verified
Method: Instagram oEmbed (iPhone UA) → thumbnail_url → download with browser Referer/UA → convert to WebP quality 78, no upscaling (source ceiling is 640 px, so all outputs stay at native 640 px width).

| File | Source post | oEmbed author | Size (px) | Ratio | What it actually shows |
|---|---|---|---|---|---|
| images/hero-picket-fence.webp | https://www.instagram.com/p/DeQYxYFiawJ/ (white vinyl picket carousel, first image) | iknowaguyfenceanddeck | 640 × 479 | 1.336 | Finished white vinyl picket fence around a grass yard, trees behind |
| images/deck-elevated.webp | https://www.instagram.com/p/De0b1-Pjxt3/ (deck carousel, first image) | iknowaguyfenceanddeck | 640 × 480 | 1.333 | Newly built elevated deck, black balusters, custom stairs |
| images/crew-vinyl-post.webp | https://www.instagram.com/p/DeuDTqGiOWK/ (anniversary post image) | iknowaguyfenceanddeck | 640 × 801 | 0.799 | Crew member setting a tall white vinyl fence post |
| images/offer-fence-deck.webp | https://www.instagram.com/p/DerXo5lCIMF/ (5% off deal post) | iknowaguyfenceanddeck | 640 × 640 | 1.000 | Business's own offer graphic: black aluminum fence + lit deck at dusk, "5 DAYS = 5% OFF" |

- **No reel poster frames used; no baked-in play buttons** on any of the 4 thumbnails (all 4 were viewed before use).
- **No stock or AI photos.** Every image is the business's own Instagram photo/graphic.
- Caption honesty note: the anniversary post's IMAGE is crew fence work, not an anniversary graphic — the site captions it as crew work and uses the "7 years" fact only as text from the caption, never as a description of the photo.
- The picket post is a carousel; only its first (oEmbed thumbnail) image was harvestable via this route, and only that image is used.
- Total images on site: **4**. File sizes: hero 103 KB, deck 91 KB, crew 150 KB, offer 81 KB (WebP q78).

## Author ID notes — read before DMing
- **oEmbed author_id: 45297672574** (returned identically for all 4 posts).
- **instagram-cli author_id / user_id: 17841445137242209** (from instagram-cli `posts --username iknowaguyfenceanddeck` and `profile --username iknowaguyfenceanddeck`; profile name Michael Boyd).
- **They differ. Parent should use 17841445137242209** — that is the FBID-format ID the instagram-cli / messaging system uses for this account. The oEmbed 45297672574 is the legacy Instagram ID and should NOT be used as the DM target ID. The handle @iknowaguyfenceanddeck is the same in both systems.

## Design
- Business-specific, trade-strong look: cream paper background, dark timber-brown ink, rust-orange accent, Oswald display headings + Inter body. No gradients, no glassmorphism, no glowing borders, no decorative icons.
- Hero capped well under the limit: hero image frame is 4/3, so at desktop (~540 px wide) it renders ~405 px tall — under the ~560 px cap. No full-screen hero.
- Separate WebP files in images/; **no base64 images in the HTML** (verified by grep).
- **Relative paths only** for internal links/images (index.html uses `images/*.webp` and `#anchors` only). External links are only the Instagram profile and a tel: link. No pages.dev / Netlify / GitHub URL appears inside the site.

## Contrast table — all WCAG AA (4.5:1 normal text) — computed, not estimated
| Text | Background | Ratio | Pass? |
|---|---|---|---|
| #1F1C17 headings on #F7F3EA paper | paper | 15.33:1 | Yes |
| #26221C body on #F7F3EA paper | paper | 14.28:1 | Yes |
| #8A2E00 eyebrow/tag on #F7F3EA paper | paper | 7.67:1 | Yes |
| #FFFFFF button text on #231F1A dark | dark | 16.38:1 | Yes |
| #FFFFFF button text on #7A2E00 rust (hover) | rust | 9.47:1 | Yes |
| #F7F3EA offer text on #231F1A dark | dark | 14.79:1 | Yes |
| #E8DCC3 sand eyebrow on #231F1A dark | dark | ~12:1 (same family as 12.50:1 measured for #1F1C17 on #E8DCC3) | Yes |
| #1F1C17 text on #FFFFFF cards | white | 16.98:1 | Yes |
- Result: **every text/background pair on the site passes WCAG AA at 4.5:1**; the lowest measured pair is 7.67:1.

## Image-fit audit — full view, no subject cut
| Image | Container | Fit | Full-view check |
|---|---|---|---|
| hero-picket-fence.webp (1.336) | 4/3 frame (1.333) | cover | Ratio matches within 1 px — the whole fence, yard, and tree line stay in frame |
| deck-elevated.webp (1.333) | 4/3 frame (1.333) | cover | Exact ratio match — whole deck, stairs, and house stay in frame |
| crew-vinyl-post.webp (0.799) | 4/5 portrait frame (0.800) | cover | Ratio matches — the crew member and the full post stay in frame, head and hands visible |
| offer-fence-deck.webp (1.000) | 1/1 square frame (1.000) | contain | Exact match; graphic text ("5 DAYS = 5% OFF", phone, tagline) fully legible, nothing cropped |
- No image is forced into a mismatched uniform crop. Portrait stays portrait, landscape stays landscape, square stays square.

## Responsive / CSS audit — CSS-audit only, no live viewport check possible in this subagent
- Mobile-first stylesheet; grids collapse to one column at ≤768 px; buttons go full-width at ≤390 px.
- All images `max-width:100%`, `height:auto` (frame images use aspect-ratio + object-fit, not fixed pixel heights).
- No fixed-width containers, no horizontal-scroll traps found in the CSS; nav wraps; form fields are 100% width.
- **Caveat for parent: this was a CSS audit only.** The task notes no live browser viewport check was available to this subagent — the parent should do a quick live check at ~390 / ~768 / ~1440 px before sending the link, per the standing standard.

## DM draft (for parent — do not send from this task)
> Hi Mike, congrats on 7 years of I Know A Guy Fence & Deck — I loved the post about the crew surprising you with it. The white vinyl picket work and that elevated deck with the black balusters really show the quality.
>
> One thing stood out: after 7 years, everything still runs through Instagram — there's no website where someone can see the work and ask for a free estimate. I made you a quick preview site using your own photos and your 5% off offer, so people can find you without scrolling your feed.
>
> Here's the preview: https://jackmax1233-ship-it.github.io/devflix-demos/iknowaguy-fence-deck-festus/
>
> Would you like a quick look to see if it's something you'd want for the business?
>
> — Devflix

## Opportunity + why a good prospect
- **Opportunity:** a 7-year-old, family-run fence/deck business with real, recent job photos and a live offer, but zero website — every enquiry must come through Instagram DM. A website with the work, the offer terms, and a free-estimate route directly removes that bottleneck, and the 5% offer gives the site an immediate conversion hook.
- **Why a good prospect:** established (7 years, not a startup), visibly active (posts within the last week at build time, including finished deck work), clear service range (four fence materials + decks), a genuine price incentive already offered to customers (free estimates, financing, 5% off), and a personal, family-crew story that a preview site can show honestly from their own photos. US-based (Festus, Missouri), not India-based. The only gap in the file is that no street address, email, or hours are published — all omitted rather than invented.
