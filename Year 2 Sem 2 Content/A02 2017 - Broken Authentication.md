- Occurs when credential verification or session management are poorly implemented
- Allows attackers to compromise passwords or session tokens to assume user identities 

## Prevention
---
- Implement weak password checks, such as testing new or changed passwords
- Perform re-authentication for sensitive transactions such as updating of password or monetary transfers
- Ensure a new random session ID with high entropy after login
- Session IDs should not be in the URL, and be securely stored and invalidated after logout, idle, and absolute timeouts

#EnterpriseSystemsDevelopment 
