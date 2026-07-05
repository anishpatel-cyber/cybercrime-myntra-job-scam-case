# OSINT Reputation & Behavioral Analysis – Phase 3

**Case ID:** MYNTRA-TASKSCAM-20250627-001  
**Target URL:** https://heartlight-replica.lovable.app  
**Investigation Type:** Threat Reputation + Web Behavior Analysis  
**Phase:** OSINT Enrichment (External Scanner Validation)

---

# 1. VirusTotal Analysis Summary

## 1.1 Detection Status
- Detections: 0 / 92 security vendors
- Status: CLEAN (no malicious classification)

### Interpretation:
No antivirus or web reputation engine flagged the URL as malicious at scan time.

---

## 1.2 URL Classification

- Type: text/html
- Behavioral Category: password-input page
- External Resources: detected

### Interpretation:
- Page contains authentication-like structure
- External resources indicate dynamic content loading
- Consistent with login-based scam infrastructure

---

## 1.3 Engine Verdict

- All major vendors (BitDefender, Kaspersky, Sophos, etc.): CLEAN
- No malware signature detected
- No phishing blacklist match at scan time

### Key Insight:
> “Clean” does NOT mean legitimate — it only means not yet flagged.

---

## 1.4 Redirect Behavior

- Status Code: 200 OK
- No redirect chain observed

### Interpretation:
- Direct landing page load
- No cloaking or multi-stage redirect detected at scan time
- Simplifies attacker infrastructure

---

## 1.5 Community Intelligence

- No comments
- No user submissions
- No reputation feedback available

---

# 2. URLScan.io Behavioral Analysis

## 2.1 Final URL
https://heartlight-replica.lovable.app/

---

## 2.2 Hosting & Network

- IP Address: 185.41.148.2
- Geo: Sweden
- Infrastructure: Cloudflare-backed hosting

### Interpretation:
- IP belongs to shared infrastructure
- Likely platform-hosted deployment (not attacker-owned server)

---

## 2.3 Network Activity

- Total HTTP requests: 10
- Domains contacted: 2

### Interpretation:
- Low network complexity
- Minimal external dependency
- Suggests template-based web application

---

## 2.4 Page Behavior (Screenshot Analysis)

Observed UI:

- Myntra branding (impersonated)
- "Work from home" title
- Login form:
  - Email input
  - Password input
- Gradient UI background

### Interpretation:
- Designed to simulate corporate login portal
- Strong focus on trust-building UI elements
- No visible real authentication backend

---

## 2.5 Redirect Analysis

- No redirect chain observed
- Direct load to final page

---

# 3. Cross-Tool Correlation

| Source | Finding |
|--------|--------|
| VirusTotal | Clean / no detection |
| URLScan | Login-based UI confirmed |
| DNS Analysis | Cloudflare + platform hosting |
| OSINT Phase 2 | SaaS subdomain infrastructure |
| WhatsApp Evidence | ₹200 activation scam |

---

# 4. Key Security Insight

Even though the URL is classified as "CLEAN", multiple indicators confirm:

- Fake authentication system present
- Brand impersonation (Myntra)
- Social engineering flow confirmed via WhatsApp
- Payment-based activation structure
- Controlled onboarding environment

### Critical Conclusion:
> This is a **zero-detection fraud infrastructure**, not a malware-based attack.

---

# 5. Threat Model Classification

| Category | Status |
|----------|--------|
| Malware | Not observed |
| Phishing risk | High |
| Financial fraud risk | High |
| Social engineering risk | Very High |
| Detection evasion | Passive (not actively cloaked) |

---

# 6. Key Findings

- No antivirus detection despite clear scam behavior
- Website operates as low-risk to scanners but high-risk to humans
- Uses UI-based deception instead of malware
- Infrastructure relies on trust manipulation, not exploitation
- Cloudflare + SaaS hosting reduces attribution visibility

---

# 7. Final Assessment (Phase 3)

The domain demonstrates a **common limitation in security tools**:

> Automated scanners detect malware, but fail to reliably detect *social engineering fraud platforms*.

This confirms that:

- The attack is **not technically malicious at code level**
- The attack is **behaviorally malicious at user level**
- Detection relies on human reporting, not signature-based engines

---

# 8. Transition to Next Phase

Recommended next OSINT steps:

- Correlate WhatsApp number reputation
- Reverse image search fake payment proof
- Check reuse of same template across other subdomains
- Map infrastructure reuse patterns
- Identify possible scam network clusters