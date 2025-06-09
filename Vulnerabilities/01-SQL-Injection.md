# SQL Injection

SQL Injection is type of vulnerability which involves an attacker exploting an SQL query used in an application which is used retrieve information from the webserver, if the SQL statements are improperly used, atatckers can exploit by retrieving sensitive unauthorized data or modify data in the webserver.

SQL Injection usually happens via the input data from the client to the application.

The main consequences of SQLi:

- Confidentiality: SQL databases holds sensitive informations, SQLi could result in loss of confidentiality.
- Integrity: SQLi attacks allows the possibility of altering or tampering database information.
- Authentication: If poorly written SQL statements are used for authentication process, it could lead to broken authentication.
- Authorization: If authorization of an application is held in SQL database, it may lead to privilege escalation.

