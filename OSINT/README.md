# OSINT Intelligence Report – Phase 1 (Entity Extraction)

**Case ID:** MYNTRA-TASKSCAM-20260627-001  
**Investigation Type:** Task Scam / Brand Impersonation / Advance Fee Fraud  
**Phase:** Open Source Intelligence (Initial Entity Mapping)

---

# 1. Purpose

This document consolidates all known identifiers and external entities related to the suspected scam operation.  
It serves as the foundational dataset for further OSINT and infrastructure analysis.

---

# 2. Core Identifiers

## 2.1 Website (Primary Infrastructure)
- URL: https://heartlight-replica.lovable.app
- Type: Subdomain-based web application
- Purpose: Fake job registration / onboarding platform

---

## 2.2 Social Media Entry Point
- Platform: Instagram
- Username: `adanafffjnnn529`
- Role: Initial victim acquisition via job advertisement

---

## 2.3 Messaging Channel
- Platform: WhatsApp
- Number: +44 7988 014666
- Role: Recruitment communication + persuasion + payment request

---

## 2.4 Invitation / Access Control
- Invitation Code: `456321`
- Purpose: Required for registration / onboarding process

---

# 3. Financial / Fraud Indicators

## 3.1 Fake Identity Used in Payment Proof
- Name: janakpandey82@gmail.com
- Customer ID: 7948AB18
- Context: Displayed in alleged earnings/payment screenshot

---

## 3.2 Payment Requirement
- Amount: ₹200 (activation recharge)
- Claimed Purpose: Account activation for job access
- Nature: Advance fee fraud indicator

---

# 4. Brand Impersonation

## 4.1 Impersonated Organization
- Brand: Myntra

## 4.2 Observations
- Logo visually resembles official Myntra branding (~90% similarity reported)
- Brand identity used without authorization
- Used to create trust and legitimacy

---

# 5. Entity Relationship Summary

```text id="osint_flow_001"
Instagram Ad (adanafffjnnn529)
        ↓
WhatsApp (+44 7988 014666)
        ↓
Fake Job Offer (Myntra impersonation)
        ↓
Registration Website (lovable.app)
        ↓
₹200 Activation Request
        ↓
Fake Payment Proof (janakpandey82@gmail.com / 7948AB18)
```

---

# 6. Initial OSINT Observations

- Multi-platform coordination observed (Instagram → WhatsApp → Web)
- Use of free/low-cost hosting infrastructure (lovable.app)
- Structured scam progression (job lure → trust → payment request)
- Reuse of generic identity elements (fake email + customer ID)
- Brand impersonation used as primary trust mechanism

---

# 7. Threat Classification (Preliminary)

| Category | Level |
|----------|------|
| Social Engineering | High |
| Financial Fraud | High |
| Brand Impersonation | High |
| Infrastructure Sophistication | Medium |
| Malware Risk | Low (no evidence observed yet) |

---

# 8. Notes for Further Investigation

The following areas require deeper OSINT in next phase:

- Domain registration / WHOIS lookup
- Hosting infrastructure of lovable.app subdomain
- Certificate transparency logs
- Possible reuse of same template across other scams
- Tracking WhatsApp number reputation
- Reverse image search of fake payment proof
- Instagram account reuse in other campaigns

---

# 9. Conclusion

This phase confirms the operation as a coordinated **task-based advance fee fraud system** using:

- Social media advertising
- Messaging-based manipulation
- Fake web onboarding platform
- Fabricated financial proof

Further technical OSINT is required to identify infrastructure origin and possible linked scam clusters.