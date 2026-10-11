# Shared Frontend Contract for SJAH Projects

This contract applies across **BUD AI**, **Tracker AI**, **Recruit AI**, **Pulse AI**, research tools, and all future SJAH web applications unless an explicit, documented project-specific decision overrides it.

---

## 1. Global Specifications (Must Share)

Every web application built under the SJAH umbrella must strictly adhere to the unified specifications maintained in the design system:

1. **Color & Theme Tokens:** [[Design Tokens]] (Dark Blue-Black `#0D0B18` primary with Dark Blue-Violet gradients, Light Mode Teal accents, and surface glassmorphism).
2. **Typography & Motion:** [[Typography & Branding]] and [[Interaction & Motion]] (Futuristic Space-Age typography, center-to-top-left smooth heading entrance, and reduced-motion fallbacks).
3. **App Layout & Navigation:** [[Global App Shell]] and [[Navigation & Profile Menu]] (Gemini-style 3-gridline burger menu, sliding drawer, permanent bottom links for Home/Settings).
4. **User Profile Popover:** [[Navigation & Profile Menu]] (Top-right avatar trigger with floating user details card and log out actions).
5. **Interactive AI Chatbot:** [[AI Assistant Widget]] (Floating FAB with mascot introduction and doubt clarification capabilities).
6. **Authentication & Email Flow:** [[Authentication & OTP]] (Sliding desktop card / mobile stacked layout, creative OTP email template with mascot artwork).
7. **Footer Brand Attribution:** [[Footer & Brand Attribution]] (Mandatory `— [SJAH Emblem] A Project of SJAH —` lockup with AI disclaimer and glow preservation).
8. **Accessibility & Responsive Standards:** [[Accessibility & UX Rules]] and [[Responsive Layout & Spacing]] (Keyboard focus indicators, WCAG color contrast, and fluid breakpoints).

---

## 2. Local Scope (Must Remain Project-Specific)

While the visual foundation and core interaction shell are shared, the following architectural and domain elements **must be implemented independently** per project:

* **Product Navigation & Pages:** Specific sidebar links, page routes, and domain-specific view hierarchies.
* **Permissions & Roles:** User access controls (e.g., Admin, Student, Educator, Recruiter).
* **AI System Behavior:** System instructions, mascot persona nuances, Model Context Protocol (MCP) tool integrations, RAG pipelines, and API endpoints.
* **Domain Workflows & Analytics:** Charts, data visualization components, dashboard widgets, and specific business logic.
* **Auth Backend & Sessions:** NextAuth/Supabase/FastAPI authentication providers, token management, and session cookies.
* **Error Handling & Telemetry:** Application error boundaries, toast notifications, logging, and analytics tracking.

---

## 3. Production Integration Rules

> [!WARNING]
> **No Static Code Drops**  
> Do not paste a generic static HTML/CSS mock directly into a production codebase and consider it complete. 

When onboarding a new project to this contract:
1. **Component Modularization:** Port HTML/CSS specifications from [[UI Components]] into native framework components (e.g., React/Next.js JSX, Vue components, or Svelte templates).
2. **State & Theme Integration:** Connect theme tokens directly to your application's global CSS variables or Tailwind CSS configuration file.
3. **Real Service Binding:** Connect navigation items to live router links, map the top-right profile popover to real user session state, and point the AI widget to live Gemini API endpoints.
4. **Verification:** Test all responsive breakpoints, dark/light theme switching, and keyboard navigation prior to deployment.