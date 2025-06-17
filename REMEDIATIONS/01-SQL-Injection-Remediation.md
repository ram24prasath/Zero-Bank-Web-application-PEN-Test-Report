# SQL Injection Remediation

To remediate SQL Injection, first we need to understand how the injection takes place, what causes this vulnerability in the application. This type of vulnerabilities arises when an SQL query in the appplication dynamically queries the database with the `user-controllable data`. 

So what is this user-contorllable data?

In application sometimes, it takes input from the end-user of the application to perform certain actions. Attacker will try to use this input fields to find and exploit injection vulnerabilities.

