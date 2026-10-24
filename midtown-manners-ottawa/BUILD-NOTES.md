# Build notes — Midtown Manners (Ottawa, ON)
Slug: `midtown-manners-ottawa` · Built Fri 2026-10-23 (afternoon batch) · Preview: https://the-cut-co.pages.dev/midtown-manners-ottawa/

## (a) Contrast table — all pairs WCAG AA computed via relative-luminance script
| # | Foreground | Background | Ratio | Used for | Verdict |
|---|-----------|-----------|-------|----------|---------|
| 1 | #3A2A1C (ink) | #FAF6EF (cream) | 12.76:1 | body text, headings, brand, nav links | PASS ≥4.5 |
| 2 | #6B5844 (muted) | #FAF6EF (cream) | 6.28:1 | lede, section subs, footer, notes | PASS ≥4.5 |
| 3 | #A03E14 (terracotta) | #FAF6EF (cream) | 6.10:1 | eyebrow labels, links, brand sub | PASS ≥4.5 |
| 4 | #FAF6EF | #2E2113 (dark band) | 14.51:1 | strip list, CTA heading/body, skip link | PASS ≥4.5 |
| 5 | #F2C87D (gold) | #2E2113 (dark band) | 9.93:1 | gold buttons, caption highlights, outline CTA | PASS ≥4.5 |
| 6 | #FFFDF8 | #3A2A1C (ink button) | 13.52:1 | header "DM on Instagram" button | PASS ≥4.5 |
| 7 | #FFFDF8 | #A03E14 (accent button) | 6.47:1 | primary "DM @midtown_manners" button | PASS ≥4.5 |
| 8 | #A03E14 | #F1E8D6 (card bg) | 5.40:1 | step numerals (2.4rem serif, large text ≥3:1) | PASS (large) |
| 9 | #3A2A1C | #F1E8D6 (card bg) | 11.29:1 | service/about/steps card text, blockquote | PASS ≥4.5 |
| 10 | #2E2113 | #F2C87D (gold button) | 9.93:1 | gold "Message @midtown_manners" button | PASS ≥4.5 |
| 11 | #FAF6EF on rgba(46,33,19,.92) | dark caption pill over photo | ≈14:1 | hero caption (Miko label) | PASS ≥4.5 |

10 of 11 pairs pass at ≥4.5:1; the one large-text pair (#8) passes at 5.40:1 (≥3:1). **Contrast audit: PASS.**

## (b) Image-fit audit — per image
| File (img/) | Natural px (px) | Frame ratio | Fit | object-position | Full-view note |
|---|---|---|---|---|---|
| miko-training.webp (hero) | 640×853 (0.750) | 3/4 (0.750) | cover | default (center) | Frame == natural ratio → zero crop; dog fully visible |
| crew-walk-heidi-rosie.webp (about) | 640×480 (1.333) | 4/3 (1.333) | cover | default | Frame == natural ratio → zero crop |
| styx-max-sideview.webp | 640×853 (0.750) | 3/4 | cover | default | zero crop |
| max-bodhi-styx-porch.webp | 640×853 (0.750) | 3/4 | cover | default | zero crop |
| penny-puppy-ikea.webp | 640×851 (0.752) | 3/4 | cover | default | ≤0.3% vertical variance → no visible crop |
| heidi-rosie-bodhi-porch.webp | 640×480 (1.333) | 4/3 | cover | default | zero crop |
| bodhi-walk-style.webp | 640×725 (0.883) | 8/9 (0.889) | cover | default | 0.7% vertical variance → no visible crop |
| penny-leash-manners.webp | 640×851 (0.752) | 3/4 | cover | default | ≤0.3% vertical variance → no visible crop |

Every frame matches its photo's natural orientation (portrait → portrait, landscape → landscape); `cover` only ever crops sub-pixel slivers, never faces or dogs. All 8 photos are Adam's own Instagram posts — no stock, no AI.
Size discipline: hero figure max-width 400px → ~533px tall (≤560px cap); dog cards in 3-col grid (~340px wide) — portrait cards run taller than the ~340px card guideline; per the Oct 21 standing order, **full view wins over uniform card frames**, so card height is accepted.

## (c) Fact sources — every claim traced, nothing invented
- "Midtown Manners", Ottawa, ON, Canada, IG @midtown_manners, 18 followers — research JSON `batch-afternoon-23oct-USCA.json` (Midtown Manners entry).
- IG display name "Adam | Dog Trainer Ottawa"; bio "Helping Humans and Dogs Build Better Relationships" + "DM for a 1-on-1 consultation" — research JSON `bio_facts`; hero H1 uses his bio words verbatim.
- Services: training, boarding, walking; 1-on-1 consultations via DM — research JSON + IG captions: "Styx came for a board and train" (post https://www.instagram.com/p/DatH4x1Pqtg/), walking reels ("Walking around the (Mid) town with Heidi, Rosie and Styx"), training captions across the grid.
- Named dogs featured: Miko (DdbpdaquCKT), Styx & Max (Dbs_UdFOt4X), Max/Bodhi/Styx (Dbs7wXxO3xD), Penny the Puppy (DcCwO0zjGRF), Heidi/Rosie/Kali/Hamish/Max crew (DaeddgLMwQJ), Heidi/Rosie/Bodhi (DaLEUFvu8BN), Bodhi (DaeckR4MH03), Penny (DaMCWQFjqZB) — all from instagram-cli post captions, Oct 23 harvest. Captions under photos paraphrase his own caption text.
- Training focus chips (loose-leash, reactivity, socialization, sit-stays, calm settle/place, puppy manners) — distilled from his captions/reel captions (Miko loose-leash; Styx reactivity; porch/Parkdale socialization; sit-stay reels with Max/Joey; calm/relaxation captions; crate/place reel; Penny puppy posts). NOT presented as a service menu he published — labelled "Training focus areas".
- "No published price list — quoted personally by DM" — research JSON: NO prices, NO phone, NO email published; CTA is IG DM only. The honest-note in About states this explicitly.
- "No website whatsoever" — research JSON `opportunity_observed` (website field empty, no bio links, none found via web search). Footer states the page is a concept preview.
- Recent activity: posted 2026-10-22 (selfie-style training video), 0–8 likes, up to 4 comments — research JSON `activity_evidence`; used only in notes, not on the page.
- DM CTA link https://ig.me/m/midtown_manners — standard IG DM deep link for the handle.

NOT on the page (deliberately): prices, phone, email, address, reviews, ratings, credentials, years of experience, team, service areas beyond Ottawa, testimonials, guarantees. None were published by Adam.

## (d) Photo harvest log
- instagram-cli `posts` for @midtown_manners (account devfl_ix) returned 49 posts; 8 photo posts selected (reels excluded — no reliable stills).
- oEmbed called for all 8 via `https://www.instagram.com/api/v1/oembed/?url=https://www.instagram.com/p/<id>/` — all returned `author_name: midtown_manners` (verified). 640px CDN ceiling.
- Downloaded with iPhone UA + `Referer: https://www.instagram.com/`; converted to WebP q78 (PIL), total 540 KB.
- Source posts: https://www.instagram.com/p/DdbpdaquCKT/ · https://www.instagram.com/p/Dbs_UdFOt4X/ · https://www.instagram.com/p/Dbs7wXxO3xD/ · https://www.instagram.com/p/DcCwO0zjGRF/ · https://www.instagram.com/p/DaeddgLMwQJ/ · https://www.instagram.com/p/DaLEUFvu8BN/ · https://www.instagram.com/p/DaeckR4MH03/ · https://www.instagram.com/p/DaMCWQFjqZB/
- One transcription slip in an early scratch script (two URLs mangled) was caught before any download — URLs were re-pulled programmatically from oEmbed JSON; nothing was fetched from a hand-typed URL.

## (e) Personalized DM draft (Devflix outreach)
> Hey Adam — came across Midtown Manners while looking at Ottawa dog trainers. The grid with Miko, Styx, Max and the crew is great — and "helping humans and dogs build better relationships" is a line people remember.
>
> One thing stood out: everything right now runs through your DMs, and there's no website to land on. A simple one-page site — services, the dogs you've trained, and a clear path to your consultation DM — would professionalize the whole funnel without changing how you work.
>
> I mocked up what that could look like, using your own photos and captions: https://the-cut-co.pages.dev/midtown-manners-ottawa/
>
> Happy to tweak it to exactly how you describe things — would a simple page like this be useful for you?

(Genuine observation: named client dogs + his bio line + the DM-only funnel. Why it helps: professionalizes the 1-on-1 consultation funnel. Preview link, one low-pressure question. No fake compliments, no invented stats.)

## (f) Honest shortfalls
1. **Smallest profile in the batch: 18 followers, 0–8 likes per post.** Real business, textbook gap — but the research file itself flags it as a stretch pick. Set expectations accordingly; this DM is low-odds by follower arithmetic.
2. **640px image ceiling** (IG oEmbed thumbnail max) — adequate for this design's display sizes (hero ≤400px, cards ≤340px) but not for full-screen imagery. No way around it without his originals.
3. **No live visual verification.** No Chromium on this build VM, so verification was a careful CSS audit (breakpoints 640/900, overflow-x hidden, stacked grids, wrapping header, full-width mobile CTAs) — a real-browser visual pass at 390/768/1440px is recommended before DMs go out.
4. **Thin service detail by design.** Adam publishes no prices, process, or credentials, so the site stays modest — services + chips + DM CTA. That's honesty, but a prospect comparing against trainers with pricing pages may want more; the DM draft positions the site as the start of that conversation.
5. Nellie (named in captions — "Nellie the calf" reel) not featured: reels have no reliable stills; not invented instead.
