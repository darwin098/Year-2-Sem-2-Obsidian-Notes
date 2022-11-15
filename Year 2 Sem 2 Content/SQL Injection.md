- A web security vulnerability that allows attackers to interfere with the queries that an application makes to its database
- Subset of the unverified / un-sanitized user input vulnerability by convincing the application to run SQL code that was not intended
- Targeted at stealing information from an entire database

## Consequences
---
- Violates the [[CIA Triad]]
The attacker will be able to:
- view **confidential** data that they are not normally able to retrieve (Eg data of other users) 
- Compromises the **integrity** of data (Eg alter values in the database)
- Removes the **availability** of services (Eg remove tables from database)

### Examples
- Read and modify sensitive data from the database
- Execute administration operations on the database
	- Shutdown auditing or the DBMS
	- Truncate tables and logs
	- Add users
- Recover the content of a given file present on the DBMS file system
- Issue commands to the operating system

## Types
---
### In-band SQLI (Classic SQLI)
- Attacker is able to use the same communication channel to both launch the attack and gather results

#### Error-based SQLI
- Attacker performs actions that cause the database to produce error messages
- Attacker can potentially use the data provided by these error messages to gather information about the structure of the database

#### Union-based SQLI
- Attacker leverages the UNION SQL operator to combine the results of two or more SELECT statements into a single result which is then returned as part of the HTTP response

### Inferential SQLI (Blind SQLI)
- Attacker tries to guess contents of database by sending different payloads to server and observing the return results

#### Boolean-based
- Attacker sends alternate SQL queries that result in TRUE and FALSE conditions
- If results returned by the two queries are different, it an be inferred that the application is vulnerable to an SQL injection attack

#### Time-based
- Attacker sends SQL query which forces database to wait for specified amount of time before responding
- Depending on the result, a HTTP response will be returned with, or without a delay
- Attacker can infer if payload used returned true or false, even though no data from the database is returned


### Out-of-band SQLI
- The result of the attacker's activities is received using another channel
- Not common as it depends on feature being enabled on the database server

## Prevention
---
- Ensure user input which contains malicious SQL are eliminated and/or not allowed to execute at the back-end

### Defence options
#### Parameterized Queries (MOST IMPORTANT)

^4940e7

![[Pasted image 20221112122601.png]]

#### Stored Procedures

^93266f

- An SQL function

![[Pasted image 20221112122924.png]]

#### Allowed-list Input Validation

^ddcfb6

- Only send the database query if the user input passes the regular expression test
- Useful if inputs are well-structured data such as dates, email, addresses etc, but hard to implement for free-form text

![[Pasted image 20221112123028.png]]

#### Escape User Input 

^cb977f

- Should only be used as a last resort
- The escaping technique depends on database server being used

![[Pasted image 20221112123207.png]]

#EnterpriseSystemsDevelopment 