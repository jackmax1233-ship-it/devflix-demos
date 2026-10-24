# Char Celebrates — build notes (night batch, 21 Oct 2026)

## 1. Business facts (all business-published, with sources)

| Fact | Source |
|---|---|
| Business name: Char Celebrates; celebrant: Char (Charlotte) | IG profile @charcelebrates, author_name "Char \| Civil Celebrant" |
| Civil wedding celebrant — "professional celebrator of love & life" | IG bio |
| Service area: Brisbane, Sunshine Coast (Gubbi Gubbi) & beyond; will travel | IG bio ("SC/Gubbi Gubbi & beyond"); task brief confirms "Will travel" |
| Followers: 204 | instagram-cli profile data (21 Oct 2026) |
| Contact: charcelebrates@gmail.com (published in bio); IG DM | IG bio |
| Niche: LGBTQ+ friendly ("🌈 friendly space") + Auslan friendly ("🤟🏽 friendly space"); Diploma in Auslan (Australian Sign Language) | IG bio; reel caption 29 Jul 2026 ("I have my Diploma in Auslan") |
| "ALL LOVE IS CELEBRATED HERE 🌈. Come as you are. Love who you love. The paperwork doesn't care who signs it." | IG post caption, 14 Jun 2026 (quoted verbatim in site) |
| Celebrancy journey began 2024 | Welcome post, 21 Oct 2026 |
| Lawyer by day; 2023 bride (married hubby in a bar); born & raised Brisbane; lives Sunshine Coast; fur-mum to a deaf French bulldog | Welcome post fast-facts, 21 Oct 2026 |
| Real weddings w/ dates: Sam & Nick 08.08.2026; Mon & Conor 01.08.2026; G & Scott 18.07.2026; Megan & Matt 18.07.2026; Josh & Chantae; Jess & Lewis (colourful wedding, two French bulldogs) | Post captions 11 Oct / 29 Sep / 26 Sep / 15 Sep / 10 Sep 2026 |
| Photographers credited in captions (not named on site — only Char's own photos used) | captions |

## 2. Gap evidence (opportunity)

- **No website.** IG bio link is Facebook only; zero usable web links.
- Enquiries funnel: email only (charcelebrates@gmail.com) or IG DM — no booking page, no date-availability, no portfolio page, no services/pricing page.
- Google finds nothing for "Char Celebrates celebrant" (per brief research) — all discovery is one IG account with 204 followers.
- Clear, evidenced gap: a warm one-page site (real weddings, inclusivity niche, email/IG CTAs) would give couples a shareable link and a reason to enquire.

## 3. Portfolio (images — her own public IG photos, via instagram-cli + hatch-zeitgeist thumbnails)

| File | Subject (verified by viewing) | Natural dims | Frame | Fit / focal |
|---|---|---|---|---|
| img/josh-chantae.webp | Josh & Chantae holding hands, laughing, lawn in front of Queenslander house | 1100×1467 (3:4) | hero, aspect 3/4, max-w 420px → 560px tall | cover; ratio matches native → **full view**; focal: couple, centre |
| img/jess-lewis.webp | Flat-lay: "The Wedding" embroidered book, colourful bouquet, lace shoes, sparkly bag, "J&L" ring dish | 1100×1467 (3:4) | gallery, 340px-high frame | **contain** → full view; focal: book, centre |
| img/mon-conor.webp | Mon & Conor with wedding party, couple centre | 1100×1467 (3:4) | gallery, 340px-high frame | contain → full view; focal: couple, centre |
| img/g-scott.webp | G & Scott with bridal party (magenta bridesmaids) | 1100×1467 (3:4) | gallery, 340px-high frame | contain → full view; focal: couple, centre-right |
| img/megan-matt.webp | Megan (holding little one, face heart-obscured) & Matt among trees | 1100×1467 (3:4) | gallery, 340px-high frame | contain → full view; focal: couple, centre |
| img/sam-nick.webp | "CHARCELEBRATES CELEBRANT" ceremony folder on table | 720×959 (3:4) | gallery, 340px-high frame | contain → full view; focal: folder, centre |
| img/char-portrait.webp | Char in heart sunglasses + heart-print blouse, disco balls, confetti (her own intro graphic; baked-in text retained) | 1080×1350 (4:5) | about, aspect 4/5, max-w 380px | cover; ratio matches native → **full view**; focal: her face, upper-centre |

- All 7 converted to WebP q78, max width 1100. Hero: eager + fetchpriority=high; rest lazy.
- Gallery uses `object-fit: contain` in 340px frames so every face/couple/detail is shown whole (full-view hard gate wins over the uniform-frame size cap, per 21 Oct order). No faces cut at any width.
- Sam & Nick gallery card uses the folder detail shot because that post's carousel cover is the folder image; labelled as the Sam & Nick wedding per its caption.

## 4. Palette & type

- Palette (wedding-warm, editorial — no gradients, no purple/pink glow): warm ivory `#FBF7F0` (page), sand `#F3EAD9` (about band), deep eucalyptus `#2E4B3F` (headings/bands), deeper green `#1F352C` (buttons/dark band), espresso `#3E3429` (body), dark gold `#75571F` (eyebrows/accents), terracotta `#A63D2F` (display accent, her brand's red family), espresso-brown `#4A3423` (footer).
- Type: Fraunces (display serif, italic accents) + Inter (body), Google Fonts with display=swap, ≤2 families.

## 5. Contrast audit (computed, WCAG AA)

| Pair | Ratio | Required | Verdict |
|---|---|---|---|
| #2E4B3F on #FBF7F0 (headings/nav/buttons-text) | 8.96:1 | 4.5:1 | PASS |
| #3E3429 on #FBF7F0 (body) | 11.38:1 | 4.5:1 | PASS |
| #FBF7F0 on #2E4B3F (ribbon band text) | 8.96:1 | 4.5:1 | PASS |
| #FBF7F0 on #1F352C (buttons, hero caption chip, inclusive band) | 12.26:1 | 4.5:1 | PASS |
| #75571F on #FBF7F0 (eyebrows, "where" line, card dates) | 6.26:1 | 4.5:1 | PASS |
| #75571F on #F3EAD9 (about eyebrow) | 5.60:1 | 4.5:1 | PASS |
| #75571F on #FFFFFF (card dates) | 6.69:1 | 4.5:1 | PASS |
| #A63D2F on #FBF7F0 (display accent "celebrated", contact email) | 5.91:1 | 4.5:1 | PASS |
| #A63D2F on #F3EAD9 (sand section) | 5.28:1 | 4.5:1 | PASS |
| #2E4B3F on #F3EAD9 (about headings) | 8.01:1 | 4.5:1 | PASS |
| #1F352C on #F3EAD9 (ghost button) | 10.96:1 | 4.5:1 | PASS |
| #D9B96A on #1F352C (eyebrow on dark band) | 6.92:1 | 4.5:1 | PASS |
| #EFE6D2 / #E5D9C2 on #1F352C (pillar/sec text) | 10.55 / 9.37:1 | 4.5:1 | PASS |
| #EDE4D2 on #2E4B3F (ribbon paragraph) | 7.58:1 | 4.5:1 | PASS |
| #E3D5BD / #EDE0C8 / #C9B795 on #4A3423 (footer) | 8.04 / 8.91 / 5.92:1 | 4.5:1 | PASS |

15/15 PASS. Note: gold was darkened #8A6A2B → #75571F after it failed 4.21:1 on the sand section.

## 6. Facts discipline

- No prices, packages, reviews, ratings, testimonials, hours, phone, or address — none published by her; none invented.
- Couple names + dates only where her captions state them. "Dogs in bow ties / pets very welcome" phrased as welcome, not a service claim. "Will travel" from brief's verified facts.
- Photo credit line in footer: "Photos: Char Celebrates (@charcelebrates), from her public Instagram." + "Preview concept by Devflix."

## 7. Responsive verification (static + layout math; no live browser available to this builder)

- 1440px: 2-col hero (text 560px / photo 420px→560 tall), 3-col gallery, 3-col pillars.
- 768px: single-col hero (photo ≤440px wide), 2-col gallery (contain = full view), 1-col pillars.
- 390px: single-col everything; nav links become a horizontal scroll row (no clipping); CTA buttons full-width; email link has word-break; h1 clamps to 38–48px; no fixed widths that can overflow; gallery images contain full-view in 340px frames.
- Reveal animation gated behind `.js` (content visible without JS); `prefers-reduced-motion` respected.
- HTML: tags balanced, all 8 `<img>` refs exist with width/height, zero base64, CSS braces balanced.

## 8. DM draft (~80 words, for parent to send post-deploy)

> Hi Char — your Jess & Lewis wedding post stopped me mid-scroll; the colour in that celebration (and two very good French bulldogs) says everything about your style. I also noticed your Auslan-signing niche — a genuinely rare offering for couples. Quick thought: with no website, couples can only find you through Instagram. I built you a one-page preview using your own photos and words: [URL]. No strings — if you love it, happy to make it yours. Is email still the best way to reach you? — Devflix

Facts used in DM: Jess & Lewis colourful wedding + two French bulldogs (her caption), Auslan-signing niche (her reel), no website (verified gap). No invented stats, no fake compliments.
