# FINAL INCIDENT REPORT

**Case ID:** MYNTRA-TASKSCAM-20250627-001  
**Incident Type:** Task Scam / Advance Fee Fraud / Brand Impersonation / Social Engineering Attack  
**Investigator:** Anish Kumar Patel  
**Location:** Kathmandu, Nepal  
**Report Type:** Digital Forensics & Incident Response (DFIR)

---

# 1. Executive Summary

This investigation documents a multi-stage **task-based fraud operation** targeting individuals through social media advertisements impersonating the brand **Myntra**.

The attack chain involved:

- Instagram advertisement for fake job opportunity
- WhatsApp-based social engineering interaction
- Fake onboarding website hosted on a SaaS platform
- Request for ₹200 activation fee
- Fake earnings and payment simulation

No financial loss occurred as the victim identified the scam before payment.

---

# 2. Incident Scope

## Platforms involved:
- Instagram (initial contact)
- WhatsApp (social engineering communication)
- Web platform (https://heartlight-replica.lovable.app)

## Objective of attacker:
- Induce victim to pay activation fee
- Simulate employment onboarding process
- Potential escalation to larger financial fraud

---

# 3. Attack Timeline Summary

## Phase 1: Initial Contact
- Instagram advertisement promoting “Myntra Work From Home Job”

## Phase 2: Social Engineering
- Victim redirected to WhatsApp: +44 7988 014666
- Job offer presented with high commission promise (30–50%)

## Phase 3: Commitment Trap
- ₹200 activation fee requested
- Justified as onboarding requirement

## Phase 4: Fake Infrastructure
- Website: lovable.app subdomain
- Login system (email/password)
- Fake dashboard and earnings simulation

## Phase 5: Fraud Attempt
- Fake payment proof shown (NPR 325.00)
- Attempt to build trust and encourage payment

## Phase 6: Termination
- Victim identified scam
- No payment made
- Evidence preserved

---

# 4. Technical Analysis Summary

## 4.1 Website Infrastructure
- Domain: lovable.app (SaaS-hosted)
- Subdomain: heartlight-replica.lovable.app
- Hosting: Cloudflare-backed infrastructure
- IP: 185.41.148.1 / 185.41.148.2

## 4.2 Security Observation
- No malware detected
- No redirects observed
- Login page is purely UI-based simulation
- No verified backend authentication system

---

# 5. OSINT Findings

## Identifiers:
- Instagram: adanafffjnnn529
- WhatsApp: +44 7988 014666
- Invitation Code: 456321
- Fake email: janakpandey82@gmail.com
- Customer ID: 7948AB18

## Brand Impersonation:
- Myntra (visual + identity misuse)

---

# 6. Threat Intelligence Analysis

## Key Techniques Observed:
- Social engineering (high effectiveness)
- Brand impersonation
- Fake job advertisement lure
- Payment-based activation scam
- Fake proof-of-payment manipulation
- Multi-platform migration (IG → WhatsApp → Web)

## MITRE-style mapping:
- Initial Access: Social media advertisement
- Execution: User engagement via WhatsApp
- Credential Harvesting: Fake login form
- Impact: Financial fraud attempt

---

# 7. Threat Actor Assessment

## Observed Characteristics:
- Low technical sophistication
- High social engineering capability
- Scripted communication flow
- Modular scam infrastructure
- Highly scalable deployment model

## Likely classification:
- Scam-as-a-Service operation
- Small organized fraud group or template-based network

---

# 8. Risk Assessment

| Category | Level |
|----------|------|
| Financial Risk | High |
| Social Engineering Risk | Very High |
| Malware Risk | Low |
| Detection Evasion | Medium |
| Attribution Difficulty | High |

---

# 9. Key Findings

- No malware involved; purely behavioral attack
- Entire system is UI-driven fraud simulation
- Infrastructure is SaaS-based and easily replicable
- Attack relies on psychological manipulation rather than technical exploitation
- Clean reputation in security scanners does not indicate safety

---

# 10. Impact Assessment

- No financial loss incurred
- No credentials compromised
- No malware execution
- User awareness successfully prevented escalation

---

# 11. Conclusion

This incident represents a **structured task-based fraud ecosystem** designed to:

- Attract victims via social media
- Build trust through messaging apps
- Simulate employment via web application
- Extract small initial payments
- Potentially escalate to larger financial fraud

The operation demonstrates **high social engineering sophistication with low technical complexity**.

---

# 12. Recommendations

- Report Instagram and WhatsApp accounts
- Report hosting abuse on lovable.app platform
- Increase awareness about task scam patterns
- Monitor reuse of same templates across platforms
- Educate users about fake job activation fees

---

# 13. Final Statement

This report was prepared for educational and forensic analysis purposes.  
All data is based on observed evidence and OSINT collection.  
No unauthorized access or interaction beyond observation was performed.