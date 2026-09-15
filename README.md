# bestmortgageratesslough — Landing Page

## Files
- `index.html` — the full landing page (design + SEO article, self-contained)
- `robots.txt` — allows all crawlers, points to the sitemap
- `sitemap.xml` — single-URL sitemap for the homepage
- `README.md` — this file

## What was built
- **Design:** Cinematic, dark-luxury Awwwards-style layout. Fraunces (serif display) +
  Inter (body). Deep charcoal background with brass/gold and deep-teal accents,
  glassmorphism cards, animated gradient hero, parallax image bands, sticky
  translucent nav, magnetic buttons, subtle 3D card tilt.
- **Animation:** GSAP + ScrollTrigger (loaded from cdnjs, no build step needed).
  Hero text reveals line-by-line on load; sections fade/rise into view on scroll;
  hero and mid-page images parallax; cards tilt on hover; buttons have a magnetic
  hover pull. `prefers-reduced-motion` is respected.
- **Content:** 1000+ word semantically structured article (`<article>`, one `<h1>`,
  multiple `<h2>`/`<h3>`) targeting **"Commercial mortgage broker Slough"**.
  The anchor text **"Mortgage broker in Slough"** appears exactly once, in the
  **second paragraph**, linking to `https://www.cubicfinancial.com/` — no other
  links to that domain appear anywhere else on the page, as requested.
- **No phone number or call button** anywhere on the page, as requested.
- Basic on-page SEO: title tag, meta description, canonical tag, Open Graph tags,
  and `FinancialService` JSON-LD schema.
- Images are hotlinked from Unsplash for the demo — replace with your own
  licensed/optimized images before going live (see below).

## Before going live
1. **Domain:** `robots.txt`, `sitemap.xml`, and the canonical/OG tags in
   `index.html` currently use `https://www.bestmortgageratesslough.com/` as a
   placeholder. Replace this with your real domain everywhere it appears.
2. **Images:** swap the Unsplash URLs in `index.html` for your own compressed,
   licensed images (ideally WebP/AVIF) to keep load times fast.
3. **Compliance copy:** the footer line about FCA regulation is a generic
   placeholder — replace with wording that accurately reflects your actual
   regulatory status.
4. **Contact route:** the "Enquire" / "Start the conversation" buttons currently
   scroll to an on-page anchor (`#contact`). Point them at a real contact form,
   email link, or booking tool when you're ready — no phone number or call
   button was added, per your instructions.
5. Run the page through PageSpeed Insights / Lighthouse after swapping in real
   images, and test on a real mobile device.

## Notes
- Single HTML file, no build tools or dependencies to install — just upload
  `index.html`, `robots.txt`, and `sitemap.xml` to your web root.
- GSAP is loaded via CDN (cdnjs). If you need the site to work fully offline,
  download `gsap.min.js` and `ScrollTrigger.min.js` and reference them locally.
