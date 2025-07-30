# 🛡️ Web Application Penetration Testing Report

## 🎯 Target: [YoungSkilledIndia.com](https://www.youngskilledindia.com/)

This repository contains the structured documentation and final report for a black-box **Web Application Penetration Test** conducted on [YoungSkilledIndia.com](https://www.youngskilledindia.com/), an educational platform offering professional development and language certification courses.

---

## 📌 Project Summary

- **Assessment Type**: Black-box Web Application Penetration Test  
- **Duration**: July 2025 – August 2025  
- **Tools Used**: Burp Suite (Community), Nmap, Sublist3r, WhatWeb, Wappalyzer  
- **Methodology**: Based on [OWASP Web Security Testing Guide (WSTG)](https://owasp.org/www-project-web-security-testing-guide/)  
- **CVSS Scoring**: Used to evaluate vulnerability severity

---

## 🧪 Testing Scope

| Category                     | Details                                              |
|-----------------------------|------------------------------------------------------|
| **Target URL**              | https://www.youngskilledindia.com/                   |
| **Test Type**               | Black-box (No source code access)                    |
| **Authentication**          | Public areas only (unauthenticated testing)          |
| **Permission**              | Written permission obtained from the site owner      |

---

## 🔍 Reconnaissance & Enumeration

Tools and techniques used for passive and active information gathering:

- `Sublist3r` for subdomain enumeration
- `WhatWeb` and `Wappalyzer` for tech stack fingerprinting
- `Nmap` for port and service discovery
- Passive DNS and SSL info via `crt.sh`, `Dig`, and `Nslookup`

---

## 🧰 Vulnerability Assessment

Vulnerabilities were tested under these OWASP WSTG categories:

- **WSTG-INFO-02**: Fingerprinting Web Server
- **WSTG-CONF-01**: Configuration Management Testing
- **WSTG-ATHN-01**: Testing for Credentials Transport over an Encrypted Channel
- **WSTG-SESS-02**: Session Fixation
- **WSTG-INPV-01**: Reflected Cross-Site Scripting (XSS)
- **WSTG-CLNT-05**: DOM-Based XSS (Client-Side)

*Note: Only non-intrusive tests were performed to comply with the responsible disclosure policy.*

---

## 📄 Report Contents

The full report includes:

- Executive Summary  
- Methodology & Tools  
- Vulnerability Details  
- CVSS v3.1 Risk Ratings  
- Screenshots & Proof of Concepts  
- Remediation Recommendations  

