# ColorsLab-108 · Approved visual guidelines

Updated: 2026-11-08

## Gradient

Exactly **two hex color stops**:
```css
background: linear-gradient(110deg, #329ED8 0%, #D7F1FF 100%);
```
Color 1: rich bright deep (mid saturation). Color 2: soft luminous pastel, usually nearly white. Do **not** introduce a third color stop.

Bad example: `linear-gradient(110deg, #329ED8, #A5EAF5, #FFFFFF)` (3 colors).
Good example: `linear-gradient(110deg, #329ED8 0%, #D7F1FF 100%)`.

## Typography

- Comfortaa preferred. Fall back to system-ui/sans-serif when unavailable.
- Headings: dark ink (e.g. `#173B63` or `#172B4D`), not multicolored gradient text.
- Text: `#334155` or `#172B4D`.
- **Check actual WCAG contrast against both ends of a gradient**. A heading may need an opaque light panel if an unusually dark first stop is selected.
- Do not rely on color alone to communicate state.

## Example page elements

- Header: logo at top-right **using the approved official logo asset**; fallback is blank space, not a fabricated brand mark.
- Header: theme-relevant quote; concise, accessible.
- Hero: two-stop gradient; strong heading; 1–2 lines of introduction.
- Statistics: white/light `rgba(255,255,255,.94)` cards, border `#DDE5EC`, shadow `0 8px 24px rgba(20,50,75,.08)`.
- CTA: distinct solid blue `#1263B4`; provide visible focus, button hover state and sufficient contrast.
- Footer: “Architecting experiences for a better world.”
- No automatic music/audio; comply with reduced motion.
- Preserve page-specific country/content differentiation, rather than replacing content with a generic template.

## Responsive checklist

- 320px mobile: avoid horizontal overflow, allow cards to stack, comfortable touch targets.
- Desktop: ample whitespace, max-width around 1200px, clear hierarchy.
- Visible :focus-visible styling; keyboard navigation.
- Reduced-motion media query.
- Test text contrast in gradients, cards, and CTA.

## Dynamic country token use

```js
const entry = palettes.countryPalettes.find(p => p.name === countryName);
hero.style.background = `linear-gradient(110deg, ${entry.start} 0%, ${entry.end} 100%)`;
```

## Source and governance

- Country palette mappings here are **new deep-bright proposals**. The earlier flag-inspired mapping in the Notion deployment plan remains a separate historical reference and is not silently overwritten.
- No association is implied between a particular country palette and one of the 20 SuperLabs.
- Colors may repeat across countries as explicitly permitted.
- This repo is a design reference; publishing it does not update existing country payroll websites.

## Sample choices

| Context | Start | End |
|---|---|---|
| Arctic dashboard | `#329ED8` | `#D7F1FF` |
| Tropical mint | `#37C5C8` | `#D9FAFA` |
| Emerald learning | `#42C58D` | `#E0FAEC` |
| Violet innovation | `#9576E7` | `#EFE7FF` |
| Rose experience | `#E57CA8` | `#FFE5F0` |
| Coral action | `#F18A76` | `#FFF0E6` |
| Golden insight | `#E9B54B` | `#FFF3D1` |

## Reuse

Use `data/palettes.json` as the single maintained palette registry, while design components should read that data rather than duplicating hardcoded palettes.
