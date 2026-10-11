# Footer & Brand Attribution

## Required Brand Lockup
`— [SJAH Emblem] A Project of SJAH —`

### Design Guidelines & Constraints
* **Emblem Asset:** Always point to `../05 - Assets/sjah-emblem.png` (or `/assets/sjah-emblem.png` in root-relative deployments)[cite: 9].
* **Alignment:** Centered horizontal flex container flanked by subtle gradient accent lines.
* **Typography:** Custom brand font (`SpaceAge` / `Orbitron`) applied sparingly for brand voice.
* **Theme Testing:** Glow filters tested across both Dark (`--bg-primary: #0D0B18`) and Light (`--bg-primary: #F8FAFC`) modes without damaging image colors[cite: 9].
* **AI Disclaimer:** Includes the standard AI safety disclaimer required across all SJAH interactive projects.

---

## 1. Accessible HTML Structure

```html
<footer class="main-footer" role="contentinfo" aria-label="Site Footer">
  <!-- AI Disclaimer Banner -->
  <div class="ai-disclaimer">
    <span>AI can make mistakes. Check important information.</span>
  </div>

  <!-- Brand Lockup -->
  <div class="footer-lockup">
    <div class="footer-line" aria-hidden="true"></div>
    
    <div class="footer-branding">
      <div class="logo-wrapper">
        <img 
          src="../05 - Assets/sjah-emblem.jpg" 
          alt="SJAH Crest Logo" 
          class="sjah-crest-logo"
          loading="lazy"
          width="44"
          height="44"
        />
      </div>
      <span class="footer-text">A Project of SJAH</span>
    </div>

    <div class="footer-line" aria-hidden="true"></div>
  </div>
</footer>
/* ==========================================================================
   FOOTER & BRAND ATTRIBUTION COMPONENT
   ========================================================================== */

.main-footer {
  margin-top: auto;
  padding: 32px 16px 24px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 16px;
  border-top: 1px solid var(--border-color);
  background: var(--bg-primary);
  width: 100%;
}

/* AI Safety Disclaimer */
.ai-disclaimer {
  font-size: 0.8rem;
  color: var(--text-secondary);
  text-align: center;
  opacity: 0.8;
  letter-spacing: 0.2px;
}

/* Brand Lockup Wrapper */
.footer-lockup {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
  width: 100%;
  max-width: 600px;
}

/* Side Accent Lines */
.footer-line {
  height: 1px;
  flex: 1;
  max-width: 120px;
  background: linear-gradient(
    90deg, 
    transparent, 
    var(--text-secondary), 
    transparent
  );
  opacity: 0.4;
}

/* Branding Content */
.footer-branding {
  display: flex;
  align-items: center;
  gap: 12px;
}

.logo-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

/* Emblem Image & Glow Preserving Filters */
.sjah-crest-logo {
  height: 44px;
  width: auto;
  object-fit: contain;
  /* Gold/amber outer glow matching emblem edge highlights */
  filter: drop-shadow(0 0 6px rgba(234, 179, 8, 0.35));
  transition: transform 0.3s cubic-bezier(0.16, 1, 0.3, 1), filter 0.3s ease;
}

.sjah-crest-logo:hover {
  transform: scale(1.08);
  filter: drop-shadow(0 0 14px rgba(234, 179, 8, 0.65));
}

/* Light Mode Specific Contrast Adjustment */
[data-theme="light"] .sjah-crest-logo {
  /* Natural shadow to retain emblem definition against light backgrounds */
  filter: drop-shadow(0 2px 6px rgba(0, 0, 0, 0.4));
}

[data-theme="light"] .sjah-crest-logo:hover {
  filter: drop-shadow(0 4px 10px rgba(0, 0, 0, 0.5));
}

/* Brand Attribution Text */
.footer-text {
  font-family: 'SpaceAge', 'Orbitron', -apple-system, sans-serif;
  font-size: 0.9rem;
  font-weight: 600;
  letter-spacing: 2.5px;
  color: var(--text-primary);
  text-transform: uppercase;
  white-space: nowrap;
}

/* Responsive Scaling for Mobile Screens */
@media (max-width: 480px) {
  .footer-line {
    max-width: 50px;
  }
  
  .sjah-crest-logo {
    height: 36px;
  }

  .footer-text {
    font-size: 0.8rem;
    letter-spacing: 1.8px;
  }
}