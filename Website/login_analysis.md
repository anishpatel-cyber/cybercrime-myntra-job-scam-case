# Website Forensic Analysis – Login Page Stage

**Case ID:** MYNTRA-TASKSCAM-20260627-001  
**URL:** https://heartlight-replica.lovable.app/login  
**Stage:** Authentication Interface (Pre-Login)  
**Analysis Type:** Passive Web Observation (No Interaction)

---

# 1. Observation Summary

When accessing the website via browser, the system automatically redirects to the `/login` endpoint.

The page displays a login interface claiming to be related to "Work from Home" employment under the **Myntra brand impersonation**.

No authentication was performed. All data below is based on visible UI elements only.

---

# 2. Page Metadata

| Field | Value |
|------|------|
| Page Title | Work from home |
| URL | /login |
| Redirection Behavior | Automatic redirect from root domain to login page |
| Authentication Type | Email + Password (fake login form) |

---

# 3. UI Elements Observed

## Branding Section
- Logo displayed: **Myntra**
- No official Myntra domain reference present
- Branding appears visually imitated

---

## Login Form Structure

The following input fields are visible:

- Email Address field
- Password field

Buttons / Options:

- Login
- Register
- Forgot Password

---

## Supporting Text

- "Please enter your email and password"
- "Login"
- "Register"
- "Forgot password?"

---

# 4. Functional Observations

- No actual authentication verification observed at this stage
- No visible CAPTCHA or security mechanism
- No corporate domain authentication (e.g., myntra.com SSO not used)
- Login appears to be a **custom-built form likely controlled by attacker infrastructure**

---

# 5. Behavioral Analysis

This login page demonstrates typical characteristics of **fraudulent job portal infrastructure**:

## 5.1 Brand Impersonation
- Use of Myntra branding without official domain
- Attempt to create trust via recognizable corporate identity

## 5.2 Fake Authentication Layer
- Email/password form likely used to:
  - Collect credentials
  - Create illusion of real job portal
  - Track victims per session

## 5.3 Controlled Access Pattern
- Entry restricted via login screen
- Suggests multi-stage scam platform:
  - Login → Dashboard → Earnings → Payment request

---

# 6. Social Engineering Role in Attack Chain

This login page acts as:

### Stage 3: Victim Engagement Layer

| Stage | Description |
|------|-------------|
| 1 | Instagram advertisement (job lure) |
| 2 | WhatsApp persuasion |
| 3 | Login portal (THIS STAGE) |
| 4 | Fake dashboard & earnings |
| 5 | Payment / recharge request |

---

# 7. Risk Assessment

| Risk Type | Level | Reason |
|-----------|------|--------|
| Credential Harvesting | High | Email/password fields present |
| Brand Impersonation | High | Myntra branding misuse |
| Financial Fraud | High | Known ₹200 activation flow |
| Malware Risk | Low | No executable payload observed at login stage |

---

# 8. Indicators of Compromise (IoCs)

- URL: `https://heartlight-replica.lovable.app/login`
- Brand impersonated: Myntra
- Page Title: "Work from home"
- Authentication method: Fake email/password login form
- Redirect behavior: Forced `/login` routing

---

# 9. Key Forensic Insight

This login page is not a legitimate authentication system. Instead, it is a **controlled access checkpoint** designed to:

- Segment victims
- Track engagement
- Simulate corporate onboarding
- Prepare users for fake dashboard + payment flow

---

# 10. Preliminary Conclusion

The login page confirms that the infrastructure is not a simple static scam page but a **multi-stage fraudulent job simulation system**, likely designed to:

- Build trust through UI realism
- Capture user credentials
- Transition victims toward financial exploitation stages

No interaction was performed, preserving forensic integrity.