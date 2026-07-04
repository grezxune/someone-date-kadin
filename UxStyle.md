# UxStyle.md — Someone Date Kadin

The permanent visual identity for this microsite. All future changes must conform.

## Concept

**"Country Club Editorial."** A Masters-style vintage golf-club aesthetic — deep
fairway green, cream cardstock, gold foil — structured as an 18-hole scorecard
for Kadin's dating eligibility. Sincere craftsmanship carrying deadpan humor:
the design plays it straight so the copy can be funny.

## Color palette

Defined as tokens in [css/tokens.css](css/tokens.css). Never hardcode hex values in components.

| Token       | Value     | Use |
| ----------- | --------- | --- |
| `--cream`   | `#f6f1e4` | Page background, light sections |
| `--cream-2` | `#efe7d2` | Alternate light section background |
| `--green`   | `#123b2a` | Primary brand, dark sections |
| `--green-2` | `#0c2b1e` | Deepest green (finale, footer, menu overlay) |
| `--gold` / `--gold-2` | `#b8923d` / `#d8b563` | Foil accents, accents on green |
| `--rust`    | `#c4552d` | Sharp accent (eyebrows, hover, focus rings) |
| `--ink`     | `#211f1a` | Body text on light |
| `--snap`    | `#fffc00` | Snapchat CTA only — never decorative |

Dark sections use the `.theme-green` class, which re-maps the semantic slots
(`--bg`, `--fg`, `--accent`); components read only semantic tokens.

## Typography

- **Display:** Fraunces (variable serif) — headlines, scorecard caption, committee names. Italic + gold for emphasis words.
- **Body:** Instrument Sans — copy, labels, buttons.
- **Handwritten:** Caveat — photo captions and "personal note" moments only.
- Scale via `--text-*` tokens; hero uses `--text-hero` (fluid clamp).

## Signature elements

- **Hole labels:** every section opens with `HOLE N · PAR N` eyebrow + rule line.
- **Polaroid photo cards:** white matte, masking-tape accent, slight rotation (`--tilt`), Caveat caption. Hover straightens.
- **Scorecard table:** green header, cream zebra rows, italic Fraunces "par" scores.
- **Ticker marquee:** green strip, gold uppercase facts, slight rotation, ⛳ separators.
- **Rotating badge:** circular SVG text, 22s spin.
- **Paper grain:** fixed SVG-noise overlay at 5% opacity across the page.
- **Full-bleed cover:** edge-to-edge photo banner (`.cover`) with a bottom
  green scrim and a Caveat caption; used to open the ice-breaker section.
- **Breaker cards:** numbered (`№`) opener cards on off-white stock with a
  handwritten rust suggested opening line pinned to the bottom; 2×2 grid with
  photo cards placed on the diagonal.
- **Polaroid rows:** `.polaroid-row` — three staggered, alternately tilted
  photo cards (middle card dropped); used for talent exhibits and the friends
  collage.

## Motion

- Scroll reveals: fade + 26px rise, ~900ms `cubic-bezier(0.16,1,0.3,1)`, staggered via delay classes.
- Micro-interactions on buttons (lift + hard shadow) and photo cards (untilt).
- `prefers-reduced-motion` collapses all animation; reveals render visible.

## Accessibility

- WCAG 2.1 AA contrast on all text/background pairs.
- Visible rust focus rings (`:focus-visible`), semantic landmarks, alt text on every photo.
- Mobile nav: right-side overlay, `aria-expanded` toggle, Escape/outside-click to close.

## Layout rules

- Max container `72rem`; sections breathe with `--space-7` fluid padding.
- No horizontal page scroll ever (`overflow-x: clip` at root); wide tables scroll inside `.scorecard-wrap`.
- Breakpoints: single column below `56rem`, mobile nav below `48rem`.
