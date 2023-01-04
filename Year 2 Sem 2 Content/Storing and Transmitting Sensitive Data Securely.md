- Passwords are a form of sensitive data that is stored in the database
- We have seen in various reports of passwords being leaked online as a result of systems being hacked
- Other forms of sensitive data may include credit card numbers, NRICs etc
- Sensitive data should not be stored or transferred in plain-text format

## Hashing vs Encryption
---
| [[Hashing]] | [[Encryption]] |
|-|-|
|One-way function where data is mapped to a fixed-length value | A two-way function where information is scrambled in such a way that it can be unscrambled later|
| Primarily used for authentication ||
| Salting is an additional step during hashing, typically seen in association to hashed passwords that adds an additional value to the end of the password that changes the hash value produced||

#EnterpriseSystemsDevelopment 