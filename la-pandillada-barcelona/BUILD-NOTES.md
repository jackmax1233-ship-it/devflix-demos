# BUILD NOTES — La Pandillada (Barcelona) · la-pandillada-barcelona

Built: Fri 23 Oct 2026 (afternoon batch) · Builder: Devflix site-builder subagent
Preview placeholder: https://the-cut-co.pages.dev/la-pandillada-barcelona/
Copy language: Spanish (lang="es", UTF-8). Fonts: Fraunces (display serif) + Nunito (body) via Google Fonts display=swap.

## (a) Contrast table — every text/background pair (all ≥ 4.5:1, normal text)

| # | Text | Background | Ratio | Verdict |
|---|------|------------|-------|---------|
| 1 | Body ink `#3E2A1E` | Cream `#FBF6EC` | 12.54:1 | PASS |
| 2 | Soft ink `#5C4636` (lede, sub, captions) | Cream `#FBF6EC` | 8.18:1 | PASS |
| 3 | Soft ink `#5C4636` | White `#FFFFFF` (figcaption, pillar body) | 8.81:1 | PASS |
| 4 | Olive `#55602E` (eyebrows, brand sub) | Cream `#FBF6EC` | 6.29:1 | PASS |
| 5 | Terracotta `#A84E22` (H1 em, links, time) | Cream `#FBF6EC` | 5.16:1 | PASS |
| 6 | Terracotta `#A84E22` | Cream-2 `#F3EAD8` | 4.65:1 | PASS |
| 7 | Terra-deep `#7E3517` (quote, pillar h3) | Cream `#FBF6EC` | 8.09:1 | PASS |
| 8 | Terra-deep `#7E3517` | White `#FFFFFF` | 8.72:1 | PASS |
| 9 | White `#FFFFFF` (buttons, band text/links) | Terracotta `#A84E22` | 5.56:1 | PASS |
| 10 | White `#FFFFFF` (button hover) | Terra-deep `#7E3517` | 8.72:1 | PASS |
| 11 | Cream `#FBF6EC` (footer text) | Footer `#2F2117` | 14.43:1 | PASS |
| 12 | Peach link `#F6C99B` | Footer `#2F2117` | 10.18:1 | PASS |
| 13 | Muted `#C9B99F` (foot-note) | Footer `#2F2117` | 8.09:1 | PASS |
| 14 | Ink `#3E2A1E` (chips) | Cream-2 `#F3EAD8` | 11.30:1 | PASS |

No large-text-only (3:1) exceptions used — everything meets 4.5:1.

## (b) Image-fit audit — full-view guarantee (childcare: zero cropped faces)

Every figure's `aspect-ratio` matches the source photo's natural ratio exactly, so
`object-fit:cover` cannot crop anything. All 12 harvested photos were visually
inspected before selection; the one text-heavy graphic not used is noted below.

| File (img/) | Source post | Natural | Frame | Fit | Faces fully visible? |
|---|---|---|---|---|---|
| hero-grupo.webp | CVdXqDuK0AG | 640×608 (1.05) | 640/608 | cover (=contain, ratios match) | YES — 4 children + adult, whole group in frame |
| pandi-arbol.webp | Cgm1XVIrqmS | 640×640 (1:1) | 1/1 | cover (=contain) | YES — 3 children laughing, full faces |
| cargobike-parque.webp | CpaS0yQtI1b | 640×640 (1:1) | 1/1 | cover (=contain) | n/a — no people; whole bike in frame |
| cargobike-barrio.webp | C5y3JdmoA3E | 640×480 (4:3) | 4/3 | cover (=contain) | YES — 3 children on scooters + bike, full bodies |
| dia-playa.webp | Dd1nEP6scfN | 640×856 (3:4) | 640/856 | cover (=contain) | YES — 2 children playing, backs/side, uncut |
| juego-lluvia.webp | DeKE2qRDL3g | 640×853 (3:4) | 640/853 | cover (=contain) | n/a — child in rain suit seen from back, umbrella; nothing cropped |
| juego-tiza.webp | Cz6LekZo-Za | 640×640 (1:1) | 1/1 | cover (=contain) | YES — girl drawing, head/face fully in frame |
| juego-calle.webp | C7wFxLVIVWD | 640×640 (1:1) | 1/1 | cover (=contain) | n/a — children running away, backs; uncut |
| juego-verano.webp | CRlkKWLl5N6 | 640×480 (4:3) | 4/3 | cover (=contain) | YES — 3 children, sunglasses, full faces |
| juego-skate.webp | CW8R9BdqOoE | 640×800 (4:5) | 4/5 | cover (=contain) | YES — child on skateboard, face + full body |
| cartel-plazas.webp | DepKFHisWiC | 640×798 (4:5) | 640/798 | contain-equivalent | n/a — business's own enrollment poster graphic, fully legible |

NOT used: DJjKAvZICKZ (photo of a Catalan-language book page about gender roles — text-heavy, off-brand for Spanish copy; skipped, not a face/framing issue).
Size discipline: hero ≤520px tall desktop; content/card images ≤440px; poster ≤480px. All ≤340KB each; lazy-loaded below fold; width/height attrs on all.

## (c) Fact sources — every claim traced, nothing invented

- Business name "La Pandillada", display name "La PandillAda | Infancia en movimiento", handle @la_pandillada, 463 followers: instagram-cli profile/posts (author_name, follower_count), 2026-10-23.
- Bio verbatim: "Acompaño criaturas • 0-3 / Cuidado respetuoso • Máx. 4 / Salidas diarias en Cargobike / Movimiento • Juego libre / 📍El Born, BCN / 2 plazas • Dossier por DM" — author_bio from instagram-cli.
- Location El Born, Barcelona (Ciutat Vella district): bio "El Born, BCN" + tagged_location_name "Ciutat Vella, Barcelona" on posts.
- 0–3 años, máx. 4 criaturas: bio + enrollment caption.
- "2 plazas libres": posts https://www.instagram.com/p/DepKFHisWiC/ (2026-10-18) and https://www.instagram.com/p/Dd1nEP6scfN/ (2026-09-28).
- Hours 9:30–14:30; recogida en casa desde 9:15; acogida temprana desde 8:45 con contratación previa (sujeto a disponibilidad): business's own enrollment poster graphic (post DepKFHisWiC) + research JSON bio_facts.
- WhatsApp +34 678 830 419; email adarecupero@gmail.com: published in Oct 18 post caption (their own words).
- "¡Te recogemos en nuestra cargobike!"; destinations Parques / Ludotecas / Playa / Espacios del barrio; tags Juego libre / Movimiento / Vida al aire libre / Comunidad: business's own poster graphic.
- «La nave con la que recorremos la ciudad»: caption of post https://www.instagram.com/p/CpaS0yQtI1b/.
- «Somos La Pandillada»: caption of post https://www.instagram.com/p/CVdXqDuK0AG/ (hero image source).
- «A veces solo hace falta la ropa adecuada» (rain): caption https://www.instagram.com/p/DeKE2qRDL3g/.
- «Salir, explorar nuevos espacios… Jugar afuera. Moverse libremente»: caption https://www.instagram.com/p/Cz6LekZo-Za/.
- "Acompañamiento cercano y personalizado" / "tranquilo, flexible y respetuoso… autonomía y seguridad": Oct 18 enrollment caption.
- Skateboard joy: caption https://www.instagram.com/p/CW8R9BdqOoE/ ("Skateboarding always brings joy!!").
- No website at all / enrollment via DM ("Dossier por DM"): research JSON dual-check (bio links empty + web search found no official site).
- Prices: NOT published anywhere — site shows none and says "consúltanos" nowhere needed; inscription section only offers contact channels.
- No staff names used (caption signs "Ada Vilar" — deliberately omitted; site says "su acompañante").
- No invented claims about meals, curriculum, accreditations, or exact street address (none published).

## (d) Photo harvest log

Method: instagram-cli `posts --username la_pandillada` (53 own posts listed) → 12 candidate
shortcodes → public oEmbed endpoint (iPhone UA); all 12 returned `"author_name": "la_pandillada"`
(verified own content, not login-walled) → thumbnails downloaded with browser UA + Referer
(640px CDN ceiling per TOOLS.md) → converted to WebP q78 at natural size via PIL.

| Shortcode | Post URL | Used as |
|---|---|---|
| CVdXqDuK0AG | https://www.instagram.com/p/CVdXqDuK0AG/ | hero-grupo.webp |
| Cgm1XVIrqmS | https://www.instagram.com/p/Cgm1XVIrqmS/ | pandi-arbol.webp |
| CpaS0yQtI1b | https://www.instagram.com/p/CpaS0yQtI1b/ | cargobike-parque.webp |
| C5y3JdmoA3E | https://www.instagram.com/p/C5y3JdmoA3E/ | cargobike-barrio.webp |
| Dd1nEP6scfN | https://www.instagram.com/p/Dd1nEP6scfN/ | dia-playa.webp |
| DeKE2qRDL3g | https://www.instagram.com/p/DeKE2qRDL3g/ | juego-lluvia.webp |
| Cz6LekZo-Za | https://www.instagram.com/p/Cz6LekZo-Za/ | juego-tiza.webp |
| C7wFxLVIVWD | https://www.instagram.com/p/C7wFxLVIVWD/ | juego-calle.webp |
| CRlkKWLl5N6 | https://www.instagram.com/p/CRlkKWLl5N6/ | juego-verano.webp |
| CW8R9BdqOoE | https://www.instagram.com/p/CW8R9BdqOoE/ | juego-skate.webp |
| DepKFHisWiC | https://www.instagram.com/p/DepKFHisWiC/ | cartel-plazas.webp |
| DJjKAvZICKZ | https://www.instagram.com/p/DJjKAvZICKZ/ | NOT used (Catalan text-heavy book photo) |

## (e) Personalized DM draft (Devflix outreach)

> Hola 👋 Vi que anunciasteis 2 plazas libres y me encantó vuestro modelo: pocos proyectos de 0–3 salen cada día en cargobike a parques, playas y ludotecas. Eso merecería verse más allá de Instagram.
>
> Hoy toda vuestra inscripción pasa por DMs ("dossier por DM"), así que preparé una propuesta de web sencilla con vuestras fotos, horarios y canales de contacto, por si os sirve de inspiración: https://the-cut-co.pages.dev/la-pandillada-barcelona/
>
> ¿Os vendría bien tener algo así para que las familias os encuentren en Google y pidan el dossier directamente?

Why it works: one genuine observation (cargo-bike daily outings + the 2-open-spots post), the real
gap (enrollment lives entirely in DMs, zero web presence), the preview link, one low-pressure question.
No fake compliments, no invented stats, no prices mentioned.

## (f) Honest shortfalls

1. No live visual pass: no Chromium on this VM — verification was a careful CSS audit
   (breakpoints 390/760/900/1024, overflow-x hidden, nav collapse, grid stacking, per-image
   aspect-ratio frames). A real-browser check at 390/768/1440px is recommended before DMs.
2. Photos are 640px CDN ceiling (oEmbed limit) — adequate for display sizes used (≤520px), but
   not retina-sharp on large desktop. No way to get higher-res without their originals.
3. 11 visuals used (10 photos + their own enrollment poster); the Catalan book-page photo was
   deliberately excluded. Pool had ~30 own photos; videos/reels were not harvested (static site).
4. "2 plazas libres" reflects their Oct 18 post — verify it's still current before sending the DM;
   if filled, the band/poster section needs a one-line edit.
5. Copy is Spanish only (their bio mixes Catalan/Spanish); no ES/CA toggle — acceptable per brief.
6. The tick-list checkmark uses an inline SVG mask data-URI (decorative only, not a photo — no
   base64 imagery; HTML has zero base64 images).
