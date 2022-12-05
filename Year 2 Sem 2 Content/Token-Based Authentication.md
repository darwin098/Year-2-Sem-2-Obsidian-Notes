- In token-based authentication, [[JSON Web Tokens (JWT)]] are used for authentication

## Steps
---
1) User submits form to server
2) Server creates an encrypted [[JSON Web Tokens (JWT) | JWT]] token for users
3) Server sends back [[JSON Web Tokens (JWT) | JWT]] token to user
4) JWT is stored in local storage of user's browser
5) Whenever user makes a request to view a page, [[JSON Web Tokens (JWT) | JWT]] is sent along with it
6) Server validates [[JSON Web Tokens (JWT) | JWT]] and then sends required response back to the client

- The user's state is stored in the [[JSON Web Tokens (JWT) | JWT]] on the client side
- When user logs out, the token is deleted form the client's local storage
- Thus most of the data is stored in the client side and accessed directly instead of sending requests to the server

![[Pasted image 20221122003221.png]]

#EnterpriseSystemsDevelopment 