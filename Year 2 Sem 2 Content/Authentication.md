- The process or action of proving or showing something to be true, genuine, or valid
- I.e. Confirms users are who they say they are

## Types of Authentication
---
- [[Session-Based Authentication]]
- [[Token-Based Authentication]]

## Usage
---
- In modern web applications, [[JSON Web Tokens (JWT) | JWTs]] are widely used as it scales better than session-based cookies
- With session-based authentication, server memory is used to store user data
	- This might be an issue when a large number of users access the application at once
- With [[JSON Web Tokens (JWT) | JWT]], user information is sent along with every request
	- even if it is encoded, sensitive information should be avoided to prevent security attacks

#EnterpriseSystemsDevelopment 