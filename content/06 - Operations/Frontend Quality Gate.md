# Frontend Quality Gate

Run this gate before declaring a shared UI implementation complete.

## Automated
- [ ] Lint
- [ ] Typecheck
- [ ] Unit/component tests
- [ ] Production build
- [ ] Accessibility checks where available
- [ ] Responsive screenshot checks for key routes

## Manual
- [ ] Fresh account signup/login flow
- [ ] OTP expiry, incorrect code, resend cooldown, and rate limit
- [ ] Logout and session expiry
- [ ] Keyboard-only navigation
- [ ] Screen reader labels on key controls
- [ ] Reduced-motion preference
- [ ] Theme preference after refresh
- [ ] Mobile drawer, backdrop, and Escape
- [ ] AI assistant success, timeout, provider failure, and empty state
- [ ] Light/dark logo contrast and footer spacing

## Definition of done
A UI is done only when the appearance, behavior, accessibility, responsive states, and connected backend behavior have all been verified. A rendered mockup alone does not pass this gate.
