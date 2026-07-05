# Threat Actor Profiling Report – Phase 5

**Case ID:** MYNTRA-TASKSCAM-20260627-001  
**Phase:** OSINT Threat Actor Analysis  
**Objective:** Identify possible actor behavior patterns and reuse indicators

---

# 1. Known Identifiers

## 1.1 Social Entry Point
- Instagram: `adanafffjnnn529`

## 1.2 Communication Channel
- WhatsApp: +44 7988 014666

## 1.3 Infrastructure
- URL: https://heartlight-replica.lovable.app
- Platform: lovable.app subdomain

## 1.4 Fraud Elements
- Invitation Code: 456321
- Fake Email: janakpandey82@gmail.com
- Customer ID: 7948AB18

---

# 2. Behavioral Fingerprint

## Observed Patterns

- Job advertisement impersonation (Myntra)
- Work-from-home lure
- Commission-based earning promise (30–50%)
- Low entry fee scam (₹200 activation)
- Fake onboarding system
- Fake earnings proof
- WhatsApp-based persuasion loop

---

# 3. Infrastructure Pattern Analysis

## Observations
- Uses SaaS-hosted subdomain (lovable.app)
- No custom domain ownership
- Cloudflare DNS masking
- Template-based deployment structure
- Likely reusable scam kit

## Interpretation
This suggests:
> A scalable scam deployment model rather than a single static website.

---

# 4. Identity Reuse Analysis

## 4.1 Fake Identity Artifacts
- Email used in proof: janakpandey82@gmail.com
- Customer ID reused format: 7948AB18

## 4.2 Interpretation
- Likely synthetic identities used for fake trust simulation
- No evidence of real person linkage at this stage
- Possibly auto-generated placeholders

---

# 5. Cross-Platform Correlation (Hypothesis Layer)

## Potential reuse signals to investigate further:

- Same WhatsApp number appearing in other job scams
- Same Instagram pattern (random alphanumeric username)
- Similar “₹200 activation” scams using same structure
- Reused “Myntra work-from-home” templates
- Same lovable.app subdomain pattern across other cases

---

# 6. Threat Actor Behavior Model

## Observed Traits:

- Low technical sophistication
- High social engineering capability
- Scripted communication flow
- Modular scam infrastructure
- High scalability operation

---

# 7. Possible Actor Type Classification

| Category | Assessment |
|----------|-----------|
| Individual attacker | Unlikely |
| Small scam group | Possible |
| Organized scam network | Likely |
| Automated scam kit operators | Highly likely |

---

# 8. Key Intelligence Findings

- No direct attribution possible (no personal identity exposed)
- Strong indicators of reusable scam infrastructure
- Communication likely scripted or semi-automated
- Infrastructure suggests “scam-as-a-service” model

---

# 9. Threat Assessment

| Factor | Level |
|--------|------|
| Technical Skill | Low |
| Operational Scale | Medium–High |
| Victim Targeting Ability | High |
| Detection Avoidance | Medium |
| Reusability | Very High |

---

# 10. Conclusion

The available data suggests this is not an isolated scam instance but likely part of a **repeatable fraud template system** deployed across multiple victims.

Attribution to a specific individual or organization is not possible with current OSINT data.

However, behavioral and infrastructure patterns strongly indicate a **coordinated scam operation using reusable digital assets.**

---

# 11. Next Recommended Phase

To strengthen attribution analysis:

- Reverse image search fake payment proof
- Check WhatsApp number presence in scam databases
- Search Instagram username reuse patterns
- Compare lovable.app subdomains across other cases
- Look for identical UI templates in other scams