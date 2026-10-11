# SJAH Design System Home

> [!abstract] Purpose
> A single source of truth for the look, feel, and reusable frontend behavior of SJAH projects.

## Core references
- [[Design Tokens]]
- [[Typography & Branding]]
- [[Interaction & Motion]]
- [[Responsive Layout & Spacing]]
- [[Accessibility & UX Rules]]
- [[Authentication & OTP]]
- [[AI Assistant Widget]]
- [[Footer & Brand Attribution]]
- [[Frontend Quality Gate]]
- [[Project Design Checklist]]

## Standard experience
1. **First visit:** show a brief project-name type-on animation centered in the viewport, then move it into the top-left header position.
2. **App shell:** three-line navigation control, project title, theme control, and profile avatar.
3. **Navigation:** sliding desktop sidebar; accessible overlay drawer on mobile; persistent Home and Settings entries at the bottom.
4. **Main content:** spacious, responsive content layout with project-specific modules.
5. **AI helper:** floating assistant control with a consistent SJAH AI mark/mascot, contextual greeting, and a clear chat panel.
6. **Footer:** supplied SJAH emblem + “A Project of SJAH”, framed by horizontal lines, plus a concise AI limitation notice where relevant.

## Implementation rule
The visual blueprint is not proof that a feature works. Authentication, OTP delivery, persistence, AI responses, account management, and logout must be connected to real backend/API behavior and tested. Avoid shipping static mock interactions as if they were functional.
