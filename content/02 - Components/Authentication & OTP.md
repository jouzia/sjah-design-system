# Authentication & OTP

## UX flow
1. New or returning user enters email.
2. Backend applies rate limits and sends a one-time code using a configured transactional email provider.
3. User enters the code in a dedicated verification screen.
4. Backend verifies code, expiry, attempt count, and single-use status.
5. On success, create a secure session and route to the app.
6. Offer resend with a cooldown and clear error states.

## Email copy
**Subject:** Your SJAH sign-in code

Dear User,

Your one-time password (OTP) for login is:

**{{OTP_CODE}}**

This code is valid for **05:00 minutes**. Do not share this code with anyone.

If you did not request this code, you can ignore this email.

A supplied “Let’s Go..” cat illustration may appear below the message if the email provider supports embedded or hosted assets. Use a verified production asset URL or CID attachment; never leave `your-domain.com` placeholders in production.

## Security requirements
- Generate codes with a cryptographically secure random generator.
- Store only a hash of the OTP where feasible.
- Enforce five-minute expiry server-side, single use, and attempt limits.
- Rate-limit sends and verification attempts by account and IP/device signals.
- Avoid revealing whether an email address is registered.
- Never log raw OTPs or put them in analytics.
- Use HTTPS; protect sessions with secure, HttpOnly, SameSite cookies when using cookie sessions.
- Add CSRF protection as appropriate to the architecture.
- Resend invalidates previous codes or follows a clearly documented policy.
- Keep email delivery secrets on the server, never in frontend code.

## Design guidance
- Desktop: split-panel auth card can be used if it remains readable and does not overcomplicate the flow.
- Mobile: stacked layout with clear Login/Create account switching.
- Labels remain visible; password visibility control is optional if password auth exists.
- Social login buttons should only appear when the provider is actually configured.
- Avoid combining OTP and password fields on one screen unless the flow requires it.
