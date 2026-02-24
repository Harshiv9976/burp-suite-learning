## 🔐 Web Application Security Testing with Burp Suite (Altoro Mutual)

## 📌 Project Overview

This repository demonstrates practical web application security testing using Burp Suite Community Edition on the intentionally vulnerable demo application Altoro Mutual (testfire.net).

The goal of this project is to understand real-world vulnerabilities, how attackers exploit them, and how security analysts identify such issues during penetration testing / SOC analysis.

⚠️ Note:
Altoro Mutual is a legal demo application designed for security training and learning purposes only.

🛠 Tools Used

Burp Suite Community Edition

Web Browser (Chromium-based)

Demo Target: Altoro Mutual (testfire.net)

## 🔍 Vulnerabilities Demonstrated
## 1️⃣ Brute Force / Credential Testing (Burp Intruder)
<p align="center">
  <img src="screenshourts/attack1.png" width="800">
</p>
<p align="center">
  <img src="screenshourts/attack2.png" width="800">
</p>

Used Sniper / Pitchfork attacks

Tested multiple username & password combinations
Analyzed:
HTTP status codes
Response length
Redirect behavior

Identified weak authentication handling

## 2️⃣ SQL Injection (Authentication Bypass)

Injected SQL payloads into login parameters

Example:

' OR '1'='1

Successfully bypassed login and accessed Admin panel

Demonstrates lack of proper input validation

## 3️⃣ Cross-Site Scripting (XSS)

Reflected XSS via search functionality

Payload example:

<script>alert('XSS Attack')</script>

JavaScript executed in browser

Confirms missing output encoding

## 4️⃣ Burp Decoder Usage

Encoded & decoded data

Hash analysis

Useful for understanding:

Tokens

Encoded parameters

Obfuscated values

## 5️⃣ Intercepting Requests (Burp Proxy)

Intercepted HTTP requests

Modified parameters before forwarding

Observed server responses in real time

📸 Screenshots Included

Burp Intruder attack results

SQL Injection login bypass

XSS popup execution

Decoder output

Intercepted HTTP requests

(All screenshots are added for learning & documentation purposes)

## 🎯 Learning Outcomes

Hands-on experience with Burp Suite

Understanding of common OWASP vulnerabilities

Request/response analysis

Practical penetration testing workflow

SOC / VAPT interview-ready knowledge

## 📊 Risk Summary Table (Burp Suite)

| Vulnerability Name               | Description                                                                                           | Severity  | Status |
| -------------------------------- | ----------------------------------------------------------------------------------------------------- | --------- | ------ |
| **SQL Injection**                | Improper input validation allows attackers to inject malicious SQL queries and bypass authentication. | 🔴 High   | ❌ Open |
| **Brute Force Attack**           | No rate limiting or account lockout enables unlimited login attempts using Burp Intruder.             | 🔴 High   | ❌ Open |
| **Cross-Site Scripting (XSS)**   | Unsanitized user input allows execution of malicious JavaScript in the victim’s browser.              | 🟠 Medium | ❌ Open |
| **Weak Authentication Controls** | Application fails to enforce strong authentication mechanisms.                                        | 🟠 Medium | ❌ Open |
| **Improper Input Validation**    | User inputs are not properly validated, increasing multiple attack vectors.                           | 🟠 Medium | ❌ Open |
| **Sensitive Data Exposure**      | Application responses may expose sensitive information in HTTP traffic.                               | 🟡 Low    | ❌ Open |
| **Lack of Security Headers**     | Missing HTTP security headers increases risk of client-side attacks.                                  | 🟡 Low    | ❌ Open |

## 📚 Disclaimer

This project is created strictly for educational and ethical purposes.
Do NOT use these techniques on real-world systems without written authorization.

## 👤 Author

Harshiv Patel
