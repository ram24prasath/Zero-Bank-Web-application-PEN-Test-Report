# SQL Injection Remediation

To remediate SQL Injection, first we need to understand how the injection takes place, what causes this vulnerability in the application. This type of vulnerabilities arises when an SQL query in the appplication dynamically queries the database with the `user-controllable data`. 

So what is this user-contorllable data?

In application sometimes, it takes input from the end-user of the application to perform certain actions. Attacker will try to use this input fields to find and exploit injection vulnerabilities.

## How to prevent against SQL Injection

Like we discussed earlier, from the anotomy for SQLi vulnerability we can understand that using unvalidated input from user and is simply appened to the query is the key issue. To avoid this we can use one of the following defense mechanisms.


### Option 1: Use of Prepared statements with parameterized queries

Prepared statement compared to dymanic queries are simple, easy to write and understand and with parameterized queries, it separates the SQL query and user-input. 

In this case developers of the application are forced to write the SQL query first and pass the input to the query later, which help the application understand which part is SQL code and which is user-input, thus when attacker injects an SQL query, it will not be executed.

### Option 2: Stored Procedures

Similar to Prepared statement, Stored procedures also helps application differentiate between sql query and user-supplied input. Only difference is that the prepared sql statement is stored in the database itself.

 While stored procedures can provide security benefits, they are not guaranteed to prevent SQL injection attacks.  The same kinds of vulnerabilities that arise within standard dynamic SQL queries can arise if any SQL is dynamically constructed within stored procedures.

### Allow list input validation

This defense technique is used to detect unauthorized input before using it in dynamic SQL query. 

