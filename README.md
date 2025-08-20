# 🛡️ Web Application Penetration Testing of YoungSkilledIndia.com

[cite_start]This report details a black-box penetration test conducted on the YoungSkilledIndia.com web application[cite: 3]. [cite_start]The assessment's objective was to identify security vulnerabilities and provide actionable recommendations for remediation[cite: 42, 45].

---

## 📌 Project Overview

* [cite_start]**Project Title**: Web Application Penetration Testing [cite: 3]
* [cite_start]**Target Application**: [YoungSkilledIndia.com](https://www.youngskilledindia.com/) [cite: 55]
* [cite_start]**Assessment Type**: Black-Box Engagement Model (no prior knowledge of internal systems) [cite: 48, 57]
* [cite_start]**Methodology**: Aligned with industry standards including OWASP Web Security Testing Guide (WSTG), OWASP Top 10, NIST SP 800-115, and PTES[cite: 43, 76].

---

## 🧪 Testing Scope & Rules of Engagement

| Category | Details |
| :--- | :--- |
| **Target URL** | [cite_start]`https://www.youngskilledindia.com/` [cite: 55] |
| **Target IP Address** | [cite_start]`195.35.44.229` (Hostinger infrastructure) [cite: 56] |
| **Test Type** | [cite_start]Black-box (unauthenticated external testing) [cite: 57] |
| **Forbidden Actions** | [cite_start]Included Denial of Service (DoS/DDoS) attacks, social engineering, and disruption of production systems[cite: 59, 60, 61, 64]. |

---

## 🔍 Key Findings & Vulnerability Summary

[cite_start]The assessment identified several vulnerabilities, with severity ratings assigned based on the Common Vulnerability Scoring System (CVSS v3.1)[cite: 52, 82].

| OWASP Category (2021) | Severity | Description / Observation |
| :--- | :--- | :--- |
| **A06: Vulnerable & Outdated Components** | High | [cite_start]Outdated Astra theme and end-of-life PHP 7.4 were identified, posing a high risk of remote code execution or data breach[cite: 87, 325, 326]. |
| **A03: Injection** | Medium | [cite_start]The login form showed response anomalies suggesting it may be vulnerable to SQL injection, potentially leading to data exfiltration[cite: 87]. |
| **A04: Insecure Design** | Medium | [cite_start]The application lacks MFA, CAPTCHA, and account lockout policies, making it susceptible to brute-force and credential stuffing attacks[cite: 87, 235, 236]. |
| **A07: Identification & Authentication Failures** | Medium | [cite_start]No brute-force prevention or strong password policies were enforced, increasing account takeover risk[cite: 87]. |
| **A08: Software & Data Integrity Failures** | Medium | [cite_start]The absence of integrity verification for plugins and themes could lead to supply chain attacks or backdoors[cite: 87]. |
| **A05: Security Misconfiguration** | Low | [cite_start]While no sensitive data was exposed, some server responses could aid attackers in future attempts[cite: 87]. |
| **A02: Cryptographic Failures** | Low | [cite_start]The application correctly enforces HTTPS and strong TLS protocols (TLS 1.2/1.3), posing minimal risk[cite: 87, 167]. |

---

## 🧰 Tools & Technologies Utilized

[cite_start]A combination of industry-standard tools was used to conduct the reconnaissance, scanning, and vulnerability analysis phases[cite: 70]:

* [cite_start]**Proxy Tools**: Burp Suite Community Edition [cite: 71]
* [cite_start]**Reconnaissance**: Sublist3r, Whois, crt.sh, theHarvester [cite: 72]
* [cite_start]**Scanning & Enumeration**: Nmap, WPScan, WhatWeb, Wappalyzer [cite: 73]
* [cite_start]**Supporting Utilities**: Dig, Dirsearch, SSL Labs [cite: 74]

---

## 📄 Report Contents

The full project report provides an in-depth analysis of the security assessment and includes the following sections:

* [cite_start]**Executive Summary**: A high-level overview of the engagement's purpose and key findings[cite: 12, 46].
* [cite_start]**Scope & Rules of Engagement**: Defines the target environment, boundaries, and permitted actions[cite: 13, 53].
* [cite_start]**Methodology**: Details the systematic approach and phases of the penetration test[cite: 18, 75].
* [cite_start]**Information Gathering**: Outlines the data collected during passive and active reconnaissance[cite: 20, 88].
* [cite_start]**Technical Findings**: Provides a detailed breakdown of each identified vulnerability, mapped to the OWASP Top 10[cite: 25, 123].
* [cite_start]**Recommendations**: Offers specific, actionable steps to remediate the identified vulnerabilities and strengthen the application's security posture[cite: 34, 457].
* [cite_start]**Conclusion**: Summarizes the overall security risk and the importance of proactive security maintenance[cite: 35, 478].
* [cite_start]**Appendices**: Contains supplementary evidence, including scan results and Proof-of-Concept screenshots[cite: 36, 483].
