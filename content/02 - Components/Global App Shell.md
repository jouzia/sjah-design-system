# Global App Shell

## Header
- Left: three-line navigation toggle and animated project title.
- Right: theme toggle and user avatar.
- Header should remain stable while content scrolls; don't cover content with fixed elements.

## Sidebar
- Main section: project-specific navigation (e.g. Dashboard, Projects, Analytics, Documentation).
- Bottom section: Home and Settings; profile entry may be placed here if it improves the information architecture.
- Active item uses blue-violet highlight in dark mode and teal in light mode.
- Provide labels, active-state semantics, and focus styles.

## Main content
- Use a consistent page container and spacing tokens.
- Every route needs loading, empty, error, and success states where applicable.
- Use project-specific navigation and modules; do not force irrelevant sections into every project.

## Footer
- Brand lockup and AI limitation notice (where AI-generated content is shown).
- Keep footer in document flow; do not pin it over short screens unless there is a clear reason.
