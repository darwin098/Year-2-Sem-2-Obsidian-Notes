- A web security vulnerability that allows attackers to induce users to perform actions that they do not intend to perform on a web service they are already authenticated to
- Attackers make use of the automated sending of session cookies by web browsers to bypass the same origin policy, designed to prevent web servers from interfering with one another

## Execution
---
1) Trick the victim to click a link or load a page
2) Send a legitimate looking request from victim's browser to target website
	- Request is sent with values chosen by the attacker including any cookies that the victim has associated with that website
3) Target website assumes request is genuine since it originated from victims browser and fulfils the request

## CSRF Vulnerabilities
---
Many CSRF vulnerabilities arise due to mistakes made in the validation of CSRF tokens
- Validation of CSRF token depends on request method
- Validation of CSRF token depends on token being present
- CSRF token is not tied to the user session
- CSRF token is tied to a non-session cookie
- CSRF token is simply duplicated in a cookie

## Prevention
---
- [[JSON Web Tokens (JWT)]] is generally seen as strong against CSRF attacks
- Generally, CSRF happens when a browser automatically adds headers and then makes the session authenticated
- Bearer tokens, or other HTTP header based tokens that need to be added manually would prevent CSRF attacks
- However if you have a XSS vulnerability, an attacker could still access the tokens

#EnterpriseSystemsDevelopment 