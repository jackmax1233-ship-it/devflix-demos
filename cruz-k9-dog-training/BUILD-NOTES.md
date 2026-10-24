# BUILD NOTES — Cruz K9 Dog Training (cruz-k9-dog-training)

**Slug:** `cruz-k9-dog-training`
**Built:** Fri 23 Oct 2026 (afternoon batch)
**Photos used:** 12 (all own-IG, oEmbed-verified `cruz_k9_dogtraining`)
**Preview link placeholder:** https://the-cut-co.pages.dev/cruz-k9-dog-training/
**Fonts:** Oswald (display, 500/600/700) + Inter (body) — 2 families, display=swap
**Palette:** deep forest green #1B3A2A / dark green #0F2419 + warm stone cream #F4EDDE, moss #41564A, ochre #8F6B00 (large-text/decorative only), gold #E9C46A (dark bg only)
**Design lane:** deliberately rugged/outdoorsy (condensed display sans, editorial asymmetric layout, photo-led) — NOT rust/terracotta + serif (that's the parallel Alba K9 Academy build's lane).

---

## (a) Contrast table (computed, WCAG AA)

| Text | Background | Ratio | Requirement | Pass |
|---|---|---|---|---|
| #1B3A2A body | #F4EDDE cream | 10.69 | ≥4.5 | ✓ |
| #41564A moss (eyebrow, copy) | #F4EDDE cream | 6.79 | ≥4.5 | ✓ |
| #41564A moss | #EFE4CC cream-2 (services) | 6.27 | ≥4.5 | ✓ |
| #41564A moss | #FFFFFF (cards) | 7.91 | ≥4.5 | ✓ |
| #F4EDDE cream (btn-solid label) | #1B3A2A green | 10.69 | ≥4.5 | ✓ |
| #FFFFFF (check circles, gallery caps over gradient) | #1B3A2A / dark gradient ≈#0F2419 | ≥12.4 | ≥4.5 | ✓ |
| #F4EDDE cream (proof band, contact) | #0F2419 dark green | 14.00 | ≥4.5 | ✓ |
| #E9C46A gold (header CTA, brand accent, band headline) | #0F2419 dark green | 9.77 | ≥4.5 (small) / ≥3 (large) | ✓ |
| #0F2419 (btn-gold label) | #E9C46A gold | 9.77 | ≥4.5 | ✓ |
| #8F6B00 ochre (hero H1 accent span only) | #F4EDDE cream | 4.22 | ≥3.0 large text | ✓ (large display text, flagged) |

**Count: 10 pairs, all pass.** Ochre is restricted to the hero H1 accent and non-text decoration; never used for body/small text.

## (b) Image-fit audit

All photos arrive at 640px ceiling from IG oEmbed (natural ratio recorded per file). Frames match each photo's natural ratio; `object-fit:cover` therefore crops nothing. No `contain` needed.

| File | Section | Natural | Frame | Fit / position | Full-view note |
|---|---|---|---|---|---|
| kilo.webp | hero | 640×853 portrait | 3/4 (max-h 560px) | cover, center | Kilo (GSD) sits fully in frame; same ratio as source → zero crop. Verified visually: dog's ears to paws all visible |
| caesar.webp | case study | 640×853 portrait | 3/4 (≤340px) | cover, center | Caesar (rottie pup) lower-left + Loki right, both fully visible by the water |
| ragz.webp | case study | 640×640 square | 1/1 (≤340px) | cover, center | Ragz lying on grass, full dog + face visible |
| cali.webp | method | 640×853 portrait | 3/4 (≤480px) | cover, center | Cali standing on hill, full body side profile visible |
| trainer.webp | services 1-to-1 | 640×853 portrait | 3/4 (≤340px) | cover, center | Trainer's face + client's dog fully visible (his own public post) |
| group.webp | services group | 640×851 portrait | 3/4 (≤340px) | cover, center | Indoor class: handlers + dogs across frame, no cropping |
| packwalk.webp | services pack walk | 640×853 portrait | 3/4 (≤340px) | cover, center | Trainer in Cruz K9 shirt + group of dogs on trail, all visible |
| finn.webp | behaviour spotlight | 640×853 portrait | 3/4 (≤480px) | cover, center | Finn the cockapoo sitting, full dog visible |
| handling.webp | wide band | 640×480 landscape | 4/3 (≤420px) | cover, center | Indoor handling class; placed in a two-column band (not full-bleed crop) so nothing is cut |
| bear.webp | gallery | 640×853 portrait | 3/4 (≤340px) | cover, center | Bear lying in grass, full dog visible |
| brodie.webp | gallery | 640×853 portrait | 3/4 (≤340px) | cover, center | Brodie the beagle sitting on bench, full dog visible |
| luna.webp | gallery | 640×853 portrait | 3/4 (≤340px) | cover, center | Head-and-chest portrait from source; Luna's full visible face in frame, nothing cut |

Gallery captions sit on a dark gradient overlay (text-over-image safe).

## (c) Fact sources (every claim traced — nothing invented)

- Bio facts (bio field returned by instagram-cli posts rows): Glasgow, Scotland · "Specialise in Behaviour Modification" · "Balanced Training" · "Fully Qualified" · "All Breeds, Sizes & Ages" · "DM for info" → nav/hero/method/contact copy.
- 1-to-1s + public group classes: bio + 23 Oct post (De1E0-_qcWc): "I don't normally allow anyone to join our group class unless they have worked with us on a 1:1 basis first". https://www.instagram.com/p/De1E0-_qcWc/
- Group class "nothing fancy, no tricks or fancy foot work, just raw exposure to triggers": reel DeSLsEtKM43 caption (returned by instagram-cli, post list row 54).
- Owner handling drills: DRRuQb2igjK caption — "focus was to develop handling skills for the owners. They took turns handling…".
- "18 reactive dogs tonight — some with bite history — some were told they were 'too aggressive'": DQm7nUUCl8K caption (verbatim paraphrase).
- Pack walks, reactive dogs welcome: DcYeynLqLJT caption ("We are back with our PACK WALKS … Reactive dogs welcome").
- Drop & Train service (trainer picks dog up / owner drops off): DPx-8S9CoFY + DaTFPIiKBTH announcement captions.
- Finn (5-yr cockapoo, bitten owner & partner in the home, resource guarding, 8 weeks → zero incidents): DcTeNrRMRaR full caption (pulled via instagram-cli).
- Kilo (7-month GSD, reactivity/lunging at dogs, improved handling busy parks): DQw03vzCnFf full caption.
- Caesar (5 months, first session, foundation/engagement/neutrality/socialisation, with Loki): DeuCpq8K3kl full caption.
- Ragz (Rottweiler, rescued from the meat trade in China, owners had him since March, detailed behaviour case study): DeUFrCaKw0F caption + research JSON.
- Cali (working-line Golden Retriever, "the reason I started all of this"): Dct_ComKfUI caption.
- Luna (ring bearer at owners' wedding): DSIhUyXiuuL caption.
- Bear (German Shepherd): DcJLSlvKtZF caption ("bear the German shep").
- Brodie (beagle, trained on his birthday): DbXrX3mqOxp caption.
- No phone, no street address published; bookings via IG DM → CTA is https://ig.me/m/cruz_k9_dogtraining. Prices deliberately omitted (see shortfalls).
- Trainer's personal name: not published anywhere → never used.

## (d) Photo harvest log

All via public oEmbed (`https://www.instagram.com/api/v1/oembed/?url=…`), `author_name` verified = `cruz_k9_dogtraining` for every post (not login-walled). 640px CDN ceiling, downloaded with browser UA + Instagram Referer, converted to WebP q78 via PIL.

| Post URL | Shortcode | Use |
|---|---|---|
| https://www.instagram.com/p/DQw03vzCnFf/ | DQw03vzCnFf | hero (Kilo) |
| https://www.instagram.com/p/DeuCpq8K3kl/ | DeuCpq8K3kl | case study (Caesar) |
| https://www.instagram.com/p/DeUFrCaKw0F/ | DeUFrCaKw0F | case study (Ragz) |
| https://www.instagram.com/p/Dct_ComKfUI/ | Dct_ComKfUI | method (Cali) |
| https://www.instagram.com/p/DbYwBFXKTZE/ | DbYwBFXKTZE | 1-to-1 card (trainer) |
| https://www.instagram.com/p/De1E0-_qcWc/ | De1E0-_qcWc | group class card |
| https://www.instagram.com/p/DZN4ItzKL1x/ | DZN4ItzKL1x | pack walk card |
| https://www.instagram.com/p/DcTeNrRMRaR/ | DcTeNrRMRaR | behaviour spotlight (Finn) |
| https://www.instagram.com/p/DRRuQb2igjK/ | DRRuQb2igjK | wide band (handling class) |
| https://www.instagram.com/p/DcJLSlvKtZF/ | DcJLSlvKtZF | gallery (Bear) |
| https://www.instagram.com/p/DbXrX3mqOxp/ | DbXrX3mqOxp | gallery (Brodie) |
| https://www.instagram.com/p/DSIhUyXiuuL/ | DSIhUyXiuuL | gallery (Luna) |

Also inspected and rejected: DcYeynLqLJT (pack-walk flyer graphic — dated "12th September", fine visually but stale date risk; skipped), DQm7nUUCl8K (kept only as caption evidence, not a photo).

## (e) Personalized DM draft (Devflix outreach)

> Hey! Watched your group class announcement for Monday — the firework conditioning session is such a smart idea ahead of bonfire night, and your Ragz case study is the kind of honest work that deserves more than an Instagram grid. Right now someone Googling "dog trainer Glasgow" can't find you, your class info, or your prices anywhere — everything lives in your DMs. I built you a demo site from your own posts and photos (Caesar and Ragz are on it): https://the-cut-co.pages.dev/cruz-k9-dog-training/ — have a look and tell me, would something like this help you fill classes without answering the same DM 20 times a day?

(No fake compliments, no invented stats, one genuine observation, preview link, one low-pressure question.)

## (f) Honest shortfalls

1. **No live visual pass:** no Chromium on this VM. Layout was CSS-audited (mobile-first single column → 2/3-col at 640/1024px; `overflow-x:clip` on html/body; nav links hidden ≤639px with DM CTA kept; all images capped per size discipline; reveal gated behind `.js` so content is fully visible without JS; prefers-reduced-motion respected). A real browser check at 390/768/1440px is recommended before DMs.
2. **Photo ceiling 640px:** oEmbed thumbnails max out at 640w — fine at display sizes but not retina-sharp. No login-walled posts encountered; 12 of 16 harvested posts used.
3. **Prices seen but omitted:** the 23 Oct group-class post lists £25 (Monday firework class) and the 23 Aug pack-walk flyer lists £25/dog. Research JSON said "none published" — these exist in captions but look per-event, so prices were left off the site deliberately (nothing invented, nothing that could be wrong). Flag for the business to confirm a price list.
4. **Trainer's name unpublished:** site never names him (only "the trainer") — reads slightly awkward in the method section; his first name from the account would fix it but wasn't published.
5. **Testimonials not quoted:** review-style text only appeared in story highlights (not machine-readable here); no reviews section invented.
6. **Alt competition note:** Alba K9 Academy (Glasgow, same industry) is built in parallel — this design deliberately avoids the warm-academy look (forest green + Oswald, rugged/behaviour-specialist voice).
