# Build notes — east-village-shoe-repair (Devflix outreach, Fri 23 Oct 2026)

Site: single `index.html` + `img/*.webp` (14 photos). Relative paths only; deploys as
subfolder at `https://the-cut-co.pages.dev/east-village-shoe-repair/`.

## (a) Contrast table (computed with relative-luminance formula, WCAG 2.1)

| # | Text | Background | Ratio | Verdict |
|---|------|-----------|-------|---------|
| 1 | Ink `#2A2119` (body, headings) | Paper `#F6F1E7` | 14.03 | PASS (≥4.5) |
| 2 | Muted `#61553F` (secondary body) | Paper `#F6F1E7` | 6.48 | PASS (≥4.5) |
| 3 | Link `#7A4E1E` (inline links) | Paper `#F6F1E7` | 6.35 | PASS (≥4.5) |
| 4 | Ink `#2A2119` | Card white `#FFFDF7` | 15.52 | PASS (≥4.5) |
| 5 | Cream `#F5EFE1` (dark-section text, solid btn label) | Coal `#201913` | 15.14 | PASS (≥4.5) |
| 6 | Cream-dim `#CFC0A6` (dark-section secondary) | Coal `#201913` | 9.71 | PASS (≥4.5) |
| 7 | Brass `#C9A15A` (kickers/nav accents on dark, nav-CTA label) | Coal `#201913` | 7.21 | PASS (≥4.5; also used for large text) |
| 8 | Coal `#201913` (nav-CTA label) | Brass `#C9A15A` | 7.21 | PASS (≥4.5) |
| 9 | Brass `#C9A15A` | Coal on nav border accent | n/a (decorative 1px border) | n/a |

All text pairs ≥ 4.5:1. No large-text-only exemptions used. Monogram "EV" uses brass on
coal (7.21). Nav links are cream on coal (15.14).

## (b) Image-fit audit — all 14 photos shown at native ratio (zero crop)

Every frame's aspect ratio equals the photo's natural ratio, so `object-fit:cover` crops
nothing and the full subject (shoe/product/person) is always visible.

| File | Natural (w×h, ratio) | Frame | Fit | object-position | Full-view note |
|------|---------------------|-------|-----|-----------------|----------------|
| hero-nike-mods.webp | 640×480 (1.333) | 4:3 (matched) | cover | center | Full shoe visible; frame = native ratio, no crop |
| restored-swears.webp | 640×853 (0.750) | portrait 640:853 (matched) | n/a (natural height) | n/a | Full pair visible in editorial row, ≤453px tall |
| tiny-platforms.webp | 640×849 (0.754) | portrait 640:849 (matched) | n/a | n/a | Full view, ≤451px tall |
| converse-samples.webp | 640×852 (0.751) | portrait 640:852 (matched) | n/a | n/a | Full view, ≤453px tall |
| nyfw-fall24.webp | 640×853 (0.750) | portrait 640:853 (matched) | n/a | n/a | Full view, ≤453px tall |
| east-village-days.webp | 640×596 (1.074) | 640:596 (matched) | cover | center | Full view; no crop |
| workshop-eugene.webp | 640×428 (1.495) | 3:2 (matched) | cover | center | Full view; no crop |
| vogue-zubo.webp | 640×741 (0.864) | portrait 640:741 (matched) | n/a (natural height) | n/a | Full view |
| fox5-segment.webp | 640×1138 (0.562) | portrait 640:1138 (matched), capped 250px wide → 444px tall | n/a | n/a | Full view (reel cover) |
| kevin-hart-gq.webp | 480×640 (0.750) | portrait 3:4 (matched) | n/a | n/a | Full view |
| nyfw-sept24.webp | 640×548 (1.168) | 640:548 (matched) | n/a | n/a | Full view |
| zubo-nyfw-fall.webp | 640×534 (1.199) | 640:534 (matched) | n/a | n/a | Full view |
| restored-swears-2.webp | 640×853 (0.750) | portrait 640:853 (matched) | n/a | n/a | Full view (gallery) |
| boris-portrait.webp | 640×796 (0.804) | portrait 640:796 (matched) | n/a | n/a | Full view (gallery) |

Hero ≤560px tall on desktop (4:3 at ~530px column ≈ 398px). Editorial images ≤453px tall
(content ≤480px rule). No face/shoe/product is cropped in any frame.

## (c) Fact sources — every claim traced

- Name, handle `@eastvillageshoerepair_bk`, 1073 Broadway Brooklyn NY 11221, phone
  347-835-8549 (ask for Boris), email eastvillageshoerepair@gmail.com, services
  (custom footwear, experimental sneaker silhouettes, resoling/shining, custom sneaker
  design): research JSON
  `~/workspace/instagram/lead-campaign/research/batch-afternoon-23oct-USCA.json`,
  `bio_facts` (published IG business info).
- Designer "Boris Zuborev", collaborator "Eugene Finkelberg": research JSON
  `why_good_prospect`.
- "Reinventing shoes" / "extending the lives of shoes for decades": the business's own
  IG bio ("Reinventing 👞") and caption on reel C7X6QAiNPOY ("For decades we've been in
  the business of extending lives of shoes…").
- Vogue mention of Zubo at NYFW Feb 2025: their own caption on
  https://www.instagram.com/p/DRK79aAEkH_/ ("Vogue mention of our ZUBO collection at
  NY Fashion Week in February'25").
- FOX5 NY segment: their own caption on https://www.instagram.com/reel/C2-bSpoOL7f/
  ("short segment from @fox5ny").
- Kevin Hart in EVSR platforms for GQ Magazine: their own caption on
  https://www.instagram.com/p/Da5iC85EZ0M/.
- Zubo adjustable-height platforms at NYFW Sept 2024 / fall '24: their own captions on
  https://www.instagram.com/p/DRK68cCElqA/, /p/DRK7ZIAkiX2/, /p/DRK6rXWkixr/
  (prototype: /p/DRK58VhkjZi/).
- "From the East Village days" heritage + Eugene at the old store: their own captions on
  https://www.instagram.com/p/DefBtOYmId6/ and /p/DRaKSZIERVu/.
- Super Bowl: named in their own IG bio ("Super Bowl, Vogue, ID Vice, Paper, Glamour,
  NY Post, Fox 5") — used only qualitatively, no numbers.
- Press names i-D/VICE, Paper, Glamour, NY Post appear in their bio; NOT used as
  headline claims (could not verify individual features from captions).
- OMITTED: any view/like counts (not sourced to their own posts); prices (none
  published); hours (none published); reviews/ratings (none published); founding year
  (not published).

## (d) Photo harvest log

Method: `instagram-cli posts` for @eastvillageshoerepair_bk → 76 posts; oEmbed public
endpoint for 16 candidates; `author_name` verified `eastvillageshoerepair_bk` on all 15
kept. One candidate rejected: `DGV013bgVtc` (author `pipencolorena`, a collaborator's
post — not the business's own). One candidate dropped for weak content
(`DTWD9MJknWR`). Final 14, all 640px CDN thumbnails (ceiling) → WebP q78.

| Post URL | Used as |
|----------|---------|
| https://www.instagram.com/p/DdZgEtIFupA/ (Nike on oversized sole) | hero |
| https://www.instagram.com/p/DP4a1S6ksIj/ (Restored vintage Swears) | services — repair |
| https://www.instagram.com/p/DbToDellg5X/ (Tiny EVSR platforms) | services — custom |
| https://www.instagram.com/p/DRKtaz9kdUb/ (Thigh-high/knee-high Converse samples) | services — modification |
| https://www.instagram.com/p/DRK7ZIAkiX2/ (Zubo NYFW fall '24) | services — signature |
| https://www.instagram.com/p/DefBtOYmId6/ (From the East Village days) | story — heritage |
| https://www.instagram.com/p/DRaKSZIERVu/ (Eugene at the old store) | story — workshop |
| https://www.instagram.com/p/DRK79aAEkH_/ (Vogue mention, Zubo NYFW Feb '25) | press — Vogue |
| https://www.instagram.com/reel/C2-bSpoOL7f/ (FOX5 NY segment) | press — FOX5 |
| https://www.instagram.com/p/Da5iC85EZ0M/ (Kevin Hart in EVSR platforms, GQ) | press — GQ |
| https://www.instagram.com/p/DRK68cCElqA/ (Zubo NYFW Sept 2024) | press — NYFW |
| https://www.instagram.com/p/DRK6rXWkixr/ (Zubo NYFW fall) | gallery |
| https://www.instagram.com/p/DeAVruikr-v/ (Restored Swears) | gallery |
| https://www.instagram.com/p/DU806jUEj41/ (Boris portrait) | gallery |

No stock, no AI images. All alt text describes the actual photo.

## (e) Personalized DM draft (Devflix outreach)

> Hi Boris — came across EVSR while looking at Brooklyn craft workshops, and I had to
> say: Vogue mentions, a FOX5 segment, NYFW runways… and still no actual website. Right
> now all of that attention has nowhere to land except a YouTube Shorts link and your
> DMs. I built you a concept site so you can see what an owned home for the workshop
> could look like — your real repair + custom work, the Zubo story, and a proper
> contact page (call/email/IG): https://the-cut-co.pages.dev/east-village-shoe-repair/
> If you ever wanted a simple page where press and customers can actually reach you —
> would something like this be useful, or are DMs working fine for you?

## (f) Honest shortfalls

1. Photo resolution ceiling: IG CDN oEmbed thumbnails max out at 640px wide; fine for
   web display at/below native size, but hero is not retina-crisp at 1440px. No higher-
   res source available without the business.
2. No live browser on this VM: layout verified by static CSS audit (breakpoints
   390/720/900/1024, overflow-x hidden, nav collapses, sections stack, reveal gated
   behind `.js`). A live visual pass at ~390/768/1440px is RECOMMENDED before any DM.
3. FOX5 image is a reel-cover thumbnail (640×1138), not a press photo — framed at
   native ratio; acceptable but portrait-tall.
4. Hours, pricing, founding year, review quotes: none published → none shown. Contact
   section is call/email/IG only (no fake booking form).
5. The 76-post list via instagram-cli returned captions but no per-post media URLs, so
   candidates were chosen by caption; some strong video moments (Lady Gaga, AGT fire
   shoes) were skipped because photo posts fit the design better.
6. Zip includes BUILD-NOTES.md (internal); harmless on deploy but parent may strip it.
