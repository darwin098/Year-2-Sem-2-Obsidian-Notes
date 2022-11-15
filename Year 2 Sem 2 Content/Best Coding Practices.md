# When Coding

## First apply
---
- [[SQL Injection#^4940e7| Parameterized Queries]]
- [[SQL Injection#^93266f | Stored Procedures]]

## Additional Protection
---
- Perform [[SQL Injection#^ddcfb6 | Input validation]] and whitelisting with regular expressions
	- Datatype checks
- [[SQL Injection#^cb977f | Escape Input]]

# When configuring the database
- Create accounts with strong passwords for database access
- Create accounts with least privileges on the database for the client applications, allowing access to required data for performance of required tasks only
- Ensure connections to database from client applications are encrypted

# Separate data and command when sending SQL query
- Separate the command and data parts of the query by sending them separately
- Leaves no room for misinterpretation and is a good way to protect against injection
- Also provides a speed boost on queries that run many times because you can reuse the same procedure

# Configure least privilege / separate database accounts
- Using different database accounts in your codes ensure that even if the attacker manages to gain access to your database, he will have limited access to it based on the grants given to that role

#EnterpriseSystemsDevelopment 