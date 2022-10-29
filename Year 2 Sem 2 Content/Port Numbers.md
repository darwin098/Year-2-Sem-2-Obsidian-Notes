- 16 bits long

## Categories
---
### Well-known Ports
- Range: 0 - 1023
- Used by system processes that provide widely used network services
- Run on servers and passively listens for connections 

### Registered Ports
- Range: 1024 - 49151
- Typically used by end user applications as ephemeral (short-live, temporary) source ports when contacting servers

### Dynamic, Private or Ephemeral Ports
- Range: 49152 to 65535
- Used for private, or customised services or temporary purposes and for automatic allocation of ephemeral ports

### Source & Destination Port Numbers
- When a sending host sends a data segment to the receiving host,
	- The sending process's port number becomes the source port number in the transport layer header
	- The sending host will use the Destination Port number in the Transport Layer header to indicate the recipient process at the receiving host
- When the receiving host replies to the sending host, the Source Port number and Destination Port number are swapped

#CybersecurityEssentials 
