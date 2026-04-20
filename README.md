# Style Stage - Project 1

**Student:** Vrushil Panchal |
**Student Number:** 200628377 |
**Course:** COMP1054 |
**Date:** April 2026 

---

## Project Overview

This is my CSS-only redesign of the [Style Stage](https://stylestage.dev/) challenge page.
Style Stage is a modern take on the classic CSS Zen Garden — the HTML cannot be changed,
only CSS is used to create a completely different visual design.

---

## Live Site

[View on GitHub Pages](https://vrushilpanchal02.github.io/Project-1-CSS/)

---

## Repository

[View on GitHub](https://github.com/VrushiLpanchal02/Project-1-CSS.git)

---

## Design Choices

### Colour Scheme
I went with a dark navy theme because I wanted the page to feel
modern and clean. The electric blue accents and glowing header
give it a tech feel which fits the CSS/coding subject of the page.
I used a teal-tinted diagonal stripe pattern in the contribute
section and a glowing blue radial gradient in the header to add
some visual interest without being too distracting.

| Colour | Hex | Used For |
|---|---|---|
| Deep Navy | `#0d1b2a` | Page background |
| Navy Alt | `#112236` | Header, guidelines, footer background |
| Surface | `#162840` | Cards, blockquote, files box |
| Border | `#1e3a55` | Card borders and dividers |
| Electric Blue | `#4fc3f7` | Headings, links, buttons, accents |
| Soft Teal | `#80cbc4` | Secondary accents, h2, profile |
| Warm Gold | `#ffd54f` | H3 headings, hover highlights |
| Off White | `#e8f1fa` | Body text |
| Muted Blue | `#8aadcc` | Subdued text, nav subtitle |

### Special Colour Effects
- **Header glow** — `radial-gradient` with `rgba(8, 52, 246, 0.323)` blue glow on the left
  and a soft teal glow on the right
- **Header h1 box shadow** — `0 0 30px rgba(79, 194, 247, 0.663)` electric blue outer glow
- **Nav hover** — `rgba(15, 84, 222, 0.273)` blue tint background,
  `rgba(3, 224, 95, 0.3)` green-tinted border
- **Contribute stripes** — `rgba(79, 247, 208, 0.33)` teal stripe
  with `rgba(113, 79, 247, 0.04)` soft purple base
- **Features card inner span** — `rgba(74, 224, 171, 0.08)` subtle green tint

### Fonts
- **Outfit** (Google Fonts) — used for all headings. Bold and clean.
- **Inter** (Google Fonts) — used for body text. Very readable at small sizes.

Both fonts are loaded via `@import` from Google Fonts.

### Layout Strategy
- Mobile first — default styles work on small screens
- CSS Grid used for the features list and footer links
- Flexbox used for the header, nav, and profile section
- `auto-fit` with `minmax()` so the features grid adapts
  automatically to screen width without lots of breakpoints

### Breakpoints
| Width | Layout Change |
|---|---|
| max 400px | Smaller padding, smaller nav font |
| min 768px | Wider header, 2+ col features grid |
| min 1024px | 3 column features, wider container |
| min 1200px | Larger nav spacing |
| min 180ch | Profile card fixed to bottom-right corner |

---

## CSS Techniques Used

- CSS custom properties (variables) for all colours and spacing
- `clamp()` for fluid responsive font sizes
- CSS Grid with `repeat(auto-fit, minmax())` for responsive cards
- Flexbox for nav, header, and profile layouts
- `radial-gradient` for the header background glow effect
- `background-clip: text` for gradient text on guidelines headings
- `repeating-linear-gradient` for the diagonal stripe in #contribute
- `scroll-behavior: smooth` for smooth anchor navigation
- `prefers-reduced-motion` media query for accessibility
- Attribute selector `[class^="link"]` to style all link variants
- `:nth-child`, `:nth-of-type`, `:nth-last-child` for targeted styling
- `::before` pseudo-element for the footer S logo mark
- CSS transitions on hover/focus for interactive feel
- Stretch link technique using `::before` on feature card links

---

## Accessibility Notes

- Skip link included and shows on keyboard focus
- All interactive elements have visible `:focus` styles
- `prefers-reduced-motion` respected — all animations disabled for users who prefer it
- `#files h3` visually hidden but still readable by screen readers

---

## File Structure
