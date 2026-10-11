# Responsive Layout & Spacing

## Layout principles
- Spacious, Gemini-inspired composition without copying proprietary branding or exact screens.
- Content max-width around 1200px; center long-form content.
- Consistent vertical rhythm and predictable card spacing.
- Keep primary actions visually distinct and near the content they affect.

## Spacing scale
| Token | Value |
|---|---:|
| `space-1` | 4px |
| `space-2` | 8px |
| `space-3` | 12px |
| `space-4` | 16px |
| `space-5` | 20px |
| `space-6` | 24px |
| `space-8` | 32px |
| `space-10` | 40px |
| `space-12` | 48px |
| `space-16` | 64px |

## Responsive behavior
- Mobile first; test at 320px, 375px, 768px, 1024px, and wide desktop.
- Under 768px, use a full-height overlay drawer rather than a narrow persistent sidebar.
- Auth forms stack vertically on phones; desktop may use a split-panel layout.
- Buttons and inputs should have comfortable touch targets (aim for 44×44 CSS px).
- Avoid horizontal overflow; long project names should truncate gracefully or wrap intentionally.
- Respect safe-area insets on mobile devices.
- Footer lines should shrink or disappear at very narrow widths while the brand lockup remains centered.
