# Interaction & Motion

## Motion language
- Navigation drawer: slide from left with a subtle spring/ease-out.
- Menus/popovers: fade + small scale/translate; anchor to the triggering control.
- Active navigation: short highlight transition, restrained glow only in dark mode.
- AI assistant: gentle idle motion; stop or reduce it when reduced motion is requested.
- Loading: use skeletons for content loading and clear progress labels for longer operations.
- Avoid long intro animations that block access to content.

## Timing guidance
| Interaction | Typical duration |
|---|---:|
| Hover/focus | 120–180 ms |
| Popover | 160–220 ms |
| Drawer | 220–320 ms |
| Page transition | 180–300 ms |
| Intro title | 1.5–2.8 s total, skippable/reduced-motion aware |

## Three-line menu
- Use a real button with an accessible name and `aria-expanded`.
- Desktop: toggles sidebar.
- Mobile: opens an overlay drawer with backdrop and close control.
- Escape closes the drawer; focus stays within modal-like mobile drawer where appropriate.
- Clicking a navigation item closes the mobile drawer.

## Profile avatar
- Top-right circular avatar opens a menu with profile details, account settings, theme preference (if not elsewhere), and Log out.
- Bottom sidebar may include the same profile entry if useful, but avoid confusing duplicate controls.
- Click outside and Escape should dismiss the menu.
- Logout must invalidate/revoke the session server-side, not merely navigate away.

## Theme switching
- Use a clear switch/button with current state announced accessibly.
- Persist preference and prevent flash on initial render.
- Do not rely on color alone to indicate active selection.
