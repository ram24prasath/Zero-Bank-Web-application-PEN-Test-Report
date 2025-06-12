# 🎯 Target and Scope

This document outlines the target system and scope boundaries for the penetration testing engagement conducted on the Zero Bank Web Application. Clear definition of scope ensures a focused, responsible, and legally compliant testing process.

---

✅ In-Scope Targets

| Target Component                  | Description                                                                 |
| --------------------------------- | --------------------------------------------------------------------------- |
| `http://zero.webappsecurity.com/` | Main web application hosted for simulation-based testing                    |
| Application Features Tested       | Login, Registration, Transfers, Bill Payment, Account Summary, Contact Form |


Only the functional application components under the main domain were tested.

---

🎯 Scope of Testing

The following areas were covered in the test:

- Authentication and Session Management
- Input Validation & Injection Flaws (SQLi, XSS)
- Broken Access Control (IDOR, vertical/horizontal privilege issues)
- Sensitive Data Exposure
- Client-side Security (DOM XSS, insecure JavaScript)
- Security Misconfigurations (debug messages, header issues)

---

⚠️ Limitations

  The test was conducted from an unauthenticated and authenticated user perspective only.

  Since this is a training platform, findings are limited to intentionally built vulnerabilities and may not reflect real-world implementations or configurations.

---

👨‍💻 Engagement Type

  - Type: Black-box Web Application Penetration Test
  - Access Provided: Publicly available test environment
  - Environment: No production systems were involved
  - Test Duration: TBD
