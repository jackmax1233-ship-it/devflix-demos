# BUILD NOTES — Jays Marquee Hire

- Fonts: Fraunces + Public Sans (Google Fonts, display=swap, 2 families).
- Contrast pairs checked (all meet WCAG AA: body >=4.5:1, large >=3:1): #1F2A22 on #FAF6EE; #4A5548 on #FAF6EE; #FFFFFF on #2E5A3C; #FAF6EE on #1F2A22 (strip).
- Images: the business's own Instagram photos via public oEmbed, author_name verified against the handle, converted to WebP q78, separate files (no base64), width/height attributes set, lazy-loaded below the fold.
- Full view: every figure's aspect-ratio matches the photo's natural dimensions and images use object-fit:contain — no face, person, pony or product is cropped.
- Hero frame: text/photo grid, photo height capped by layout (<=~560px desktop at natural ratio); gallery frames <=~340px wide columns with natural ratios.
- Responsive: single-column stacking under 760px, overflow-x hidden, verified locally at 390/768/1440 (screenshots in run31/shots; live URL checked separately with curl because Chromium cannot reach live https from this VM).
- Local-render note: Google Fonts may fall back to system fonts in local Chromium screenshots; live site loads the specified Google Fonts.
- Copy: only facts from the research record / the business's own posts. No invented prices, testimonials or stats.
