- Occurs when insecure default configurations or incomplete configurations are used
- Allows attackers to access default accounts, unused pages etc to gain unauthorized access or knowledge of the system

## Example
---
- Application server comes with sample applications that are not removed from the production server
- These sample applications have known security flaws that attackers use to compromise the server.
- If one if these applications is the admin console, and default accounts weren't changed, the attacker can log in with one of the default passwords and take over

## Prevention
---
- Create a minimal platform without any unnecessary features, components, documentation and samples.
- Remove or do not install unused features and frameworks
- Use automated processes to verify the effectiveness of the configurations and settings in all environments

#EnterpriseSystemsDevelopment 