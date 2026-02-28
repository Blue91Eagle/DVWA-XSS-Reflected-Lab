# DVWA Reflected XSS Lab

## 📌 Project Overview

This project demonstrates a Reflected Cross-Site Scripting (XSS) vulnerability discovered in DVWA (Damn Vulnerable Web Application) running in a controlled lab environment.

Environment:
- Kali Linux
- Metasploitable 2
- DVWA
- VirtualBox Lab
- Security Level: Low

---

## 🔎 Vulnerability Details

- Vulnerability Type: Reflected Cross-Site Scripting (XSS)
- Endpoint: /dvwa/vulnerabilities/xss_r/
- Method: GET
- Parameter: name

---

## 🧪 Proof of Concept

Injected payload:

```
<script>alert(1)</script>
```

Result:
The browser executed JavaScript and displayed a popup alert box with value "1".

This confirms that user input is reflected without proper sanitization.

---
## 📸 Screenshots

![XSS Input](screenshots/xss-input.png)
![XSS Alert](screenshots/xss-alert.png) 
---
## ⚠️ Impact

An attacker could potentially:
- Steal session cookies
- Perform phishing attacks
- Inject malicious scripts
- Redirect users

---

## 🛡️ Remediation

To prevent XSS:
- Escape user input before rendering
- Use proper output encoding
- Implement Content Security Policy (CSP)
- Validate and sanitize inputs

---

## ⚖️ Legal Disclaimer

This project was conducted in a controlled lab environment using DVWA.
No real systems were targeted.
