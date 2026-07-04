# Someone Date Kadin ⛳

A one-page, zero-backend microsite dedicated to a single mission: getting
Kadin Hayakawa a girlfriend. Hilarious on purpose, sincere underneath —
built with love by his best friend.

**Live behavior:** scroll the 18-hole "eligibility scorecard," meet the
approval committee, learn the ice-breaker, and add him on Snapchat
(`nidak.1999`) via the yellow CTA.

## Stack

Deliberately boring: hand-written HTML + CSS + ~60 lines of vanilla JS.
No build step, no framework, no data collection. Deploys to any static host.

## Run locally

```sh
python3 -m http.server 4173
# open http://localhost:4173
```

## Structure

```
index.html          # the entire page (single cohesive document)
css/tokens.css      # design tokens — colors, type, spacing, motion
css/base.css        # reset, typography, layout primitives, reveals
css/components.css  # nav, buttons, photo cards, scorecard, committee
css/sections.css    # hero, splits, finale, footer
js/main.js          # scroll reveals + mobile menu (progressive enhancement)
assets/images/      # optimized photos (1400px max)
prds/               # product requirements
UxStyle.md          # permanent visual identity — read before changing UI
```

## Editing rules

- Design changes must follow [UxStyle.md](UxStyle.md).
- Colors/type/spacing only via tokens in [css/tokens.css](css/tokens.css).
- The Snapchat handle appears in three CTAs — search `nidak.1999` to update all.
