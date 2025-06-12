# 🛠️ Methodology

This document outlines the methodology used to perform a penetration test on the Zero Bank Web Application. The goal of the assessment was to identify and validate security vulnerabilities that could be exploited by malicious actors. The test followed industry-standard frameworks and manual techniques tailored for web application testing.

---

1. Information Gathering (Reconnaissance)

- Collected application metadata such as server headers, technologies used (via tools like WhatWeb, Wappalyzer, and Burp Suite).
- Identified accessible endpoints and parameters using:
    - Browser exploration
    - Burp Suite's Spider
    - Tools like Dirb, Gobuster
 
---

2. Threat Modeling

    Mapped out application attack surface including:
     - Login functionalities
     - Session management
     - Account operations (transfer, bill payment, account summary)
     - Identified potential user roles and privilege boundaries (e.g., unauthenticated vs. authenticated user).
  

---

3. Vulnerability Analysis

    Tested for common web application vulnerabilities using a combination of manual and automated techniques based on OWASP Top 10:
     - SQL Injection (SQLi)
     - Cross-Site Scripting (XSS)
     - Broken Authentication
     - Insecure Direct Object References (IDOR)
     - Sensitive Data Exposure
     - Debug Info Disclosure

    Tools used:
      - Burp Suite (manual testing, Intruder, Repeater)
      - OWASP ZAP (automated scanning)
      - Nmap (for port/service discovery if applicable)
      - Gobuster, dirb
  
   ---

   4. Exploitation

    Attempted safe, controlled exploitation of identified vulnerabilities to validate their impact.

    Examples include:
     - Extracting user data via SQLi
     - Triggering JavaScript execution through XSS
     - Accessing other users' account information via IDOR
  
   ---

   5. Reporting

    Documented each vulnerability with the following structure:
     - Title
     - Severity
     - Affected Endpoint/Function
     - Proof of Concept (PoC)
     - Impact
     - Recommendation
     - Screenshots and Burp Suite logs included where relevant.
  
   ---

   6. Remediation Guidance

    Provided fix recommendations aligned with secure development practices:
      - Input validation and output encoding
      - Proper session management
      - Role-based access control (RBAC)
      - SQL query parameterization
