- Occurs when untrusted data is included in a new web page without proper validation or escaping, allowing attackers to execute malicious scripts in the victim's browser

## Example
---
- There is a URL such as 
```
http://www.sgmart.com/search?q=milk
```
which returns a HTML document containing the fragment
```
<p>Your search for 'milk' returned the following results:</p>
```
- An attacker could inject malicious code as part of the query term
```
http://www.sgmart.com/search?q=milk+%3Eevil_script()%3C/script%3E
```
so that when a victim loads this page, the browser will execute the "evil_script " fragment

## Prevention
---
- Sanitize and validate all client-supported input data
- Use frameworks that automatically escape XSS by design, such as React JS

#EnterpriseSystemsDevelopment 