# BUILD NOTES — Sadi Rasoi Tiffin Service (sadi-rasoi-tiffin)

Business: Sadi Rasoi Tiffin Service · IG @sadirasoi_ (author_id 17841435633074469)
Location: Walsall / Wolverhampton / Birmingham, West Midlands, England, UK — homemade Punjabi tiffin service
Built: 22 Oct 2026 (morning batch, UK build)

## 1. FACT SOURCES (all business-published, nothing invented)

- **Research brief**: `~/workspace/instagram/lead-campaign/research/batch-morning-22oct-UKIE.json` (qualified entry for sadirasoi_) — name, handle, author_id, ~82 followers, service areas (Walsall/Wolverhampton/Birmingham), phone 07367281459 (published in 2026-09-16 caption), ordering via IG DM, weekly tiffin menus, takeout & delivery, "tiffin services on affordable prices".
- **Visual inspection of their own IG graphics** (6 posts downloaded 22 Oct 2026 from the brief's CDN URLs, all HTTP 200): weekly-menu posters dated 18–23 Oct 2026, 11–16 Oct 2026, 04–10 Oct 2026, plus two undated. Poster text confirms:
  - "Ghar Jaisa Khana, Har Din" (tagline)
  - "Fresh Homemade Vegetarian Food", "Veg Only", "Fresh Healthy Homemade"
  - "Every Tiffin Includes": fresh homemade-style vegetarian food, hygienically prepared meals, freshly prepared rotis, dal or curry with sabzi, rice as listed, fresh salad, raita or curd as listed
  - "Good Food Brings People Together"
  - Phone 07367281459 and Instagram sadirasoi_ printed on every poster
  - Dessert examples: sweet yellow rice (jarda) with dahi bhalla, seviya, kheer, moong daal halwa, fruit custard
- **NOT published / absent (marked as such on the site, never invented):** prices, opening hours, street address.

## 2. IMAGE-FIT AUDIT (per-image)

All 6 photos are the business's own portrait Instagram menu/info posters (3072x4096 except one 1024x1360). Converted to WebP q78: hero 1024w (198 KB), menus 1100w (154–226 KB each). No base64 anywhere; width/height attrs on every img; lazy-load below the fold; hero uses fetchpriority=high.

| Image | Role | Fit treatment |
|---|---|---|
| hero.webp ("Every tiffin includes" poster) | Hero, right column, max-width 380px (≤ ~505px tall, under the ~560px hero cap) | Full-view, intrinsic portrait ratio preserved (height auto), no crop. Caption notes it's from their own poster. |
| menu-1.webp … menu-5.webp (5 weekly-menu posters) | "Weekly menus" gallery grid (1 col mobile / 2 col ≥640px / 3 col ≥1000px) | Full-view, intrinsic ratio preserved; cards are height-auto so no text clipping. Captions identify which week's menu each is. |
| object-position | Not needed — no cover-cropping anywhere on this site; every image shows in full. |

## 3. CONTRAST TABLE (computed, WCAG AA)

Palette: cream #FAF3E3, paper #FFFDF6, ink #3B2D1F, deep green #1C5B38, mustard #E9B949, dark brown #2C2117, white #FFFFFF.

| Foreground → Background | Ratio | Requirement | Result |
|---|---|---|---|
| Ink #3B2D1F on cream #FAF3E3 (body) | 12.01:1 | 4.5:1 | PASS |
| Green #1C5B38 on cream #FAF3E3 (headings) | 7.30:1 | 3.0 large / 4.5 normal | PASS |
| White #FFFFFF on green #1C5B38 (buttons/nav) | 8.07:1 | 4.5:1 | PASS |
| Ink #2C2117 on mustard #E9B949 (badges/eyebrow) | 8.60:1 | 4.5:1 | PASS |
| Green #1C5B38 on white #FFFFFF (buttons) | 8.07:1 | 4.5:1 | PASS |
| Cream #FAF3E3 on dark brown #2C2117 (footer text) | 14.21:1 | 4.5:1 | PASS |
| Mustard #E9B949 on dark brown #2C2117 (footer headings) | 8.60:1 | 3.0 large | PASS |
| Pale cream #F4EAD2 on green #1C5B38 (areas sub-text) | 6.74:1 | 4.5:1 | PASS |

Note: earlier pass — the area-card body text was set at a lighter tint; verified against the final #F4EAD2 on #1C5B38 pair.

## 4. RESPONSIVE CHECK

- Mobile-first; nav links collapse to wordmark + Call button on small screens (no overflow).
- Hero stacks (text above image, image centered max 340–380px) — no horizontal overflow; hero under the ~560px desktop cap.
- Menu gallery: 1/2/3 columns at 390/768/1440 breakpoints; images height-auto so posters never clip text.
- All text remains readable without JS (reveal gated behind `.js`, content visible by default); `prefers-reduced-motion` disables the reveal transition.
- Verified: no base64, no horizontal scroll triggers (grid + max-width containers only). Not viewable in a live browser from this subagent — parent batch will verify the deployed URL before DM.

## 5. SECTIONS / COPY

Sticky nav · Hero (name, "homemade Punjabi tiffin across Walsall/Wolverhampton/Birmingham", tap-to-call 07367281459, IG link) · Every tiffin includes (checklist from their poster) · Weekly menus (5 recent menus as published) · How it works (menu on IG → DM/call order → takeout/delivery; facts only) · Service areas (Walsall/Wolverhampton/Birmingham cards) · Contact (phone, Instagram, honest "hours not published / prices confirmed when you order" notes) · Footer + "Preview concept by Devflix". Copy is warm, short, honest — no invented prices, reviews, or delivery claims.

## 6. DM DRAFT (for the parent batch; channel: Instagram DM to author_id 17841435633074469)

> Hi! I came across @sadirasoi_ and love how much thought goes into your weekly menus — a proper Friday dessert each week is such a nice touch. One thing I noticed: all of that only lives in Instagram posts, so new customers in Walsall or Birmingham can't find Sadi Rasoi on Google at all. I made a quick preview of what a simple one-page website for you could look like: [PREVIEW LINK]. Would something like this be useful for taking orders?

Short, natural, one genuine observation (weekly menus buried in posts / Friday dessert touch), why it helps THEM (Google findability), verified preview link, one low-pressure question. No fake compliments, no invented stats, no spam wording.
