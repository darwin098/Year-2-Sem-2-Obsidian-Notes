## Types of Access Control
---
### Physical Access Controls
- Actual barriers deployed to prevent direct contact with systems
- The goal is to prevent unauthorised users from gaining physical access to facilities, equipment, and other organizational assets
- Physical access control determines who, where and when they can enter/exit

### Logical Access Controls
- Hardware and software solutions used to manage access to resources and systems
- These technology-based solutions include tools and protocols that computer systems use for identification, authentication, authorisation and accountability

### Administrative Access Controls
- Policies and procedure defined by organizations to implement and enforce all aspects of controlling unauthorised access
- Focuses on personnel and business practices

## Access Control Strategies
---
### Mandatory Access Control (MAC)
- Restricts the actions that a subject can perform on an object.
- A subject can be a user or a process
- An object can be a file, a port, or an input/output device.
- An authorisation rule enforces whether or not a subject can access the object

### Discretionary Access Control (DAC)
- Grants or restricts object access determined by the object's owner
- Controls are discretionary as an object owner with certain access permissions can pass on those permissions to another subject

### Role-based Access Control (RBAC)
- Based on the role of the subject
- Roles are job functions within an organization
- Specific roles require permissions to perform certain operations
- Users acquire permissions through their role
- Can work in combination with DAC or MAC by enforcing the policies of either one.

### Rule-based Access Control
- Uses access control lists (ACLs) to help determine whether to grant access
	- A series of rules is contained in the ACL
	- The determination of whether to grant access depends on these rules
- An example of such a rule is one that states no employee may have access to the payroll file after hours or on weekends

## Identification
---
- Identification enforces the rules established by the authorization policy
- A subject requests access to a system resources
- Every time the subject requests access to a resource, the access controls determines whether to grant or deny access
- Cybersecurity policies determine which identification controls should be used
- The sensitivity of the information and information systems determine how stringent the controls are

## Authentication Methods
---
### What You Know
- Passwords, passphrases or PINs
- Passwords are the most popular method used for authentication

### What You Have
- Smart cards and security key fobs are both examples of something that users have in their possession

### Who You Are
- A unique physical characteristic, such as a fingerprint, retina, or voice, that identifies a specific user, also known as biometrics

### Multi-factor Authentication
- Multi-factor authentication uses at least two methods of verification
- A security key fob is a good example. The two factors are something you know, such as a password, and something you have, such as a security key

## Authorisation
---
- Authorisation controls what a user can and cannot do on the network after successful authentication
- After a user proves his or her identity, the system checks to see what network resources the user can access and what the users can do with the resources
- Authorisation uses a set of attributes that describes the user's access to the network
- The system compares these attributes to the information contained within the authentication database, determines a set of restrictions for that user, and delivers it to the local router where the user is connected
- Defining authorisation rules is the first step in controlling access. An authorisation policy establishes these rules

## Accountability
---
- Accountability traces an action back to a person or process making the change to a system, collects this information, and reports the usage data
- The organization can use this data for such purposes as auditing or billing
- The collected data might include the log in time for a user, whether the user log in was a success or failure, or what network resources the user accessed
- This allows an organization to trace actions, errors, and mistakes during an audit or investigation
- Implementing accountability consists of technologies, policies, procedures and education
- Log files provide detailed information based on the parameters chosen

## Types of Security Controls
---
### Preventative Controls
- Controls / stops unwanted or unauthorised activity from happening

### Deterrent Controls
- Used to limit or mitigate an action or behaviour

### Detective Controls
- Identifies different types of unauthorized activity
- Can be very simple, such as motion detector or security guard
- Can also be more complex, such as an intrusion detection system

### Corrective Controls
- Restores systems back to a state of confidentiality, integrity and availability. Can also restore systems to normal after unauthorised activity occurs

### Recovery Controls
- Restores resources, functions, and capabilities after a violation of a security policy
- Can repair damage, in addition to stopping any further damage
- Has more advanced capabilities over corrective access controls

### Compensative Controls
- Provides options to other controls to bolster enforcement in support of a security policy
- Can also be a substitution used in place of a control that is not possible under the circumstances

#CybersecurityEssentials 