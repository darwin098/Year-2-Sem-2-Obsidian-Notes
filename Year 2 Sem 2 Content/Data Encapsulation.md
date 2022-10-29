- When data is sent from the source host to the destination host, the data goes through 
	- Encapsulations at the source host
	- De-Encapsulation (Removing the headers, aka unpackaging) at the destination host

![[Screenshot 2022-10-29 143012.png]]


## Data Encapsulation
---
- At the sending host, as the data (Eg an email) goes down the layers, the encapsulation process adds "headers" to the data
- The data link layer (refer to [[OSI Seven Layer Model]]) may add a trailer too
- Encapsulation increases the size of the data packet

![[Pasted image 20221029144057.png]]


## De-Encapsulation
---
- At the receiving host, as the data goes up the layers, the de-encapsulation process removes "headers" from the data
- Eventually the original data is recovered

![[Pasted image 20221029144916.png]]

#CybersecurityEssentials 