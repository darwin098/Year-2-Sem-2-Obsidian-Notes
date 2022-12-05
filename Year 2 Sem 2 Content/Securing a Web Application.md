## Prevents
---
- [[SQL Injection]]
- [[Cross-site Scripting (XSS)]]
- Data issues in database

## Step 1: Input Validation
---
- AKA data validation
- The proper testing of any inputs supplied by the user or application
- Prevents improperly-formed data from entering an information system

- Should be done as early as possible
- Invalid and malicious inputs should not be processed

- Inputs should **always** be validated on the server side

### Techniques
- Regular expressions (Whitelisting)
- Type checks
- Blacklists

### Application
- Apply input validation as middleware functions
	- Use regular expressions to check for acceptable input patterns


## Step 2: Output Sanitization
---
- How an application cleans and modifies the output data
- If an application has improper output handling, the output data may be consumed leading to vulnerabilities and unintended actions

- Should be done as late as possible

- Outputs should **always** be validated on the server side
- If user-supplied data is processed by JavaScript, then output sanitization will be needed on the client side as well

### Techniques
- Applying filters / middleware
	- String replace functions to convert characters like "<" and ">"
	- String remove functions
- Escaping data
	- Strips out unwanted data like malformed HTML or script tags, preventing the data from being seen as code
	- Helps secure data prior to rendering it for the end user

### Application
- Apply output sanitization as middleware functions

#EnterpriseSystemsDevelopment 