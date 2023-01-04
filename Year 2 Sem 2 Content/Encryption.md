- A two-way function where information is scrambled in such a way that it can be unscrambled later

## Classes of Encryption Algorithms
---
### Asymmetric (Public-Key Encryption)
- Two keys are used: 
	- One for encrypting
	- One for decrypting
- Sender and receiver both have their own private/public keys
- Sender encrypts data with public key of the recipient, recipient decrypts with private keys
- Asymmetric algorithms:
	- RSA (Rivest_Shamir-Adleman)
	- Diffie-Hellman
	- ElGamal
	- Elliptic Curve Cryptography (ECC)

### Symmetric (Private-Key Encryption)
- Same key pair is used to encrypt and decrypt data
- Parties exchange their keys with each other
- Faster and more efficient than asymmetric encryption
- Asymmetric encryption is used to facilitate a key exchange between two parties, and then identical symmetric session keys are used to process the encryption for the session
- Common encryption standards
	- 3DES (Triple Data Encryption Standard) - block cipher with 64-bit block size that uses a 56-bit key
	- IDEA (International Data Encryption Algorithm) uses 64-bit blocks and 128-bit keys
	- AES (Advanced Encryption Standard) has a fixed block size of 128-bits with key size of 128, 192 or 256 bits

| Asymmetric Encryption | Symmetric Encryption |
| - | - |
| More efficient and can handle more data | More efficient at protecting the confidentiality of small amounts of data|
| Key management is more problematic and harder to manage | Size and speed makes it more secure for tasks such as small data exchanges|

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
#CybersecurityEssentials 