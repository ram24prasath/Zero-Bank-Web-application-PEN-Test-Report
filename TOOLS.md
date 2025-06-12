# 🧰 Tools Used in Penetration Testing

This document outlines the tools used during the penetration testing of the Zero Bank Web Application, along with a brief explanation of their roles and use cases.

---

1. Burp Suite (Community Edition)

   Modules Used:
  
  - Proxy – Intercept and manipulate traffic.
  - Repeater – Manual testing of payloads.
  - Intruder – Automated payload injection.

---

2. WhatWeb 

   Purpose: Web technology fingerprinting.

   Use Cases:
   - Identify frameworks, server types, CMS, and JavaScript libraries in use.
   - Determine tech stack to tailor specific attacks.
  
---

3. Dirb / Gobuster

   Purpose: Brute-force directory and file discovery.

   Use Cases:
   
   - Uncover hidden directories and endpoints
   - Find sensitive files (e.g., .bak, .git, admin, manager,debug)

   
  
---

4. nmap

   Purpose: Network and port scanning.

   Use Case:

   - Identify open ports (if external services were in scope)
   - Service enumeration and OS fingerprinting
  
---
