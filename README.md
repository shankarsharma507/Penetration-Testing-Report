# 🛡️ Web Application Penetration Testing Report  

## 🎯 Target: [YoungSkilledIndia.com](https://www.youngskilledindia.com/)  

This repository documents a **Black-Box Web Application Penetration Test** conducted on **YoungSkilledIndia.com**, an educational platform providing professional development and certification courses.  

---

## 📌 Project Overview  

- **Assessment Type**: Black-box (no source code access)  
- **Duration**: July 2025 – August 2025  
- **Testing Model**: Based on [OWASP WSTG](https://owasp.org/www-project-web-security-testing-guide/) & OWASP Top 10 (2021)  
- **Tools Used**:  
  - Reconnaissance → Sublist3r, theHarvester, crt.sh  
  - Scanning & Enumeration → Nmap, WPScan, WhatWeb, Wappalyzer  
  - Proxy Testing → Burp Suite (Community Edition)  
  - Utilities → Dig, Dirsearch, SSL Labs  
- **Permission**: Explicit written approval obtained from the site owner  

---

## 🧪 Scope of Testing  

| Category             | Details |
|----------------------|---------|
| **Target URL**       | https://www.youngskilledindia.com/ |
| **Test Type**        | External Black-box |
| **Authentication**   | Public areas only |
| **Forbidden Actions**| DoS/DDoS, brute force beyond PoC, social engineering, live data exploitation, destructive testing |

---

## 📖 Methodology  

Testing followed a structured approach:  

1. **Reconnaissance** – Passive info gathering (WHOIS, DNS, SSL, Subdomains).  
2. **Enumeration** – Active probing (directories, services, components).  
3. **Vulnerability Analysis** – Testing against OWASP Top 10 categories.  
4. **Exploitation (Non-Destructive)** – Controlled PoC demonstrations.  
5. **Risk Assessment** – Severity scoring via CVSS v3.1.  
6. **Reporting** – Structured findings with business impact & remediation.  

---

## 🔍 Vulnerability Summary  

| OWASP 2021 Category | Finding ID | Severity | Status | Description |
|----------------------|------------|----------|--------|-------------|
| A01: Broken Authentication | A01-01 | N/A | Not Vulnerable | No username enumeration/session issues |
| A02: Cryptographic Failures | A02-001 | Low | Informational | HTTPS enforced, TLS strong, minor cipher notice |
| A03: Injection | A03-001 | Medium | Vulnerable | SQLi suspected in login form |
| A04: Insecure Design | A04-001 | Medium | Vulnerable | No MFA, no CAPTCHA, unlimited login attempts |
| A05: Security Misconfiguration | A05-001 | Low | Vulnerable | Minor file access anomalies (200/403/404 codes) |
| A06: Vulnerable & Outdated Components | A06-001 | High | Vulnerable | Astra theme outdated, PHP 7.4 EOL, readme.html exposed |
| A07: Identification & Authentication Failures | A07-001 | Medium | Vulnerable | Weak password policy, no brute force prevention |
| A08: Software & Data Integrity Failures | A08-001 | Medium | Vulnerable | No plugin/theme integrity validation |

---

## ⚠️ Key Findings  

- **Outdated Components**: PHP 7.4 (EOL), Astra theme outdated → Risk of RCE.  
- **Authentication Weaknesses**: No CAPTCHA, no MFA, weak password enforcement.  
- **SQL Injection Indicators**: Variances in login responses hint possible SQLi.  
- **Security Misconfigurations**: Exposed readme.html, misleading HTTP codes.  
- **No WAF Detected**: Site directly exposed to automated exploit attempts.  

---

## 📷 Proof of Concept (PoC)  

- BurpSuite captures (login requests, brute-force attempts).  
- Nmap SSL/TLS scan results.  
- WPScan output (outdated theme/plugins).  
- Screenshots of exposed files (e.g., `/readme.html`).  

*(Evidence included in `/evidence` folder of this repo)*  

---

## 🛡 Recommendations  

- **Patch Management**: Upgrade PHP ≥ 8.2, update Astra theme & plugins.  
- **Authentication Security**: Enforce MFA, strong password policy, CAPTCHA.  
- **Configuration Hardening**: Remove /readme.html, restrict sensitive files.  
- **Network Protection**: Deploy WAF (Cloudflare, ModSecurity).  
- **Monitoring**: Enable brute-force detection, implement incident response plan.  

---

## ✅ Conclusion  

The assessment revealed **critical and medium-risk vulnerabilities** that, if exploited, could lead to **RCE, site defacement, or data compromise**.  
By addressing outdated components, hardening authentication, and adopting a proactive vulnerability management strategy, **YoungSkilledIndia.com** can significantly strengthen its security posture.  

---

## 📂 Repository Contents  

- `README.md` (this file)  
- `/report` → Full penetration testing report (Major Project.docx)  
- `/evidence` → Screenshots, scan outputs, Burp logs  
