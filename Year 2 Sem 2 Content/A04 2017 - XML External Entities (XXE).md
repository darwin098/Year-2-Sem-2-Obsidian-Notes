- Occurs when outdated or poorly configured [[XML]] processors that evaluate external entity references within [[XML]] documents are used
- This allows access to internal file shares, port scanning, remote code execution

## Examples
---
- In XML, there is a reference to a file location on the system
- If the reference is re-directed to a valid file containing secret data, the data becomes compromised

![[Pasted image 20221021134346.png]]

## Prevention
---
- Use less complex data formats such as JSON, and avoid serialization of sensitive data
- Patch or upgrade all XML processors and libraries in use by the application or on the underlying operating system
- Disable XML external entity and DTD processing in all XML parsers in the application

#EnterpriseSystemsDevelopment 