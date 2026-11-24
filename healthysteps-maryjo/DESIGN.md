# Healthy Steps demo — design doc

## Files
- `public/healthysteps/index.html` (repo root) — the whole page, a standalone HTML doc, no JS.
  Served at demos.parnellprojects.com/healthysteps/.
- `public/healthysteps/img/` — resized copies of photos from her site (committed; repo is private). Originals live under
  `https://healthysteps-maryjo.com/wp-content/uploads/`:

| File | Original |
|---|---|
| class-lakeside.jpg | 2024/06/Jeri-Laura.png (hero, Lakeside Pavilion class) |
| zoom-teaparty.jpg | 2024/03/teaparty-edit-2.png |
| zoom-class.jpg | 2021/01/class-students.jpg |
| zoom-birthday.jpg | 2021/08/laughing.png |
| custard-tart.jpg | 2022/09/Screen-Shot-2022-09-19-at-9.57.10-AM.png (her cat) |
| mary-jo.jpg | 2023/01/MaryJo.png (216px only) |
| dance-floor.jpg | 2026/01/IMG_0786a.jpg (216px only) |

The homepage slider images are stock with text baked in; deliberately not used.

## Visual system
- Teal `#0D6B66` (trust, calm) + marigold `#F5B43A` for every "join" action; rose for eyebrows.
  Full dark-mode token set.
- Outfit (headings, 800) + Lexend (body, 19px; designed for readability).
- One button family (pill, 60px tall), one pill/badge family, one card family (22px radius, 1px line).
- Every `<img>` has `height: auto`; without it the width/height attributes beat `aspect-ratio` and photos stretch tall on phones.
- Audience is older: body ≥19px, buttons ≥56px, plain copy, phone number in the header.

## Section order
Demo strip → header (name + call) → hero → Classes (4 cards) → What is Healthy Steps →
Meet Mary Jo → Kind words (4 quotes) → Recent photos (Facebook slot) → Contact (teal) → footer
