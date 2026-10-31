# BUILD-NOTES — Lisa Art Dubai (lisa-art-dubai)

- Palette: Gallery white #FDFCF8, ink #23201E, vermilion #A62B1F, warm paper band #F3EEE2
- Fonts: Playfair Display (display serif) + Inter (Google Fonts, display=swap, 2 families max)
- Layout: Editorial hero (text + framed photo), services/classes cards, full-view gallery, steps, CTA band. Business-specific copy only from research/batch-morning-31oct-PKGULF.json qualified record — no invented prices, testimonials, stats or services. Business's own bio claims, where used, are attributed as such on the page.
- Images: Business's own Instagram post photos, converted JPG→WebP (PIL, quality 78, max width 1100; source images were 640px wide). Separate files in images/, never base64. width/height attributes set; hero eager, gallery lazy-loaded below fold.
- FULL VIEW: All photos use object-fit:contain inside ratio-preserving frames with max-height caps (hero ≤520px, gallery ≤330px) — no cropping; faces/products/children are never cut. Mini Sports (children) uses the same contain treatment with particular care.
- Hero frame: ≤560px tall on desktop (capped at 520px). Gallery frames: ≤340px (capped at 330px).
- Contrast (WCAG AA, computed):
- #23201E on #FDFCF8 = 15.77:1 — body text on background (AA PASS; large-text threshold 3:1)
- #3E3A37 on #FDFCF8 = 10.97:1 — lede/body copy (AA PASS; large-text threshold 3:1)
- #A62B1F on #FDFCF8 = 6.85:1 — accent / eyebrow (AA PASS; large-text threshold 3:1)
- #FFFFFF on #A62B1F = 7.03:1 — button label on accent (AA PASS; large-text threshold 3:1)
- #625C57 on #FDFCF8 = 6.42:1 — muted captions (AA PASS; large-text threshold 3:1)
- #FDFCF8 on #23201E = 15.77:1 — dark section text (AA PASS; large-text threshold 3:1)
- Responsive: grid collapses 3→2→1 columns; verified locally at 390/768/1440 (see run31/shots). No horizontal overflow check: documentElement.scrollWidth <= innerWidth.
- Motion: scroll-reveal via IntersectionObserver gated behind .js class (content visible without JS); prefers-reduced-motion disables reveal/transition.
- Local verification note: Live-URL screenshots are not possible from this VM (Chromium egress proxy fails on https); screenshots were taken against a local http.server serving the built folder. Google Fonts may fall back to system fonts in local Chromium — acceptable per coordinator note; live site loads Google Fonts normally.
- CTA: All CTAs link to the business's Instagram profile https://www.instagram.com/lisaart.dubai/
