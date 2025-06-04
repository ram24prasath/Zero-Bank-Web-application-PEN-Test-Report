# Broken Authentication

Broken authentication refers to vulnerabilities within an application's authentication mechanism that allows attackers to impersonate legitimate users
or byapss security controls.

Broken Authentication is in one of the OWASP Top 10 Vulnerabilities. 

From the gobuster enumeration results we can see some interesting directories that could reveal information, we will try to explore manually traverse
to these directories.

using `/admin` path:

![admin](SCREENSHOTS/Broken_Auth_admin.png)

As we can see, now we are able to see a admin page basically without any authentication at user end. We can naviagate through this page and extract
information that could be useful to exploit further.

![admin2](SCREENSHOTS/Broken_Auth_admin2.png)

