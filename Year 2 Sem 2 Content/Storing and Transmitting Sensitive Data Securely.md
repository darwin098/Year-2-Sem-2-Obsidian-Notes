- Passwords are a form of sensitive data that is stored in the database
- We have seen in various reports of passwords being leaked online as a result of systems being hacked
- Other forms of sensitive data may include credit card numbers, NRICs etc
- Sensitive data should not be stored or transferred in plain-text format

## Hashing vs Encryption
---
| Hashing | Encryption |
|-|-|
|One-way function where data is mapped to a fixed-length value | A two-way function where information is scrambled in such a way that it can be unscrambled later|
| Primarily used for authentication ||
| Salting is an additional step during hashing, typically seen in association to hashed passwords that adds an additional value to the end of the password that changes the hash value produced||

## Password Hashing
---
- Algorithm for password hashing:
	1) Generate a long random string
		1) This string is called "salt"
	2) Append the salt to the password
	3) Hash string from Step 2 using a strong hash function Eg bcrypt
	4) Save the salt and the hash in the user's database record

## Types of Encryption
---
### Asymmetric
- Two keys are used: 
	- One for encrypting
	- One for decrypting
- Sender and receiver both have their own private public keys
- Sender encrypts data with public key of the recipient, recipient decrypts with private keys

### Symmetric
- Same key is used to encrypt and decrypt data
- Parties exchange their keys with each other
- Faster and more efficient than asymmetric encryption
- Asymmetric encryption is used to facilitate a key exchange between two parties, and then identical symmetric session keys are used to process the encryption for the session

### Encryption and Decryption with NodeJS's Crypto Library

#### Encrypt
```
var crypto = require('crypto'); 
var mykey = crypto.createCipheriv('aes-128-cbc', 'mypassword'); 
var mystr = mykey.update(stringToEncrypt, 'utf8', 'hex') 
mystr += mykey.final('hex');
```

#### Decrypt
```
var crypto = require('crypto'); 
var mykey = crypto.createDecipheriv('aes-128-cbc', 'mypassword'); 
var mystr = mykey.update(EncryptedString, 'hex', 'utf8') 
mystr += mykey.final('utf8');
```

#EnterpriseSystemsDevelopment 