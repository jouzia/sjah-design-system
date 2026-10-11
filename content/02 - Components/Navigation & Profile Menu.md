# Navigation & Profile Menu

## Navigation
Suggested baseline:
- Dashboard / Overview
- Projects
- Activity or Analytics (only if the project has meaningful data)
- Documentation / Help (where useful)
- Bottom: Home, Settings
- Profile / Log out

Do not add menu destinations that do not exist. Use route-aware active states.

## Profile popover
Show:
- User display name and verified email, where available
- Account settings
- Theme preference if not already in the header
- Log out

Do not expose sensitive account metadata. Close on outside click and Escape. On mobile, consider a full-width bottom sheet if a small popover is awkward.
