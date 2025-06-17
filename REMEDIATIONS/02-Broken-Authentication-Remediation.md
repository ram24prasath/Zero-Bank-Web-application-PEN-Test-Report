# Broken Authentication Remediation

Broken authentication is a severe vulnerability that enables threat agents to perform brute force and dictionary attack against an authetication mechanism of an application. This vulnerability prevail in an application due to weak design and implementation of identity and access controls. All statefull applications use sessions to authenticate the user and access control.

***Impact***:

  If attackers are able gain access to few accounts or just one admin account, they can compromise the entire system. Impact will be severe based on the domain of the application, such as identity theft, social security frauds and discloure of sensitive information.

## How to find if the application is vulnerable?

Identity and access management, authentication, session management are critical to most operation of the application. Compromise in any of these management leads to broken authentication. 

The application has weak authenthication if it has any of the following:

- Permits brute force or automated attacks.
- Allows default, weak or well-known password.
- use weak/ ineffective password reset mechanisms.
- use plaintext or weak hashing for storing passwords.
- Missing or ineffective Multi factor authentication.
- Exposing Session ID.
- Predictable Session Id.


## How to prevent?

- Implement Multi factor authentication wherever possible.
- Do not allow default, weak or common passwords.
- Implement password complexity and force users to change password periodically.
- Limit login failed attempts. Log all failed alerts and report to admin.
- use server-side safe session ID.
- Randomize session ID, store it safely and invalidate after logout.

---
