# Design Tokens

## Theme palettes

### Dark mode
| Token | Value | Use |
|---|---|---|
| `--bg-primary` | `#0D0B18` | Main background |
| `--bg-elevated` | `#120F24` | Sidebar / elevated regions |
| `--surface` | `#181528` | Cards and dialogs |
| `--surface-soft` | `#211D38` | Hover / secondary surfaces |
| `--text-primary` | `#FFFFFF` | Main text |
| `--text-secondary` | `#A7A5BC` | Secondary text |
| `--border` | `rgba(255,255,255,.12)` | Dividers and outlines |
| `--accent-blue` | `#2563EB` | Blue accent |
| `--accent-violet` | `#7C3AED` | Violet accent |
| `--focus` | `#93C5FD` | Visible keyboard focus |

Dark active/selected surfaces may use a restrained blue-to-violet gradient. Keep text contrast high; do not apply gradients to long body copy.

### Light mode
| Token | Value | Use |
|---|---|---|
| `--bg-primary` | `#F8FAFC` | Main background |
| `--bg-elevated` | `#F1F5F9` | Sidebar / elevated regions |
| `--surface` | `#FFFFFF` | Cards and dialogs |
| `--surface-tint` | `#F3E8FF` | Subtle violet tint |
| `--text-primary` | `#0F172A` | Main text |
| `--text-secondary` | `#475569` | Secondary text |
| `--border` | `#E2E8F0` | Dividers and outlines |
| `--accent-teal` | `#0F766E` | Selected/active states |
| `--accent-teal-hover` | `#0D9488` | Hover state |
| `--focus` | `#0F766E` | Visible keyboard focus |

## CSS token starter
```css
:root {
  color-scheme: light;
  --bg-primary: #F8FAFC;
  --bg-elevated: #F1F5F9;
  --surface: #FFFFFF;
  --surface-tint: #F3E8FF;
  --text-primary: #0F172A;
  --text-secondary: #475569;
  --border: #E2E8F0;
  --accent: #0F766E;
  --accent-hover: #0D9488;
  --focus: #0F766E;
  --shadow: 0 12px 36px rgba(15, 23, 42, .08);
  --radius-sm: 8px;
  --radius-md: 14px;
  --radius-lg: 22px;
  --content-max: 1200px;
}

[data-theme="dark"] {
  color-scheme: dark;
  --bg-primary: #0D0B18;
  --bg-elevated: #120F24;
  --surface: #181528;
  --surface-tint: #211D38;
  --text-primary: #FFFFFF;
  --text-secondary: #A7A5BC;
  --border: rgba(255,255,255,.12);
  --accent: linear-gradient(135deg, #2563EB, #7C3AED);
  --accent-solid: #7C3AED;
  --accent-hover: #8B5CF6;
  --focus: #93C5FD;
  --shadow: 0 18px 48px rgba(0, 0, 0, .32);
}
```

## Usage rules
- Use semantic tokens; avoid hardcoding colors in individual components.
- Keep status colors separate from brand accents (success, warning, error).
- Ensure text, controls, and focus indicators meet WCAG contrast requirements.
- Do not assume a gradient is a valid CSS color for every property. For borders, icons, and focus states, use a solid token or a gradient-capable property.
- Persist theme preference in a cookie or local storage only when appropriate; for SSR apps, prevent theme flash with a safe pre-hydration theme strategy.
