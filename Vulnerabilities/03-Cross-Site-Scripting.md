# Cross Site Scripting (XSS)

XSS is a type of attack where attacker injects malicious scripts into the web application via user input fields.

Attacker can send the malicious code to the user's browser and it will get executed without much checks because the as far the user is concerned the
code came from the trusted web application.

This malicious script can steal user's data, session, cookies or other sensitive information retained by the browser from the site.

XSS atatcks can be categorised into 3 categories.
- Reflected XSS
- Stored XSS
- DOM-based XSS

1. Reflected XSS are those where injected scripts are reflected off the web server, such as in error message, search result, or any other response.
2. Store XSS, attack where injected malicious script is permanently stored on the web server, such as in database, message forum, comment fields.
   When the information stored is retrieved from the database bu the user, the script is executed in the user's browser.
3. Blind XSS:  It generally occurs when the attacker’s payload saved on the server and reflected back to the victim from the backend application.
   For example in feedback forms, an attacker can submit the malicious payload using the form, and once the backend user/admin of the application will open the attacker’s submitted form via the backend application,
   the attacker’s payload will get executed.

## Exploiting Stored XSS on Zero Bank Application

The stored xss vulnerability if found in a input form in the path /admin of the web application. 
Previously using enumeration techniques, we found the hidden `/admin` page, please refer 02-Broken-authentication.md file for more details.

After visting the admin page, navigate to the currencies section and here you find the 'add currency' section. Upon clicking that you will be presented a input form.

I have found that the input field `country` is suseptible to xss type of vulnerability, crafted a payload to store a malicious script in the database.

```bash
<svg onload=alert("Hacked")>
```

![XSS_payload](/SCREENSHOTS/XSS1.png)

What this script does is whenever a user visits the `/admin/currencies` page, this script will executed and create a pop-up alert. 

![XSS_alert](/SCREENSHOTS/xss2.png)


Although this maybe seem harmless from a user's perpective, this script is just to showcase the presence of this type vulnerability. Attacker can craft payloads to steal sensitive information that the application is retreiving from the database to the user's browser. This information can be stolen in the form of cookies, sessions etc.

This type of xss is stored permanently in the database and whenever a user is visting the page, the atatcker's script will be executed in the background.

![XSS_DB](/SCREENSHOTS/xss3.png)

## Exploiting Reflected XSS on Zero Bank Application

Reflected attacks are those where the injected script is reflected off the web server, such as in an error message, search result, or any other response that includes some or all of the input sent to the server as part of the request.

I found one of the input form in the page `/add-new-payee` vulnerable to reflected xss using the simple crafted input. 

```bash
<script>alert(1)</script>
```

This is one of most basic script commonly injected into input forms to check if the form is vulnerable to cross site scripting.

![reflected_XSS1](/SCREENSHOTS/reflected_xss1.png)

The field payee description is the recipient of the payload. We can see the alert pop-up immediately once we submit the input form.

![reflected_XSS2](/SCREENSHOTS/reflected_xss2.png)
