# Insecure Direct Object Reference

IDOR occurs when an application provides direct access to objects based on user-supplied inputs. As a result of this vulnerability attackers can bypass authorization giving them access to information that they normally do not have.

In Other words, IDOR allows attackers to directly access resources by modifying value of a paramater that is directly pointed to an object.

## IDOR Vulnerability in ZERO Bank Web application

After logging in to the Zero Bank Application, navigate to `Account Activity` tab. Here we can see in the URL that there is a direct reference to an object `accountId`.

![IDOR1](/SCREENSHOTS/IDOR1.png)

Because the application make parameter exposed in the URL, attacker can modify the value of the parameter to check the response from the server.

![IDOR2](/SCREENSHOTS/IDOR2.png)

We can see that by changing `accountId=2`, attacker is able to retrieve account activities of a different user from the database. Similarly we can try different parameter values.

![IDOR3](/SCREENSHOTS/IDOR3.png)

---
