- The unique address of every end device in a computer network
- Types:
	- [[IPv4 Addressing Space]] (32-bit)
	- IPv6 (128-bit)

## Format
---
- Generally expressed in four dotted decimal format (x.x.x.x), and x is an integer between 0 to 255 (inclusive)
![[Pasted image 20221021190009.png]]

- Compromises of two portions:
	- Network portion
		- Represents a group of IP addresses
	- Host portion
		- Used to uniquely define each IP address within that group of IP addresses

## Subnet Masks
---
- Indicates how the 32 bits of an IP address are divided between the "Network" and "Hosts" portions
- A 32-bit binary number (Just like IP addresses) and is also expressed in the dotted decimal format

- Consists of a string of '1's, followed by a string of '0's where '1's represent the Network portion and '0's represent the HOST portion

![[Pasted image 20221021192214.png]]


## IP Classes
---
- Total of five different groups of IP addresses (A, B, C, D, E) that exist on the internet
- A, B and C (Classful IP addresses) are assigned to governments, companies, schools and public entities for use on the internet
- D and E are reserved for multicasting and experimentation

### Class A (Classful)
- Leads with pattern "0" in binary format
- From the first 8 bits, the range is from 1 to 126 in decimal notation
- For governments throughout the world

![[Pasted image 20221021193919.png]]

### Class B (Classful)
- Leads with pattern "10" in binary
- From the first 8 bits, the range is from 128 to 191 in decimal notation
- Assigned to large and medium sized companies

![[Pasted image 20221021194020.png]]

### Class C (Classful)
- Leads with patter "110" in binary
- Class C network addresses can range from 192 through 223 in decimal notation
- Assigned to groups that do not meet the qualifications to obtain Class A or B addresses

![[Pasted image 20221021194123.png]]

### Class D (Classless)
- Leads with pattern "1110" in the first four binary digits
- From the first 8 bits, the range is from 224 to 239 in decimal notation
- Also known as "Multicast Addresses"
- Reserved for multicasting

![[Pasted image 20221021194303.png]]

### Class E (Classless)
- Leads with pattern "1111" in the first four binary digits
- Everything above and including 240 (in decimal notation) in the first octet
- Reserved for research, testing and experimentation

![[Pasted image 20221021194354.png]]

### Overview
![[Pasted image 20221021194420.png]]


### Default / Standard Subnet Masks
![[Pasted image 20221021195422.png]]

### All "0"s
- 0000.0000.0000.0000 is reserved as network addresses and identifies the network as a group
- Routers use this to route packets to any computer in a LAN

### ALL "1"s
- 1111.1111.1111.1111 is reserved as broadcast addresses to a particular network
- Used any time a computer needs to send a packet to every host in its LAN

## Classless Inter-Domain Routing (CIDR)
---
- Breaks away from the restriction of using multiples of 8-bits for the network portion
- Advantages:
	- More flexible
	- Less wasteful addressing scheme
- CIDR notation for an IP addressis x.x.x.x /N, where N is the network prefix
- Network prefix is the network portion of a Classless IP address (Eg /27 means 27 network bits)

#CybersecurityEssentials 