# BUILD NOTES — EarthPro Landscaping & Tree Care preview site

## 1. Business facts (sources)
| Fact | Source |
|---|---|
| EarthPro Landscaping & Tree Care, @earthproservices | Instagram profile bio |
| 📍 Melbourne, VIC | IG bio |
| 📞 0481 958 464 | IG bio |
| Free On-Site Quotes | IG bio |
| Fully Insured | Campaign brief (policy published by business) |
| 197 followers | IG post rows (author_follower_count) |
| Services: excavation & site prep, concrete cutting & removal, machine scraping & ground levelling, soil & rubbish removal, mini excavator & Kanga loader hire, natural turf installation, artificial grass installation, timber edging, concrete paver walkways, decorative privacy screens, garden bed makeovers, complete landscaping | Campaign brief + IG captions (e.g. "Complete Lawn Transformation" post lists site clearing, machine scraping, topsoil, levelling, natural turf, clean-up; Point Cook post lists artificial grass + timber edging + compaction + weed mat + silica sand) |
| Tree removal / tree care | IG captions: "Another big tree safely removed", "Large tree removal completed safely" |
| Recent job locations named in captions: Point Cook, Viewbank, Highett, Narre Warren North | IG captions (used only generically as "Melbourne" — no street addresses on site) |
| Contact: tel:+61481958464, https://www.instagram.com/earthproservices/ | Derived from published phone + handle only |

**Omitted (never published by the business):** street address, hours, email, prices. None appear anywhere on the site.

## 2. Gap evidence
- Business has **no website** — only an Instagram profile (@earthproservices) and phone/DM contact. Online presence = Instagram-only.
- All quoting happens by phone/DM; no service list, no quote form, no service-area page a Google searcher can land on. A one-page site converts "landscaper Melbourne" searches into free-quote calls.
- Their 238-post portfolio lives only inside Instagram's feed — a site gallery surfaces before/afters to non-Instagram searchers.

## 3. Photos table (all harvested from @earthproservices public IG; nothing invented)
| File | Subject | Natural dims | Frame aspect | Fit / focal |
|---|---|---|---|---|
| img/hero-excavator.webp | Bobcat E20 mini excavator lifting concrete slabs (earthworks action) | 1100×1466 (3:4, resized ≤1100w q78) | 3:4 portrait frame, object-fit cover (no effective crop — ratios match) | Machine fully in frame; sky above is decorative. Hero eager, width/height attrs set |
| img/work-kanga-scrape.webp | Kanga loader on site, machine scrape & levelling | 1100×1466 | 3:4 | Loader centred; full view |
| img/work-turf-laying.webp | Worker carrying fresh turf roll; stacked turf rolls on levelled ground | 1100×1955 | 3:4 | Full view, subject uncut; lazy |
| img/work-lawn-renovation-before.webp | Before: overgrown lawn & site debris (their own "Before" label kept honest via caption) | 1100×1466 | 3:4 | Full view |
| img/work-backyard-before.webp | Before: blank Melbourne backyard with pergola (their "Original Backyard" label) | 1100×1466 | 3:4 | Full view |
| img/work-privacy-screen-before.webp | Before: side yard ahead of decorative privacy screen install | 977×1051 | 977/1051 (natural) | Full view, matched frame |
| img/work-tree-care.webp | Yucca trees crowding fence before safe removal | 1066×1890 | 9:16 (natural) | Full view, matched frame |

Note: several source thumbnails are "before" shots with the business's own baked-in Before/Original labels. The gallery is honestly captioned ("Before · …") rather than presented as finished work. "After" carousel frames are not exposed by any available IG endpoint, so the gallery pairs before-shots with in-progress action shots.

## 4. Palette & type
- Palette: warm paper `#F6F2E9`, warm ink `#2E2A22`, deep eucalyptus `#1E3A2A` / `#16291E`, moss `#3E6B45`, soil brown `#6B4F33` / `#3E3226`, hi-vis amber `#E9A614` (workwear accent). No gradients, no glassmorphism.
- Type: **Zilla Slab** (slab display, trade feel) + **Inter** (body), Google Fonts with display=swap; Georgia/system fallbacks.
- Size caps: hero photo 420w × 560h on desktop (at cap); gallery frames keep natural portrait aspects — the 340px card cap is deliberately overridden because uniform cropping would cut machinery/lawns (FULL VIEW wins per the 21 Oct standing order).

## 5. Contrast audit (computed, WCAG AA ≥ 4.5:1 normal text)
| Pair | Ratio | Use |
|---|---|---|
| `#2E2A22` on `#F6F2E9` | 12.78 | Body text on paper |
| `#F6F2E9` on `#1E3A2A` | 11.10 | Header/nav/trust text on deep green |
| `#2E2A22` on `#E9A614` | 6.75 | Amber CTA buttons |
| `#2E2A22` on `#C98F0E` | 5.05 | Amber button hover |
| `#E9A614` on `#1E3A2A` | 5.86 | Amber headings/links on dark |
| `#E9A614` on `#16291E` | 7.25 | Amber on darkest green |
| `#3E6B45` on `#F6F2E9` | 5.54 | Hero accent headline span |
| `#6B4F33` on `#F6F2E9` | 6.73 | Section kickers |
| `#4A443A` on `#F6F2E9` | 8.63 | Lede/body-soft on paper |
| `#4A443A` on `#FFFFFF` | 9.64 | Service card body |
| `#1E3A2A` on `#FFFFFF` | 12.40 | Policy chips |
| `#F6F2E9` on `#3E3226` | 11.13 | Gallery section headings |
| `#EDE6D4` on `#3E3226` | 9.99 | Gallery captions |
| `#EDE6D4` on `#1E3A2A` | 9.96 | Why/contact body on green |
| `#CFC7B2` on `#16291E` | 9.10 | Footer |

## 6. Facts discipline
- Every service, policy and photo is from the business's own published Instagram captions/bio or the verified campaign brief. 
- NOT invented: no prices, no service-area suburbs beyond "Melbourne VIC", no reviews/ratings/testimonials (site has none), no address/hours/email, no project counts except "hundreds of project photos" (brief: 238-post portfolio).
- "One crew from scrape to finish" is evidenced by captions listing full work scopes per job; "machines on hand" by their machine fleet posts.

## 7. Responsive verification
- Mobile-first CSS; breakpoints 640px / 900px. `overflow-x:hidden` on body; `.wrap` = min(1120px, 100% − 2.5rem).
- Hero stacks at <900px (text then full-view portrait photo); services 1→2 col; gallery 1→2→3 col; trust strip 1→3 col; process 1→3 col.
- Nav links hidden <900px, brand + "Free On-Site Quote" CTA remain — usable without hamburger on a one-pager.
- No headless browser available in this environment; verified by systematic CSS review: all flex/grid containers wrap, clamp() type, no fixed widths, frames use aspect-ratio matching natural photo ratios, focus-visible outlines on all interactive elements. JS-gated reveal keeps content visible with JS disabled; prefers-reduced-motion respected.
- Known trade-off (documented): gallery cards exceed the 340px height cap at desktop (3:4 portraits) — full-view rule wins per standing order.

## 8. DM draft (~80 words)
Hi! I came across EarthPro on Instagram — the mini excavator pulling up concrete slabs and your turf jobs in Point Cook stood out; you clearly handle the whole job from scrape to finish. I noticed you don't have a website yet, so I built a free one-page preview from your own job photos: [URL]. It lays out your services and makes the free on-site quote easy to request. Want me to tailor it or put it live for you? — Devflix
