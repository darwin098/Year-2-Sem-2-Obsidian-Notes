
## 15 mins vid
---
1) Show how to exploit the vulnerabilities in the given insecure web app
	- Show 6 vulnerabilities
2) Show how to remedy those 6 vulnerabilities
3) Start off the vid by giving off the definition of the vulnerability
	- I.e. First I am going to show how this web app contains an XSS vulnerability
	- XSS vulnerability is a vulnerability whereby...
	- Go on to show how you can execute an exploit for that category of vulnerability
	- Finally you will wrap up with a quick demo of how you will patch it, you can show the important parts of it if no time

## Vulnerability Assessment Report
---
- Marks for 6 vulnerabilities:
	- Definition
	- Showing steps to exploit
	- Showing steps to remedy
	- Include relevant screenshots and code snippets
	- Showing evidence that the vulnerability is no longer there
		- [[A01 2017 - Injection]]
		- [[A02 2017 - Broken Authentication]]
		- [[A03 2017 - Sensitive Data Exposure]]
		- [[A05 2017 - Broken Access Control]]
		- [[A07 2017 - Cross-Site Scripting (XSS)]]
		- [[A10 2017 - Insufficient Logging & Monitoring]]

## Code Review (Bonus Marks)
---
- Point out what code is inefficient etc.

## Test
---
### SQL Injection
##### Lack of parameterized queries
- userService.js, recordID is not used as a parameterized query, leading to possible SQL injection
- User can access backend API through the network inspector
- User can look for each specific user's information by injecting sql through the search parameter
- localhost:5000/api/user/design/ API
- I.e. 0 union select * from user where user_id=101 at the back of the url

###### Fix
- Usage of parameterized queries for the API

### Broken Authentication
##### Token stored in Local Storage
- Tokens, user_id and role_name is stored in the local storage, allowing for easy stealing of user identity
- Hacker can then go to direct links and set himself as administrator for example

###### New Fix
- Password check middleware using input password and token user id
- Password check is there for when you enter a page to update a single user's privileges
- If the password fails, the user cannot update or see any data of the user.

### Sensitive data exposure
- password can be seen in interception of form request

###### Fix
- Sensitive data is being transmitted in plain text as seen in burp suite. With encryption, data is no longer able to be easily intercepted.
- Add in encryption from backend to frontend to encrypt the sensitive data (password and token)

### Broken Access Control
##### Normal users can access admin pages
- I.e. Kelly, a normal user, can access the manage users page to make herself or someone else an admin
- She can also make others not an admin, inflicting serious damage
- Admin checks are needed to be implemented for admin pages and admin functions

###### Fix
- Script placed in head to check role before all else, and redirect them to home page when unauthorized
- Add in a middleware to check token role and if its not admin reject them

### XSS
##### Lack of input validation (when updating design details)
- Design title and description has no input sanitization and can allow scripts to be entered and saved

###### Fix
- Input validation middleware added
- Output sanitization escaping performed

### Insufficient Logging and Monitoring
##### After setting up input validation etc
###### Fix
- Add on the email function to alert admin on access control failures and input validation failures