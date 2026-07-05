# Attack Chain Analysis (Kill Chain Model)

**Case ID:** MYNTRA-TASKSCAM-20260627-001  
**Phase:** OSINT Correlation (Step 4)

---

# 1. Attack Overview

This document maps the full lifecycle of the scam operation from initial contact to attempted financial exploitation.

---

# 2. Full Attack Flow

```text
Instagram Advertisement (adanafffjnnn529)
        ↓
Social Engineering Entry Point
        ↓
WhatsApp Redirection (+44 7988 014666)
        ↓
Job Offer Manipulation (Myntra impersonation)
        ↓
Trust Building + Commission Promise (30–50%)
        ↓
₹200 Activation Fee Request
        ↓
Fake Registration Website
(heartlight-replica.lovable.app)
        ↓
Fake Login System (Email + Password)
        ↓
Fake Dashboard / Earnings Simulation
        ↓
Payment / Withdrawal Illusion
        ↓
Potential Escalation (NOT REACHED)
Higher deposits / withdrawal block
```

---

# 3. Attack Stage Mapping (MITRE-style simplified)

| Stage | Description |
|------|-------------|
| Initial Access | Instagram advertisement |
| Execution | User interaction via WhatsApp |
| Persistence | Continued messaging + persuasion |
| Credential Harvesting | Fake login page |
| Collection | Email/password input (potential capture) |
| Impact | Financial fraud attempt (₹200 activation fee) |

---

# 4. Infrastructure Mapping

## 4.1 Entry Layer
- Instagram account: `adanafffjnnn529`
- Purpose: victim acquisition

## 4.2 Communication Layer
- WhatsApp: `+44 7988 014666`
- Purpose: persuasion + control channel

## 4.3 Application Layer
- URL: https://heartlight-replica.lovable.app
- Platform: lovable.app (SaaS hosting)
- Purpose: fake job system simulation

---

# 5. Behavioral Pattern Analysis

The attack follows a structured **task scam progression model**:

## Phase 1: Attraction
- Fake job advertisement
- High salary promise

## Phase 2: Trust Building
- Friendly communication
- Simple job explanation
- Commission promise

## Phase 3: Commitment Trap
- ₹200 "activation fee"
- Small investment justification

## Phase 4: Simulation
- Fake login system
- Fake dashboard
- Fake earnings proof

## Phase 5: Escalation (intended but not reached)
- Larger deposits
- Withdrawal blocking
- Continued extraction

---

# 6. Infrastructure Insights

- Uses SaaS-hosted subdomain (low-cost deployment)
- No independent domain ownership
- Cloudflare-backed infrastructure
- Template-based scam deployment system
- Easily replicable across multiple campaigns

---

# 7. Key Intelligence Findings

- Entire system is modular and reusable
- No malware or exploit usage
- Fully relies on psychological manipulation
- Infrastructure is low sophistication, high scalability
- Designed for rapid victim turnover

---

# 8. Threat Classification

| Category | Level |
|----------|------|
| Technical Sophistication | Low |
| Social Engineering | Very High |
| Financial Fraud Risk | High |
| Detection Difficulty | High (for users, low for scanners) |

---

# 9. Conclusion

This attack is a **multi-stage social engineering fraud system** that:

- Uses social media for targeting
- Uses messaging apps for manipulation
- Uses web apps for simulation
- Uses financial triggers for exploitation

The operation is **not malware-driven**, but **behavior-driven fraud architecture**.

---

# 10. Next Phase Recommendation

Proceed to:

- WhatsApp number reputation OSINT
- Reverse image search of fake payment proof
- Template reuse detection across other subdomains
- Threat actor clustering analysis