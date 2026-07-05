# OSINT Domain Intelligence Report – Phase 2

**Case ID:** MYNTRA-TASKSCAM-20250627-001  
**Target URL:** https://heartlight-replica.lovable.app  
**Investigation Type:** Infrastructure & Domain Analysis  
**Phase:** OSINT Technical Enrichment

---

# 1. Domain Overview

The investigated domain is a **subdomain hosted under a third-party platform (lovable.app)**.

```
heartlight-replica.lovable.app
```

### Key Observation:
- No independently registered domain owned by attacker
- Infrastructure relies on shared hosting platform

---

# 2. Registrar Information (Root Domain)

| Field | Value |
|------|------|
| Registrar | Cloudflare, Inc. |
| IANA ID | 1910 |
| Abuse Contact | registrar-abuse@cloudflare.com |
| Abuse Phone | +1.4153197517 |

### Interpretation:
- Root domain (`lovable.app`) is managed via Cloudflare Registrar
- Cloudflare provides DNS + protection layer
- Attribution is obscured due to proxy infrastructure

---

# 3. Domain Lifecycle Information

| Field | Value |
|------|------|
| Creation Date | 2023-05-06 |
| Last Updated | 2025-10-10 |
| Expiry Date | 2029-05-06 |

### Interpretation:
- Domain is relatively recent (≈ 2–3 years old)
- Long expiry suggests legitimate platform infrastructure (not attacker-controlled domain)
- Attacker likely abuses **platform hosting**, not domain ownership

---

# 4. Name Server Analysis

```
ivan.ns.cloudflare.com  
rafe.ns.cloudflare.com
```

### Interpretation:
- DNS fully managed by Cloudflare
- No independent DNS infrastructure exposed
- Makes direct attribution difficult
- Common in SaaS / hosting platforms

---

# 5. IP Address Analysis

```
185.41.148.1  
185.41.148.2
```

### Interpretation:

- Multiple IPs suggest load-balanced hosting
- Likely shared infrastructure used by platform
- Attacker does NOT control these IPs directly
- IP belongs to hosting provider network

---

# 6. CNAME / DNS Structure

- No CNAME record detected
- Direct A record mapping to IP addresses

### Interpretation:
- Straightforward routing
- Typical of platform-generated subdomains
- No custom enterprise DNS setup

---

# 7. SSL / Certificate Analysis

- No certificate transparency data found (crt.sh empty)

### Interpretation:
Possible reasons:
- Certificate not indexed yet
- Short-lived or dynamically generated certificate
- Platform-managed TLS termination (common in SaaS hosting)

---

# 8. Infrastructure Assessment

## Hosting Model
- Platform-based hosting (lovable.app)
- Multi-tenant infrastructure
- Dynamic subdomain generation

## Control Level
- Attacker control level: LOW–MEDIUM
- Platform control level: HIGH

---

# 9. Threat Intelligence Interpretation

This infrastructure indicates:

### Not a traditional phishing website
Instead:
- Template-based scam deployment system
- Rapid creation of multiple scam pages
- Low-cost scalable fraud infrastructure

---

# 10. Risk Assessment

| Category | Level |
|----------|------|
| Infrastructure Ownership | Low (platform-controlled) |
| Attribution Difficulty | High |
| Domain Abuse Potential | Medium |
| Fraud Usage Risk | High |
| Malware Risk | Low |

---

# 11. Key Findings

- Domain is NOT attacker-owned
- Scam is hosted via legitimate SaaS platform
- Cloudflare used for DNS + protection abstraction
- IP addresses belong to hosting infrastructure
- Likely part of scalable scam template system

---

# 12. Conclusion

The infrastructure behind the scam is **not independently controlled by the threat actor**, but rather deployed using a **third-party hosting platform (lovable.app)**.

This significantly increases:
- Deployment speed of scams
- Difficulty of attribution
- Ability to replicate campaigns

However, it also indicates:
> The attacker is operating at a "low infrastructure maturity level" but high social engineering effectiveness.

---

# 13. Next OSINT Phase Recommendation

Proceed with:

- VirusTotal URL analysis
- URLScan.io behavior inspection
- Reverse IP / infrastructure correlation
- Certificate transparency monitoring over time