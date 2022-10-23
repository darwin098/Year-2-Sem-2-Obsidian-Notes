- Occurs when applications use unpatched 3rd party components with vulnerabilities
- Enables attackers to execute code, often at full permission levels

## Example
---
- Multipart parser in Apache Struts in 2.3.x and 2.5.x has incorrect exception handling and error-message generation during file-upload attempts, which allows remote attackers to execute arbitrary commands

## Prevention
---
- Continuously check all components used and monitor known security vulnerabilities and patch/remove them when they have known vulnerabilities
- Only obtain components from official sources over secure links and prefer signed packages to reduce the change of including a modified, malicious component

### NPM audit example
- When you invoke "npm audit" on a node project, a list of vulnerabilities is generated
- The vulnerabilities are flagged on the dependencies used in the project
- Such vulnerabilities should be fixed to a minimal

![[Pasted image 20221021163550.png]]


#EnterpriseSystemsDevelopment 