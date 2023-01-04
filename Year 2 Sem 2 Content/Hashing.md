- A one-way function where data is mapped to a fixed-length value
- Primarily used for authentication
- Salting is an additional step during hashing, typically seen in association to hashed passwords that adds an additional value to the end of the password that changes the hash value produced

## Password Hashing
---
- Algorithm for password hashing:
	1) Generate a long random string
		1) This string is called "salt"
	2) Append the salt to the password
	3) Hash string from Step 2 using a strong hash function Eg bcrypt
	4) Save the salt and the hash in the user's database record


#EnterpriseSystemsDevelopment 


