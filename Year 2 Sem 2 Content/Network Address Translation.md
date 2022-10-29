- IP packets from within private networks into the internet is "translated" from the private IP address to a public IP address by the router before it's forwarded to the internet
- For vice versa, the IP address is converted from public to private
- Done by modifying the IP packet header

## Types
---
### 1) Static
- The mapping of private-public IP addresses is fixed, on a one-to-one basis
- A private IP address is always translated to the same public IP address
- Useful when a device in the private network needs to be accessible from the public network.

### 2) Dynamic
- The mapping of private-public IP addresses is dynamic
- A private IP address is translated to the first public IP address.
- Can support more devices in the private network, since not all devices use the translation at the same time

### 3) Overloading
### 4) Overlapping

#CybersecurityEssentials 