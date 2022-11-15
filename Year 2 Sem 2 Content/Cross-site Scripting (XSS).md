- An injection attack where the attacker attaches malicious code onto a legitimate website that will execute when the victim loads the website
- The attack is not aimed at the web application, but at the users of vulnerable applications

## Uses
---
- Steals cookies of users and impersonate them online
- Gain access to APIs that contain geolocation coordinates, webcam data, and other sensitive information

## Types
---
### Reflected (Non-persistent) XSS

^0335c5

- The malicious script comes from the current HTTP request

- The simplest variety of XSS
- Arises when an application receives data in a HTTP request and includes the data within the immediate response in an unsafe way
- The malicious code is executed by a victim's browser, and the payload is not stored anywhere
- Returned as part of the server's HTML response

### Stored XSS

^c327f0

- The malicious script comes from the website's database

- Occurs when a web application stores user input and later serves it to others
- Malicious code is executed by a victim's browser, and the payload is stored on the server. It is returned as part of the response from the HTML that a server sends
- Relatively more dangerous as it is self-propagating, and anyone that now visits the site is at risk

### DOM-based XSS

^fd7b5e

- The vulnerability exists in client-side code rather than server-side code

- Document Object Model-based Cross-site Scripting
- Code attacks the DOM of the HTML page, accessing properties and values 
- Malicious code is executed by a victim's browser, and the payload might not reach the server
- Hence, does not get detected by intrusion systems

## Examples
---
- Malicious code can be inserted by:
	- Adding it to the end of a URL
	- Getting it stored into a server database which displays as user-generated content'
- Most common locations:
	- Search fields that echo a search string back to the user
	- Input fields that echo user data
	- Error messages that return user supplied text
	- Hidden fields that contain user supplied data
	- Any page that display user supplied data
		- Message boards
		- Free form comments
	- HTTP Headers


#EnterpriseSystemsDevelopment 