# ColorsLab-108 — SuccessLabs Academy Color Design System

**Architecting experiences for a better world.**

ColorsLab-108 is the reusable visual-design reference for SuccessLabs Academy's interactive HTML workbooks, Product Innovation Labs, global payroll pages, digital checklists and other learning experiences.

## Latest agreed standards (8 November 2026)

1. **Exactly TWO colors per gradient** — no middle color stops, no rainbow headings.
2. **Rich, bright first stop → luminous pastel second stop.** Colorful enough to feel deep but never visually heavy or muddy.
3. **Standard direction:** `linear-gradient(110deg, var(--gradient-start) 0%, var(--gradient-end) 100%)`.
4. Use **Comfortaa** for headings and the user interface; include a sensible local fallback.
5. Use dark, accessible heading and body colors rather than gradient-colored headline letters. Verify contrast for real text.
6. Use white or near-white cards, gentle borders, subtle shadows and generous whitespace.
7. Reserve strong blue or teal for accessible buttons and interactive controls; ensure focus indicators and hover states.
8. Keep the SuccessLabs Academy **official logo top-right** when its approved asset is available; never fabricate a replacement logo or replace it with text.
9. Use a meaningful, theme-relevant quote in the central header and the mission statement in the footer.
10. No background audio by default. Respect reduced-motion preferences and mobile responsiveness.
11. **Country palettes are a design proposal, not official flag colors.** Countries may repeat palette colors. This registry is independent of SuperLab mapping.
12. Preserve country-specific content: the visual theme must not homogenize payroll configuration or other local learning material.

## Files

| File | Purpose |
|---|---|
| [index.html](index.html) | Interactive visual catalogue, live page previews, search, country filtering and copyable CSS |
| [data/palettes.json](data/palettes.json) | Machine-readable country registry and 100 richer studio gradient choices |
| [standards/COLOR-GUIDELINES.md](standards/COLOR-GUIDELINES.md) | Design tokens, examples, accessibility and implementation rules |
| [examples/hero-example.html](examples/hero-example.html) | Copy-and-adapt single-HTML demo |

**Explore on GitHub Pages:** https://nbnayak88.github.io/ColorsLab-108/ (requires GitHub Pages to be enabled under repository Settings → Pages → Deploy from a branch → main / root).

### Quick CSS example

```css
:root {
  --gradient-start: #329ED8;
  --gradient-end: #D7F1FF;
}
.hero {
  background: linear-gradient(110deg, var(--gradient-start) 0%, var(--gradient-end) 100%);
  color: #173B63;
}
```

**Registry scope:** 195 country color mappings and 100 studio gradients. These are curated proposed palettes, not a verified global country or jurisdiction taxonomy.

© SuccessLabs Academy — visual system reference.
