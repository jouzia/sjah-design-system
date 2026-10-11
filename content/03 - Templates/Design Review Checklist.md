# Design Review Checklist

## Visual system
- [ ] Colors use semantic tokens
- [ ] Typography hierarchy is consistent
- [ ] Spacing and card radius are consistent
- [ ] Logo is correct, proportional, and clear in both themes
- [ ] Active/hover/focus states are visible
- [ ] No unnecessary neon glow or excessive glass effects

## Interaction
- [ ] Navigation opens/closes correctly
- [ ] Profile menu works with keyboard and pointer
- [ ] Theme preference persists without a flash
- [ ] Motion respects reduced-motion preference
- [ ] Every visible control has a real action
- [ ] Empty/error/loading/success states are implemented

## Responsive and accessible
- [ ] 320px, 375px, tablet, laptop, wide desktop checked
- [ ] No horizontal overflow
- [ ] Touch targets are usable
- [ ] Focus order is logical
- [ ] Dialog focus and Escape handling work
- [ ] Text contrast meets WCAG AA
- [ ] Screen-reader labels are present

## Production readiness
- [ ] No placeholder domains or demo OTPs
- [ ] No secrets in frontend bundles
- [ ] Authentication and authorization verified server-side
- [ ] AI failures/rate limits handled
- [ ] No console errors
- [ ] Lint, typecheck, tests, and build pass
