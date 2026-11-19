# Lili's homepage mockup — design doc

## Files
- `design/Main.dc.html`: the whole homepage as one Design Component artboard. It is a fluid
  page with `expand: fill` and a 1440px preview. Inline styles throughout, with one `accent` tweak prop.
- `design/canvas.json`: the canvas index. It has one board and launches focused on Main.
- These are copies of what is published to the canvas. **The canvas is the source of
  truth**, and someone may have edited it by hand there. Before changing anything, read the
  live canvas with Artifact `read` and the file's `path`, then republish to the same URL with `root`
  set to a folder that holds `project/Main.dc.html` and `project/canvas.json`.

## Images
The images were uploaded to the canvas's asset store and are referenced by `/_blob/<id>` URLs in
Main.dc.html. Originals are from the restaurant's own site under
`https://www.lilisbraziliansteakhouse.com/wp-content/uploads/`. Not committed here
because they are the restaurant's photos.

| Blob id | Original | Used in |
|---|---|---|
| af8301b2… | 2026/09/logo-horizontal-768x384.png (transparent) | nav, footer |
| 6e53d425… | 2024/04/lilis-brazilian-steakhouse-logo.png (round badge) | uploaded, unused |
| 08d9a344… | 2025/09/home-slider.webp (steak plate) | hero |
| dcd948e3… | 2026/11/restaurant-interior.jpg (table + guitarist) | Steakhouse section |
| d37d59b9… | 2025/08/Lili-12-2-1-scaled.jpg (guest at buffet) | Private events |
| 2046b8b7… | 2026/11/home-diningroom.jpg | Visit section |

The site blocks curl's default user agent with a 406. Fetch with a browser User-Agent header.

## Visual system: "Festa"
The goal was less regal and more vibrant Brazilian. The current site is gold on cream with
floral corners and serif headings, which feels formal.

- **Colors**
  - Deep green `#0B5D33` is the ground. It is pulled from the restaurant's real green walls.
  - Sunshine yellow `#FFD23F` echoes their mustard napkins and the Brazilian flag.
  - Flag blue `#12307A` is for the Steakhouse section.
  - Coral `#FF7A6B` is the `accent` tweak. Pink, orange and turquoise are offered as alternatives.
  - Turquoise `#3CC6B8`, leaf green `#7BD389`, and a cream page `#FFF6E5`.
  - Text on colored blocks is ink `#1B1B1B`. White on coral fails contrast, so it is not used.
- **Type**
  - Bricolage Grotesque 800 for headings. It is chunky and friendly, which replaces the regal serif.
  - DM Sans for body text at 18–21px.
  - Caveat for short handwritten Portuguese lines (*Bem-vindos!*, *Sabor do Brasil*, *Festas & eventos*, *O que dizem*, *Vem com a gente*). They are small accents, never body text.
- **Motifs**
  - Copacabana *calçadão* waves: an inline SVG pattern used as faint waves in the hero and as two full-width bands (black/cream and yellow/green).
  - Wavy section edges.
  - Arched photo frames with an offset colored shape behind them.
  - A rotated round "feito com AMOR" sticker.
  - Slightly tilted testimonial cards.
- **Components:** one pill shape for every button and label (≥56px tall for buttons), and one card family (32px radius, flat color fills, no borders or shadows except the dashed drinks strip).
- **Accessibility, matching Bill's audience rules:** tap targets ≥56px, body text ≥18px, plain English copy with Portuguese only as decoration, and real `<a>`/`<button>` elements.

## Section order
1. Announcement strip
2. Nav
3. Hero
4. Taste of Brazil: four dish cards plus a drinks strip
5. Calçadão band
6. Steakhouse Night (blue)
7. Private events
8. Takeout band (yellow)
9. Testimonials
10. Visit (hours, location, photo)
11. Calçadão band
12. Footer

## Content I wrote that isn't on their site (needs owner review)
- The one-line dish descriptions are general descriptions of each dish.
- "Live music & good company" is inferred only from the guitarist in their photo.
- The hero headline and the section headlines are new. The body copy is adapted from theirs.
