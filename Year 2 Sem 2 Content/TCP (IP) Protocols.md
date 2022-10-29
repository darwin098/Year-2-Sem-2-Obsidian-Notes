- TCP/IP protocols specify the formatting, addressing and routing mechanism that ensures the delivery of our messages to the correct recipient
- Also has [[Data Encapsulation]]

## Layers
---
| Layer | Function | Examples |
|-|-|-|
| Application | Provides process-to-process application data exchange| DHCP, DNS, HTTP |
| Transport | Handles host-to-host communication | [[Transmission Control Protocol (TCP)]], [[User Datagram Protocol (UDP)]] |
| Internet | Connects hosts across networks | IP, ICMP |
| Network Access | Handles communication for a single network segment (link) | Ethernet |

- Transport layer
	- Establishes a data channel for an application to achieve to achieve end-to-end data exchange
	- Also responsible for:
		- Application Addressing
		- Segmentation of Data
		- Error Control
		- Flow Control
		- Congestion Control

#CybersecurityEssentials 