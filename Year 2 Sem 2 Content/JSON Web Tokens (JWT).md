- An open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object
- Prevents [[Cross-site Request Forgery (CSRF)]]

- We can make use of JSON Web Tokens to provide [[Token-Based Authentication]] by:
	- Performing [[Authentication]] through a login, and having our service return a token that can be used with subsequent requests

## JWT Structure
---
![[Pasted image 20221122004955.png]]

## JWT Authentication Flow
---
- A JSON Web Token contains 3 segments
- Each of these segments are separated by a single period
- All three segments are Base64 encoded

### JWT Header
- The first segment
- Comprises of:
	- The algorithm used
	- The token type
	- Eg { "alg": "HS256", "typ": "JWT"}

### JWT Payload (Body)
- The middle segment
- Usually encoded payload information in JSON format

### JWT Signature
- The final segment
- A cryptographically produced hash of the earlier segments
- Pseudocode to create the hash, based on a chosen algorithm:
	> HMACSHA256(base64UrlEncode(header) + base64UrlEncode(payload), 's3cr3t')
	


#EnterpriseSystemsDevelopment 