# CLAUDE.md — L'Amur Studija Frontend Rules

## Always Do First
- **Invoke the `frontend-design` skill** before writing any frontend code, every session, no exceptions.

## Project Context
- **Client:** L'Amur Studija — grožio salonas, Vilnius, Lithuania
- **Brand tone:** Luxury, refined, feminine. Think Paris meets Vilnius. Not flashy — understated elegance.
- **Language:** Lithuanian (UI copy), English (code comments)
- **Target audience:** Women 25–45, Vilnius, premium beauty services

## Brand Identity
- **Primary color (Gold):** `#C9A84C` — use for accents, logo, borders, hover states
- **Dark:** `#0D0D0D` — backgrounds, heavy text
- **Cream/Off-white:** `#F5F0E8` — page backgrounds, light surfaces
- **Warm grey:** `#8A8078` — body text, secondary elements
- **Logo files available in `brand_assets/`:**
  - `L-AMUR_STUDIJA_gold_Logo_WEBP.webp` — use on dark backgrounds
  - `L-AMUR_STUDIJA_black_Logo_WEBP.webp` — use on light backgrounds
  - `L-AMUR_STUDIJA_white_Logo_WEBP.webp` — use on dark/photo backgrounds
- **Typography direction:** Serif display font (e.g. Cormorant Garamond, Playfair Display) + clean sans body (e.g. Jost, DM Sans). Never use Inter, Roboto, or Arial.

## Reference Photos Available
Located in project root (uploaded by client):
- `IMG_4415.JPG` — wax/depilation service close-up (black glove, dark wax)
- `IMG_4417.JPG` — salon interior wide shot (manicure stations, warm lighting)
- `IMG_4418.jpg` — treatment room (white bed, clean spa aesthetic)
- `IMG_4426.PNG` — waiting area (grey velvet chairs, pampas grass, marble table)
- `IMG_4428.PNG` — hair wash station (dark wood, products, plants)

Use these photos as real content — do NOT replace with placehold.co when they are available.

## Design Guardrails
- **Never** use default Tailwind palette (indigo, blue, violet, etc.)
- **Never** use flat shadows. Use layered, warm-tinted shadows: `box-shadow: 0 4px 24px rgba(201,168,76,0.08), 0 1px 4px rgba(0,0,0,0.12)`
- **Gradients:** Warm, subtle. From `#F5F0E8` to `#EDE5D8`. Add SVG grain texture for depth.
- **Animations:** Only `transform` and `opacity`. Spring easing. No `transition-all`.
- **Hover states:** Every interactive element must have hover + focus-visible + active. Gold underline or glow on hover.
- **Images:** Always wrap in a container with `overflow: hidden`. Add subtle gradient overlay on hero images.
- **Spacing:** Generous. This is luxury — breathe. Use 80–120px vertical rhythm between sections.
- **Depth:** Nav floats above content. Cards elevated above page background. Use backdrop-filter blur for glass elements if needed.

## Output Defaults
- Single `index.html` unless user specifies otherwise
- All styles inline via `<style>` tag or Tailwind CDN
- Mobile-first responsive (hamburger menu on mobile)
- Google Fonts loaded via `<link>` in `<head>`

## Hard Rules
- Do not invent services, prices, or staff names — use placeholder text like `[Paslauga]`, `[Kaina]` if real data not provided
- Do not use generic AI beauty site layouts (hero with centered text + 3 feature cards = banned)
- Do not stop after one version — always offer a second pass after user feedback
- Do not use `transition-all`
- Do not use default Tailwind blue/indigo/violet as any color
- Always load brand logo from `brand_assets/` folder, never recreate it in CSS/SVG
