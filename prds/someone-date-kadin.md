---
title: Someone Date Kadin — single-page microsite
created: 2026-07-04
owner: Tommy
log:
  - 2026-07-04: Initial requirements documented and v1 shipped (full page, all four photos, Snapchat CTA, docs).
  - 2026-07-04: v1.1 — hero portrait selfie added (face visible immediately, per owner), "musician" replaces "campfire guitarist" in all copy.
  - 2026-07-04: v1.2 — ice breakers expanded to four openers (fishing trip, Florida chapter with glowing water, Texas→Vietnam travel, family board games) under a full-bleed paddleboard cover photo.
  - 2026-07-04: v1.3 — missing-club, driver-swing, and kayak photos added; walks-the-course fact corrected (no cart); "too nice" ticker line cut and ticker loop fixed; hero seal moved off the portrait; Snap handle removed from CTA buttons.
  - 2026-07-04: v1.4 — Talents section added (guitar / pool winnings / practice net); rocket-launch ice breaker №5; friends section rebuilt as a three-photo collage with Tommy plug and "webmaster" removed per owner.
---

# Someone Date Kadin

## Problem

Kadin Hayakawa — golfer, pool player, guitarist/singer, and one of the most
caring people his friends and family know — is single. His best friend Tommy
is commissioning a world-class, hilarious-but-sincere one-page microsite to
introduce him to prospective girlfriends and route them to his Snapchat.

## Business Context

Personal project under Grez Studios. Zero budget, zero backend, maximum love.
Success is measured in Snapchat adds and laughs per scroll.

## Goals & KPIs

- A visually world-class single page that feels designed, not templated.
- Humor that is genuine and kind — never rude, never at Kadin's expense in a mean way.
- Primary conversion: Snapchat add of `nidak.1999` (Snapchat-branded CTA, top and bottom).

## Personas / Journeys

- **The Prospect:** lands via shared link, laughs, learns Kadin is a catch, taps the Snapchat CTA.
- **The Friend-of-a-Friend:** forwards the link to someone who'd be perfect for him.

## Functional Requirements

1. Single static page, no backend, no forms.
2. Hero with headline + Snapchat CTA (brand yellow `#FFFC00`, ghost mark, handle `nidak.1999`, links to `snapchat.com/add/nidak.1999`).
3. Golf section using the bar/hoodie photo — he runs 18 Birdies social media and films golf videos; the hoodie roasting golf shows self-awareness.
4. Ice-breaker section using the fallen-tree photo — teases last summer's fishing trip where he almost died; positioned as a first-message opener, story deliberately unspoiled.
5. Legal-style disclaimer with the baby photo — prop baby "Ashem" does NOT come with Kadin and is not his property.
6. ~~Approval committee roster~~ — removed entirely per owner directive 2026-07-04. Family names (David, Sara, Keston, Kyla, Ben) no longer appear on the page.
7. Friends section with a three-photo collage of Kadin's crew (beach nights, pool league). Owner directive 2026-07-04: no Tommy self-plug copy, and the term "webmaster" is banned site-wide.
8. Mentions of secondary hobbies: pool (billiards), guitar, singing.

## Non-functional Requirements

- Fully responsive (mobile → desktop), accessible mobile nav overlay.
- WCAG 2.1 AA contrast, keyboard navigation, reduced-motion support.
- No horizontal page scrolling; wide tables scroll in their own container.
- Conforms to [UxStyle.md](../UxStyle.md) ("Country Club Editorial").

## Data & Integrations

- Static assets only. Photos resized to 1400px max, quality 82 (`assets/images/`).
- Google Fonts (Fraunces, Instrument Sans, Caveat). Sole external dependency.
- Outbound link to Snapchat add URL. No analytics, no cookies, no data collection.

## Security Architecture & Threat Model

- No backend, no forms, no user input, no secrets → attack surface is effectively nil.
- Only external link uses `rel="noopener"`; only third-party origin is Google Fonts.
- No PII collected. Content published with the subjects' knowledge via the site owner.

## Performance Strategy & Budgets

- Budget: < 1.8MB total transfer, LCP < 2.5s on 4G, CLS ≈ 0.
- Images lazy-loaded below the fold and pre-compressed (~350–650KB each).
- No JS frameworks; ~60 lines of vanilla JS, CSS-only animation elsewhere.

## Architecture Notes & Exceptions

- Global stack defaults (Next.js/Auth.js/Convex) intentionally waived: the owner
  specified a one-page static site with no backend or forms. Plain HTML/CSS/JS
  is the simplest correct architecture and deploys anywhere.
- `index.html` exceeds the 200-line file target: it is a single cohesive
  document (one page = one file); CSS and JS are split into focused modules.

## Open Questions

- Custom domain + hosting target (Vercel? GitHub Pages?) — deploy when Tommy decides.
- OG image should become an absolute URL once the domain exists.

## Risks & Mitigations

- **Risk:** Kadin objects to a joke. **Mitigation:** all humor is affectionate; copy is easily editable in one file.
- **Risk:** Snap handle changes. **Mitigation:** handle appears in three CTAs — search `nidak.1999`.

## Success Metrics

- Kadin laughs. The committee approves. At least one quality Snapchat add.

## Rollout Plan

1. ✅ v1 build verified locally (desktop + mobile screenshots, console/network clean).
2. Share with the approval committee for copy sign-off.
3. Deploy to static hosting; set absolute OG image URL.

## Next Steps

- Decide hosting/domain, then run deployment.
