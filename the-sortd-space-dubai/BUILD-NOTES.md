# BUILD-NOTES — The Sortd Space (the-sortd-space-dubai)

- Palette: Warm linen #FAF7F1, ink #2B2926, deep olive #3E4F36, stone band #EFE9DC
- Fonts: Fraunces (display serif) + Inter (Google Fonts, display=swap, 2 families max)
- Layout: Editorial hero (text + framed photo), services/classes cards, full-view gallery, steps, CTA band. Business-specific copy only from research/batch-morning-31oct-PKGULF.json qualified record — no invented prices, testimonials, stats or services. Business's own bio claims, where used, are attributed as such on the page.
- Images: Business's own Instagram post photos, converted JPG→WebP (PIL, quality 78, max width 1100; source images were 640px wide). Separate files in images/, never base64. width/height attributes set; hero eager, gallery lazy-loaded below fold.
- FULL VIEW: All photos use object-fit:contain inside ratio-preserving frames with max-height caps (hero ≤520px, gallery ≤330px) — no cropping; faces/products/children are never cut. Mini Sports (children) uses the same contain treatment with particular care.
- Hero frame: ≤560px tall on desktop (capped at 520px). Gallery frames: ≤340px (capped at 330px).
- Contrast (WCAG AA, computed):
- #2B2926 on #FAF7F1 = 13.56:1 — body text on background (AA PASS; large-text threshold 3:1)
- #3D3A35 on #FAF7F1 = 10.59:1 — lede/body copy (AA PASS; large-text threshold 3:1)
- #3E4F36 on #FAF7F1 = 8.26:1 — accent / eyebrow / links (AA PASS; large-text threshold 3:1)
- #FFFFFF on #3E4F36 = 8.84:1 — button label on accent (AA PASS; large-text threshold 3:1)
- #5F5A51 on #FAF7F1 = 6.4:1 — muted captions (AA PASS; large-text threshold 3:1)
- #FAF7F1 on #2B2926 = 13.56:1 — dark section text (AA PASS; large-text threshold 3:1)
- Responsive: grid collapses 3→2→1 columns; verified locally at 390/768/1440 (see run31/shots). No horizontal overflow check: documentElement.scrollWidth <= innerWidth.
- Motion: scroll-reveal via IntersectionObserver gated behind .js class (content visible without JS); prefers-reduced-motion disables reveal/transition.
- Local verification note: Live-URL screenshots are not possible from this VM (Chromium egress proxy fails on https); screenshots were taken against a local http.server serving the built folder. Google Fonts may fall back to system fonts in local Chromium — acceptable per coordinator note; live site loads Google Fonts normally.
- CTA: All CTAs link to the business's Instagram profile https://www.instagram.com/thesortdspace.ae/
