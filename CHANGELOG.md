# Changelog

## 2026-07-04 — v1.9.0

- Added Vercel Web Analytics (no-framework script snippet, since this is a
  plain static site with no build step/package.json). Requires enabling
  Web Analytics for the project in the Vercel dashboard (Project → Analytics
  → Enable) to actually start collecting data.

## 2026-07-04 — v1.8.0

- Added a surfboard/beach photo to ice breaker №4, "Board game night," per
  owner's explicit direction (photo depicts surfing, not board games —
  flagged before applying).

## 2026-07-04 — v1.7.2

- Removed the leftover "A public service announcement" eyebrow from the
  OG/social share image template (it was cut from the live page earlier
  but missed in the card); image regenerated.

## 2026-07-04 — v1.7.1

- Canonical domain is now someonedatekadin.com: canonical link, og:url, and
  all og/twitter image URLs updated.
- Social share image regenerated (crisp 2× headless-Chrome render): shows
  someonedatekadin.com instead of the vercel.app URL and the updated
  "Someone (normal), please, date Kadin." headline; og/twitter titles and
  alts synced to match.

## 2026-07-04 — v1.7.0

- Guitar exhibit replaced with the wedding performance photo (vest, tie,
  microphone); caption updated to match.
- Blue "if golf was easy" hoodie photo removed entirely; golf section now
  runs a single swing polaroid and the hoodie copy was rewritten.
- Hero headline is now "Someone (normal), please, date Kadin." and the
  "public service announcement" eyebrow line was removed.
- Spinning seal text now uses SVG textLength so the dots space evenly
  around the circle (no more gap after "Included").

## 2026-07-04 — v1.6.1

- Vietnam summit photo (flag on the peak) added to ice breaker №3,
  "The long way around."

## 2026-07-04 — v1.6.0

- Approval committee section removed entirely per owner. Nav link replaced
  with "The Crew" (points to the friends section); ice-breaker and finale
  copy updated to drop committee references. Footer "Committee to Date
  Kadin" campaign-name joke retained.

## 2026-07-04 — v1.5.0

- Dedicated 1200×630 social share image (`assets/images/og-cover.jpg`),
  matching the site's design system — headline, hero polaroid, and a
  "Certified Single · Swing Included" badge. Source template lives at
  `assets/og/og-card.html` for future edits.
- Full Open Graph + Twitter Card meta tag set added: `og:site_name`,
  `og:url`, `og:image` (with `secure_url`/`type`/`width`/`height`/`alt`),
  `og:locale`, `twitter:card=summary_large_image` plus title/description/
  image/alt, canonical link, and `theme-color`. All image/URL tags use
  absolute production URLs (`https://someone-date-kadin.vercel.app`).

## 2026-07-04 — v1.4.1

- Name corrections: Keston (brother), Sara (mother).
- Footer simplified to "Built with love by Tommy." and now links to
  tommytreb.com.
- Finale eyebrow "Hole 18 · The 19th Hole" clarified to "Hole 18 · The Final Hole".

## 2026-07-04 — v1.4.0

- New "Talents, documented" section (Hole 5): three-polaroid exhibit row —
  guitar in the car, pool winnings with a $20, backyard practice-net session.
- New ice breaker №5, "The rocket launches" (Cape Canaveral beach photo);
  breaker grid reflowed to 2×2 with photo cards on the diagonal.
- Friends section rebuilt as a three-photo scrapbook collage of Kadin's crew;
  Tommy self-plug copy and the rafters photo removed, and the word
  "webmaster" is retired site-wide (committee role now "Built this very website").
- Shared `.polaroid-row` component for staggered three-photo rows.

## 2026-07-04 — v1.3.0

- Three new photos: the missing-club tee-box shot (scorecard section, captioned
  "unsure where his club just went"), a driver-swing action shot (golf section,
  now a two-photo stack with the hoodie polaroid), and a kayak photo on the
  Florida ice-breaker card.
- Ticker rebuilt as two identical groups for a seamless loop; "Handicap: being
  too nice" removed and "Will drive the cart" corrected to "Walks the course —
  never takes a cart" (also reflected in golf section copy).
- "Certified Single" seal moved out of the hero photo — now sits in flow below
  the CTA buttons, never overlapping the portrait.
- Snapchat CTA buttons now read "Add Him on Snapchat" (handle removed).

## 2026-07-04 — v1.2.0

- Ice breaker section expanded into "Never run out of openers": a full-bleed
  dusk cover photo (`kadin-water.jpg`, paddleboarding in Florida) with a
  glowing-water caption, the fishing-trip story as Opener №1, and a new
  three-card menu — №2 The Florida chapter (six months of golfing/surfing,
  bioluminescent water), №3 The long way around (Texas with his cousin, then
  ~8 months in Vietnam), №4 Board game night with the Hayakawa family.
- New components: `.cover` full-bleed banner with scrim, `.breaker-card` grid.

## 2026-07-04 — v1.1.0

- Hero redesigned as a two-column layout with Kadin's portrait selfie
  (`kadin-hero.jpg`) in a polaroid card — his face is the first thing visible
  on both desktop and mobile (photo ordered first on small screens).
- Rotating "Certified Single" badge now anchors to the hero photo's corner.
- Copy: "campfire guitarist" → "genuinely great musician" (hero, meta tags,
  scorecard music row); OG image now the hero portrait.

## 2026-07-04 — v1.0.0

- Initial release of the Someone Date Kadin microsite.
- "Country Club Editorial" design system (see `UxStyle.md`): fairway green /
  cream / gold palette, Fraunces + Instrument Sans + Caveat type, paper grain,
  polaroid photo cards, rotating badge, ticker marquee.
- Sections: hero PSA, eligibility scorecard, The Golf Thing (18 Birdies),
  fishing-trip ice breaker, prop-baby legal disclaimer (Ashem), approval
  committee roster, friends feature, Hole 18 Snapchat finale, footer.
- Three Snapchat-branded CTAs linking to `snapchat.com/add/nidak.1999`.
- Responsive layout with accessible right-side mobile menu overlay,
  reduced-motion support, lazy-loaded optimized images.
- Verified locally: desktop + mobile screenshots, zero console errors,
  zero failed requests, no horizontal page scroll.
