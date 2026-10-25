# MyBrow247 — Fairfax, VA — preview site build notes

## Business (verified facts only)
- MyBrow247, microblading / permanent makeup studio, Fairfax, Virginia, USA (NOT India-based).
- Instagram: @mybrow247, public business account, name "Mybrow247".
- Address from Instagram business info: 3615 Chain Bridge Rd, Suite H, Fairfax, VA. ZIP CONFLICT — see caveat below; the site therefore prints no ZIP code.
- Phone from Instagram bio: 301.233.7513. KakaoTalk from bio: mook1525.
- Bio (English line, verbatim in substance): "Virginia licensed permanent makeup tattoo".
- Booking route evidenced by the business's own bio + client review history: phone/text, no booking widget on Instagram.
- Operator age: no statement anywhere that the operator is under 18; the studio is a Virginia-licensed business. No client who looks under 18 was used.
- Follower count VERIFIED by me via instagram-cli profile on 25 Oct 2026: **1,171 followers** (following 4,297; 1,787 posts). Do not use any other number.

## Gate checks (all passed, in order)
1. **RECENCY — PASS.** Live feed via instagram-cli (25 Oct 2026) shows 7 posts dated 21 Oct 2026, all on/after 25 Sep 2026:
   - 2026-10-21 06:31 https://www.instagram.com/p/DewhT44xsnQ/
   - 2026-10-21 06:27 https://www.instagram.com/p/Dewg0GARaIm/
   - 2026-10-21 06:23 https://www.instagram.com/p/DewgcIIEYGE/ (carousel)
   - 2026-10-21 06:16 https://www.instagram.com/p/Dewfi9Cx_KS/
   - 2026-10-21 06:11 https://www.instagram.com/p/DewfBG9xI2h/
   - 2026-10-21 06:10 https://www.instagram.com/p/Dewe41WxIN_/
   - 2026-10-21 06:09 https://www.instagram.com/p/DewexIBxZFp/
2. **BIO LINK — PASS.** instagram-cli profile, 25 Oct 2026: `bio_links: []`, `website: null`, business-info `website: null`. Bio contains only the phone number and KakaoTalk ID. No website, booking widget, or booking system is linked from the bio.
3. **FEED SAFETY (PMU gate) — PASS.** I viewed all 7 harvested 21 Oct 2026 images. Every subject is an adult PMU client (close-up brow work; several visibly mature clients, including grey-haired clients). No client looks under 18, and the feed is not dominated by apparent minors. No copy is built around any young-looking client. Note: several source photos pixelate the lower face; that pixelation is in the studio's own photos and is preserved.
4. **PHOTOS — PASS.** 7 usable photos harvested (need was ≥4), all image posts from 21 Oct 2026, all via the oEmbed route below. No reels, so no baked-in play buttons. No stock/AI photos used.
5. **WEB SEARCH — PASS WITH A FLAG (read carefully).** Searched "MyBrow247 Fairfax microblading website" myself on 25 Oct 2026. Results were Yelp, BestProsInTown, and unrelated businesses — no live website or booking system for this business. ONE FLAG: a place-info aggregator result listed "Website: http://www.mybrow247.net/". I inspected that domain: a fetch of http://www.mybrow247.net/ returned HTTP 404 (no site content), and a second search for "mybrow247.net" returned no site content at all — only directory listings. Instagram's own website field is empty. Conclusion: there is no functioning website/booking system for this business that a client could use, so the build proceeded — but the DM draft below deliberately does NOT claim "you have no website"; it says everything runs through Instagram, which is true either way. Parent: re-check mybrow247.net before sending if you want an absolute claim.

## Facts deliberately NOT on the site
- No Yelp review counts/ratings (third-party aggregates are not the business's own facts).
- No hours (directory hours Mon–Sat 10–5 exist on Yelp/aggregators, but the business's own Instagram publishes no hours — omitted rather than copied from a directory).
- No prices, no service list beyond microblading/permanent makeup + one-to-one custom design (the only services evidenced by the business's own feed/bio).
- No artist name "Yunmi/YoonMi" (that name comes from a third-party review, not from the business's own bio/feed in English — omitted).
- No ZIP code (conflict: Instagram business info says 22030; the task brief and BestProsInTown say 22031; a Yelp snippet also showed 22030. Street + city + state are consistent everywhere, so only those are printed).

## Photo harvest log (oEmbed route)
- Method: `curl -A "Mozilla/5.0 (iPhone; CPU iPhone OS 17_0 like Mac OS X)" "https://www.instagram.com/api/v1/oembed/?url=https://www.instagram.com/p/<POST_ID>/"`, then downloaded `thumbnail_url` with browser Referer + iPhone UA.
- Every oEmbed response returned `author_name: mybrow247` (matches the handle) — verified per post.
- Reel poster frames with baked-in play buttons: NONE (all 7 are image/carousel posts, no reels).
- Source ceiling: 640 px wide (oEmbed thumbnails). Files are NOT upscaled; hero is 640 px wide, within the ≤1600w cap, content within ≤1100w.

| Site file | Source post | Natural size | Use |
|---|---|---|---|
| hero-brows.webp | Dewfi9Cx_KS (21 Oct 2026) | 640×736 portrait | Hero |
| work-1.webp | DewhT44xsnQ (21 Oct 2026) | 640×640 square | Gallery |
| work-2.webp | Dewg0GARaIm (21 Oct 2026) | 640×640 square | Gallery |
| work-3.webp | DewgcIIEYGE (21 Oct 2026, carousel first frame) | 640×640 square | Gallery |
| work-4.webp | DewfBG9xI2h (21 Oct 2026) | 640×640 square | Gallery |
| work-5.webp | Dewe41WxIN_ (21 Oct 2026) | 640×640 square | Gallery |
| work-6.webp | DewexIBxZFp (21 Oct 2026) | 640×640 square | Gallery |

All converted to WebP, quality 78. No base64 images anywhere in the HTML.

## Image-fit audit
- Hero: portrait source (640×736) shown with `object-fit: contain` in a frame that keeps its full height; capped at 560 px tall on desktop (480 px at ≤768 px). Full brow subject visible, nothing cropped.
- Gallery: square sources in square `aspect-ratio: 1/1` frames with `object-fit: contain` on a warm background — full subject visible at every width.
- No `cover` cropping is used on any client photo. No image is stretched or distorted (width/height attributes match natural ratios).
- Responsive: mobile-first CSS; single-column stack at ≤520 px, two-column at ≤768 px, three-column gallery at desktop. No fixed widths that overflow; nav wraps. Verification was by CSS audit only — no live viewport check was possible from this subagent (no live browser available), so the parent should eyeball ~390/768/1440 px before calling it final.

## Contrast table (WCAG AA, normal text needs ≥4.5:1)
Computed from hex values; all pass, most by a wide margin.

| Text | On background | Ratio | Pass |
|---|---|---|---|
| #2B1D16 body/heading | #FDF9F4 ivory | 15.53:1 | Yes |
| #2B1D16 body | #EFE6DC band | 13.20:1 | Yes |
| #2B1D16 body | #FFFFFF | 16.28:1 | Yes |
| #5C4030 captions/footer | #FDF9F4 ivory | 8.98:1 | Yes |
| #6B3F2A eyebrow label | #FDF9F4 ivory | 8.86:1 | Yes (white on same brown also 8.86:1) |
| #FFFFFF CTA label | #4A2C1E button | 12.57:1 | Yes |
| #4A2C1E links | #EFE6DC band | 10.19:1 | Yes |
| #FDF9F4 visit-box text | #2B1D16 dark box | 15.53:1 | Yes |

No purple/blue gradients, no glassmorphism, no glowing borders, no decorative icons. Palette (warm ivory, espresso brown, taupe) is specific to a brow/PMU studio, not a generic template. Google Fonts CDN links are the only absolute URLs in the page (allowed); all internal links/images are relative. The Instagram profile link is an external link, not an internal one.

## DM draft (for parent to send — NOT sent by this build)
> Hi! I came across your recent before-and-afters from this week — the natural, one-to-one custom brow work really stands out, especially how soft the healed-looking results are. I noticed everything runs through your Instagram right now, so I made you a small preview website that puts your recent work, your Fairfax studio address, and your phone booking in one place for new clients who find you on Google. Would you like to take a look? Here's the preview: https://jackmax1233-ship-it.github.io/devflix-demos/mybrow247-fairfax/
> — Devflix

## Opportunity / why a good prospect
- Active, recently posting (7 posts on 21 Oct 2026) Virginia-licensed studio with 1,171 followers and strong visual work, but discovery still depends on scrolling Instagram — new Fairfax clients searching for microblading have no single page with work + address + booking.
- Clear, low-friction pitch: one page, her own photos, her own booking route (phone/KakaoTalk) unchanged. No invented services or prices needed.
- Risk to note for the parent: the mybrow247.net domain flag above, and the ZIP conflict — neither blocks the pitch, but neither should be stated absolutely in the DM.

## Author ID notes (for the DM)
- instagram-cli numeric author/user ID: **17841405853059507** (matches the profile `user_id` returned by the authenticated connector).
- oEmbed author ID: **5996059101** (public oEmbed `author_id` for the same @mybrow247 account).
- The two differ because they come from different Instagram ID systems. **Parent should use 17841405853059507** — it is the ID the authenticated connector returns for this profile and is the one prior outreach builds recorded.

## Files
- `index.html`
- `images/hero-brows.webp`, `images/work-1.webp` … `images/work-6.webp` (7 images)
- `BUILD-NOTES.md` (this file)
- NOT deployed, NO tracker edited, NOBODY contacted — per task instructions.
