# BUILD NOTES — Windsor–Maidenhead Submission Grappling (WMSG)

- Slug: `wmsg-grappling-maidenhead`
- Local dir: `~/workspace/instagram/lead-campaign/sites/wmsg-grappling-maidenhead/`
- Intended preview link (deploy NOT done by this task): https://jackmax1233-ship-it.github.io/devflix-demos/wmsg-grappling-maidenhead/
- Built: Sun 25 Oct 2026, morning batch. No DM sent, no tracker edited, no deploy performed.
- Photos: the club's OWN Instagram photos only. No stock, no AI, no other business's imagery.

## (a) Contrast table (WCAG AA: ≥4.5:1 normal text, ≥3:1 large text)

Computed with the standard relative-luminance formula.

| Foreground | Background | Ratio | Use | Verdict |
|---|---|---|---|---|
| #F5F1E8 (paper) | #111111 (mat black) | 16.75:1 | Body text, headings | Pass (normal) |
| #B8B3A8 (muted) | #111111 | 9.04:1 | Secondary / caption text | Pass (normal) |
| #FFFFFF | #C1272D (red button) | 5.84:1 | Button labels | Pass (normal) |
| #F5F1E8 | #1E1E1E (band bg) | 14.79:1 | Text on band sections | Pass (normal) |
| #111111 | #F5F1E8 | 16.75:1 | (inverse pairing, if used) | Pass (normal) |
| #C1272D (red) | #111111 | 3.23:1 | LARGE display text only (hero accent word, brand accent) | Pass (large only) |

Rule enforced in the build: red #C1272D is NEVER used for body or small text — only for large headings/accents (≥3:1 large-text threshold) and as a button background with white text (5.84:1). No text sits over a photo without a solid dark ground behind it.

## (b) Image-fit audit (full-view gate)

Every image is shown with `object-fit: contain` on a solid dark ground (or, for the hero, a frame whose 16:9 ratio exactly matches the source), so no person is ever cropped mid-action. Width/height attributes are set on every `<img>`.

| File | Source size | Placement | Display | Crop? |
|---|---|---|---|---|
| mat-wednesday.webp | 640×360 (16:9) | Hero | contain, max-height 540px (renders ~281px at desktop column width) | None — frame matches source ratio |
| training-camp.webp | 640×480 (4:3) | Coach section | contain, max-height 420px | None |
| sunday-class.webp | 640×853 (3:4 portrait) | Beginners section | contain, max-height 420px | None |
| monday-class.webp | 640×360 (16:9) | Gallery | contain, 320px frame | None |
| monday-class-2.webp | 640×800 (4:5) | Gallery | contain, 320px frame | None |
| training-2.webp | 640×1138 (9:16) | Gallery | contain, 320px frame | None |
| training-3.webp | 640×1138 (9:16) | Gallery | contain, 320px frame | None |
| training-4.webp | 640×1138 (9:16) | Gallery | contain, 320px frame | None |
| training-5.webp | 640×800 (4:5) | Gallery | contain, 320px frame | None |
| training-6.webp | 640×800 (4:5) | Gallery | contain, 320px frame | None |

Size caps respected: hero ≤560px tall, cards/bands ≤420px, gallery frames 320px (340px mobile max via max-height rule). All images are separate WebP files in `images/` (quality ~78, 12–58 KB each, 368 KB total); NO base64 in HTML; all paths relative (`images/xxx.webp`, no leading slash) so GitHub Pages subpath deploys work.

## (c) Fact sources — every claim traced

All facts come from the task brief (which traces to the club's own Instagram bio/captions and a directory listing). Nothing else was invented.

| Claim on site | Source |
|---|---|
| Disciplines: BJJ, submission grappling, freestyle wrestling | Brief / club bio |
| Head coach Keith Ellis, BJJ black belt, ADCC European trials master champion | Brief / club bio ("per bio" stated on site) |
| Class times: Mon 6pm, Wed evening, Fri 6:30am, Sun 11am | Brief / club captions (Mon 6pm posts 18 & 11 Oct; Sun 11am post 17 Oct) |
| Beginners welcome ("mix from complete beginners") | Brief / club caption |
| Club "looking for more regular training partners and members" | Brief / 21 Oct caption |
| Area: Cox Green, Maidenhead, Berkshire | Brief / directory listing |
| No phone/email published; contact via IG DM | Brief (gap statement) |
| No street address published | Brief — deliberately NOT published on site |
| No prices, testimonials, ratings, or stats | None claimed anywhere on site; footer states this explicitly |

Deliberately absent: street address, phone, email, membership prices, reviews, class counts, "best" claims.

## (d) Photo harvest log

Method: public oEmbed endpoint with iPhone UA; `author_name` verified = `windsor_maidenhead_sub_grapple` for every shortcode; thumbnail downloaded with browser UA + Instagram Referer; converted to WebP quality ~78 via Python PIL. 640px is the oEmbed ceiling.

| Shortcode | Date (per brief) | File | Result |
|---|---|---|---|
| DexiXJnl3Nd | 2026-10-21 (Wed session) | mat-wednesday.webp | OK, 640×360, 28 KB |
| DexnlZrItj1 | — | training-2.webp | OK, 640×1138, 35 KB |
| DexjnfBBuPY | — | training-3.webp | OK, 640×1138, 12 KB |
| DexiufNh5El | 2026-10-21 | training-4.webp | OK, 640×1138, 33 KB |
| DepTlQpFwQD | 2026-10-18 (Mon 6pm) | monday-class.webp | OK, 640×360, 29 KB |
| Dem08lwCHpL | 2026-10-17 (Sun 11am) | sunday-class.webp | OK, 640×853, 57 KB |
| Deh3NqwMJKE | 2026-10-15 | training-5.webp | OK, 640×800, 21 KB |
| Defewo5PVBG | 2026-10-14 | training-6.webp | OK, 640×800, 41 KB |
| DeaDPmEiLyR | 2026-10-12 (camp) | training-camp.webp | OK, 640×480, 46 KB |
| DeWtcFqoRhT | 2026-10-11 (Mon 6pm) | monday-class-2.webp | OK, 640×800, 38 KB |

Harvested 10/10 attempted. No failures, no shortfall, no substitution.
Note: the first manual download attempt 403'd on 6 files because hand-copied CDN URLs were truncated; re-running as a single oEmbed→download pipeline fixed all of them. Final files above are the pipeline output.

## (e) DM draft (for the parent agent — NOT sent)

> Hi — I came across Windsor–Maidenhead Submission Grappling and noticed there's no website, so anyone new has to dig through captions just to find out when classes are on. I put together a quick preview site for the club with your class times (Mon 6pm, Wed evening, Fri 6:30am, Sun 11am), the three disciplines, and a note that complete beginners are welcome — all using your own photos: https://jackmax1233-ship-it.github.io/devflix-demos/wmsg-grappling-maidenhead/
>
> Thought it might help turn the people already finding you on Instagram into people actually walking through the door, especially with you looking for more regular training partners. Would you like me to tweak anything on it, or is a proper site something you'd want for the club?

Tone notes: addressed to the club, not to Keith as an influencer; one genuine observation (class times buried in captions); no fake compliments, no invented stats, no price claims.

## Responsive audit (CSS audit — no Chromium on this VM)

- Breakpoints: ≤900px stacks hero/split/gallery to one column; ≤480px stacks timetable to one column, gallery images switch to auto height capped at 340px.
- No fixed widths, no absolute-positioned overlapping elements, no horizontal-scroll risks identified (max-width container + box-sizing everywhere, flex-wrap on nav/CTA rows).
- Caveat: this is a careful CSS audit only. A live visual pass at ~390px / ~768px / ~1440px is still recommended before the site is called fully verified.
