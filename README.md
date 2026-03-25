# Broken Link Hijacking – quadsen.com

## Overview

This project documents a **Broken Link Hijacking (BLH)** vulnerability discovered on [quadsen.com](https://quadsen.com) during a security assessment. The vulnerability existed in the website's footer, where an Instagram link pointed to an unregistered social media handle — allowing an attacker to claim it and impersonate the brand.

---

## What is Broken Link Hijacking?

Broken Link Hijacking occurs when a website links to an external resource (social media handle, domain, or package) that no longer exists or was never registered. An attacker can claim that resource and use it to:

- Impersonate the brand
- Redirect users to phishing pages
- Spread misinformation
- Steal user credentials through deceptive outreach

---

## Target

- **Website:** quadsen.com
- **Vulnerability Location:** Footer section — Instagram social media link
- **Type:** Broken Link Hijacking (BLH)

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Browser DevTools | Inspect footer links and page source |
| curl | Verify HTTP responses from linked URLs |
| WHOIS Lookup | Check domain and handle registration status |
| Manual OSINT | Confirm Instagram handle availability |

---

## Methodology

### Step 1 — Reconnaissance
Inspected the quadsen.com footer using Browser DevTools and identified all outgoing social media links.

### Step 2 — Broken Link Identification
Found an Instagram URL in the footer pointing to a handle that did not exist. Confirmed using manual lookup and OSINT tools.

### Step 3 — Handle Registration
Registered the unclaimedInstagram handle to demonstrate attacker control.

### Step 4 — Proof of Concept
Populated the attacker-controlled Instagram profile with convincing, phishing-like content simulating brand impersonation.

### Step 5 — Verification
Clicking the Instagram link on quadsen.com redirected users to the attacker-controlled profile — confirming successful exploitation.

---

## Impact Analysis

| Threat | Description |
|--------|-------------|
| Brand Impersonation | Attacker controls a profile appearing to represent the company |
| Phishing | Users directed to malicious or deceptive content |
| Reputation Damage | Company associated with attacker's harmful content |
| Data Theft | Users tricked into sharing credentials through fake profiles |

---

## Recommendations

1. **Audit all external links** on your website regularly, especially social media links in headers and footers
2. **Only link to verified, official handles** — confirm they are active and owned by you
3. **Remove or correct broken links** immediately upon discovery
4. **Monitor brand mentions** and watch for impersonation attempts
5. **Educate your team** to verify the authenticity of linked accounts before publishing

---

## References

- [OWASP – Broken Link Hijacking](https://owasp.org)
- [HackerOne Reports on BLH](https://hackerone.com)
- WHOIS & domain/handle availability tools
- Instagram username lookup and verification guides

---

## Author

**Shivang Sawant** — Cybersecurity Engineer  
[LinkedIn](https://www.linkedin.com/in/shivang-sawant/) | [GitHub](https://github.com/rico3010)  
📧 shivangsawant30@gmail.com
