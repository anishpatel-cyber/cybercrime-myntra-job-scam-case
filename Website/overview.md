# Website Forensic Analysis

**Case ID:** MYNTRA-TASKSCAM-20250627-001  
**Evidence Source:** Suspicious Registration Website  
**URL:** https://heartlight-replica.lovable.app  
**Platform Type:** Web Application (Hosted on third-party low-code platform)  
**Investigation Type:** Phishing / Task Scam Infrastructure Analysis  

---

# 1. Purpose

This folder documents the technical and behavioral analysis of the registration website used in the suspected scam operation.

The objective is to determine:

- Website purpose and functionality
- Hosting and infrastructure characteristics
- Data collection behavior
- Potential phishing or fraud indicators
- Relationship with WhatsApp social engineering phase

---

# 2. Website Overview

The website `heartlight-replica.lovable.app` was provided to the victim during WhatsApp communication as part of a job activation process.

It was presented as:

- Registration portal for work-from-home job
- Activation system requiring ₹200 recharge
- Platform to receive “order tasks”
- System to track earnings and commissions

---

# 3. Observed Workflow (User Perspective)

1. User receives link from WhatsApp agent  
2. User is instructed to register using invitation code  
3. System displays onboarding / registration interface  
4. User is prompted to complete “activation recharge”  
5. System claims to unlock earning dashboard  
6. Fake earnings and order tasks are displayed  

---

# 4. Registration Details Provided

| Field | Value |
|------|------|
| URL | https://heartlight-replica.lovable.app |
| Invitation Code | 456321 |
| Claimed Bonus | ₹60 registration bonus |
| Activation Requirement | ₹200 recharge |

---

# 5. Infrastructure Observations

## 5.1 Hosting

- Hosted on `lovable.app` subdomain
- Indicates use of **low-code / AI website builder platform**
- No independent domain ownership observed
- No official corporate infrastructure

---

## 5.2 Domain Characteristics

- Subdomain-based deployment
- No brand-linked domain (e.g., myntra.com not used)
- Likely dynamically generated project site
- Easily replaceable infrastructure (high abuse risk)

---

## 5.3 Security Indicators

- HTTPS present (TLS enabled)
- Certificate does not validate real organization identity
- No EV (Extended Validation) certificate observed

---

# 6. Behavioral Analysis

The website exhibits characteristics consistent with **task scam platforms**:

- Prompts user for financial “activation” payment
- Simulates job onboarding process
- Displays fabricated earning potential
- Likely uses scripted UI rather than real backend commerce system
- No verifiable company identity or registration details

---

# 7. Data Collection Risk Assessment

The following potential data risks are identified:

| Data Type | Risk Level | Notes |
|-----------|-----------|------|
| Personal Info (Name/Phone) | Medium | Likely collected during registration |
| Payment Data | High | ₹200 recharge request indicates financial capture attempt |
| Email Address | Medium | May be used for fake account creation |
| Device Info | Unknown | No evidence yet, but possible via tracking scripts |
| Credentials | Unknown | No login system confirmed |

---

# 8. Technical Behavior (Expected / Inferred)

Based on similar scam architectures:

- Frontend likely built using template-based system
- Backend likely minimal or simulated
- “Earnings” likely frontend-only fake values
- Payment flow likely redirected to external payment handler (not observed here directly)
- Data may be stored in third-party services (Firebase / Supabase / webhook APIs)

---

# 9. Social Engineering Integration

This website is part of a multi-stage attack chain:

## Stage 1: Instagram
- Job advertisement bait

## Stage 2: WhatsApp
- Social engineering + persuasion + trust building

## Stage 3: Website (THIS STAGE)
- Fake job platform + payment requirement

## Stage 4 (Intended, not reached)
- Escalated deposits
- Withdrawal restriction
- Further financial exploitation

---

# 10. Indicators of Compromise (IoCs)

- URL: `https://heartlight-replica.lovable.app`
- Platform: lovable.app subdomain hosting
- Invitation Code: `456321`
- Payment Requirement: ₹200 activation fee
- Claimed Bonus: ₹60
- Impersonated Brand: Myntra

---

# 11. Risk Classification

| Category | Level |
|----------|------|
| Phishing Risk | High |
| Financial Fraud Risk | High |
| Malware Risk | Low (no executable evidence observed) |
| Credential Theft Risk | Medium |
| Social Engineering Risk | Very High |

---

# 12. Preliminary Conclusion

The website is part of a structured **task-based fraud ecosystem** designed to:

- Simulate legitimate employment onboarding
- Extract small initial payments
- Build trust for larger future deposits
- Leverage fake earnings dashboards to reinforce belief

The infrastructure suggests a **template-driven scam deployment system**, likely reused across multiple similar campaigns with different branding.

---

# 13. Evidence Integrity

- Website accessed only for observation and documentation
- No interaction with payment systems performed
- No credentials entered
- Screenshots and references preserved from WhatsApp delivery
- No modification of original URL content

---

# 14. Final Assessment

The website is assessed as a **fraudulent job activation portal** used in conjunction with WhatsApp-based social engineering to execute a task scam involving advance fee fraud tactics.

This component completes the technical layer of the scam chain.