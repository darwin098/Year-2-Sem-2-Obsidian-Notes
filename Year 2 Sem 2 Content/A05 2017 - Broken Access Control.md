- Occurs when permissions on resources are improperly enforced, allowing attackers to access unauthorized functionality or data

## Examples
---
- An attacker simply forces browsers to target URLs that require admin rights for access to the admin page
- If an unauthenticated or non-admin user can access the page, this is a flaw

## Prevention
---
- Adopt a "[[Deny-by-Default]]" mentality both during initial development and whenever new functionality or resources are exposed
- Validate permissions on every request

#EnterpriseSystemsDevelopment 