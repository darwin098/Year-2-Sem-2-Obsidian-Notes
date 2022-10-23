- Occurs when user-supplied data is deserialized by a website
- Allows an attacker to manipulate serialized objects in order to pass harmful data into the application code

## Example
---
- A ReactJS app interacts with Java Spring Boot backend by passing serialized Java objects with each request
- An attacker then uses a deserialization tool to gain access to execute code on the server

## Prevention
---
- Do not accept serialized objects from untrusted sources or use serialization mediums that only permit primitive data types
- If above not possible
	- Implement integrity checks such as digital signatures on any serialized objects to prevent hostile object creation or data tampering
	- Sanitize the data of a serialized object through filtering or validation

#EnterpriseSystemsDevelopment 