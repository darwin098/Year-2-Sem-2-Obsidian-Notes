- Occurs when untrusted data is sent to an interpreter as part of a command or query, leading to execution of unintended commands

## Examples
---
- [[SQL Injection]]

## Prevention
---
- Use a safe API which avoids the use of interpreter entirely, or provides a parameterized interface or migrate to use Object Relational Mapping Tools (ORMs)
- Use positive or "whitelist" server side input validation or escaping (Incomplete defences and usually not preferred)

#EnterpriseSystemsDevelopment 