- In session-based authentication, the server is responsible for the authentication 
- The client does not know what happens at the server side after sending a request

## Steps
---
1) User submits form to server
2) Server creates a session for the user and stores session data in server memory or cached storage
3) Server sends back a session ID to user, and this session ID is stored in a cookie in the client's browser
4) Whenever user makes a request to view a page, this cookie is automatically sent along with it
5) Server verifies user's credentials by using the cookie and comparing it with session data stored in server memory
6) When user logs out, session data is deleted from server memory and storage

![[Pasted image 20221122002155.png]]

#EnterpriseSystemsDevelopment 