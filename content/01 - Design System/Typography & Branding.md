# Typography & Branding

## Type hierarchy
- **Project wordmark:** Orbitron or a licensed Space-Age/stencil font that is supplied with the project. Use a sensible fallback.
- **UI / body:** Inter, system sans-serif.
- **Technical labels / code:** JetBrains Mono.
- **Headings:** compact, confident, readable; avoid using the decorative wordmark font for paragraphs or form labels.

## Suggested CSS
```css
:root {
  --font-ui: "Inter", ui-sans-serif, system-ui, -apple-system, sans-serif;
  --font-brand: "Orbitron", "Rajdhani", var(--font-ui);
  --font-mono: "JetBrains Mono", ui-monospace, monospace;
}
body { font-family: var(--font-ui); }
.project-wordmark { font-family: var(--font-brand); letter-spacing: .08em; }
code, pre, .technical-label { font-family: var(--font-mono); }
```

## Center-to-header title motion
- On first page load, type the project title in the center.
- After typing, transition it to the header's top-left anchor.
- Keep the final title in normal header layout after the transition; do not leave an invisible overlay covering controls.
- Use measured layout/FLIP animation or a shared layout animation in the chosen framework rather than relying on a fixed viewport coordinate that breaks on mobile.
- Respect `prefers-reduced-motion`; provide a no-animation path.
- Play once per navigation/session where appropriate, not on every small state update.

## Brand footer
Layout: `— [SJAH emblem] A Project of SJAH —`

Use the real supplied emblem asset. Keep the original logo proportions; don't distort, crop, recolor, or place a dark-background-only logo on a light surface without testing. Use an accessible alt description.

## Asset manifest
| Asset | Expected location | Status |
|---|---|---|
| “Let’s Go..” cat | `05 - Assets/cat-lets-go.png` | Included |
| SJAH emblem | `05 - Assets/sjah-emblem.png` | Add original asset |
| AI assistant mascot/mark | `05 - Assets/sjah-ai-mascot.svg` or `.png` | Add approved asset |
| Favicon / app icon | project `public/` directory | Generate from approved brand mark |
