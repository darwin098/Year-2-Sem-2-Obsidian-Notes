- A documented request/proposal to make functional changes to the IT system
- Invoked by business rule/logic changes, which will cascade to IT System behavioural changes supporting the business processes
- Can be the addition of new features, or the extension and removal of existing ones

## Management
---
### 1) Submission of Business Change Request Document/Proposal
> - Business Users/Sponsors will submit a Business Change Request stating the business logic or model changes
> - Solution Designers/System Analysts will take up from here to perform Functional Analysis on the given requirements

Example of Change Request Form:
![[Pasted image 20230104092009.png]]

##### Stakeholders 
- Business Users
- Solution Designers
- System Analysts

##### Deliverables
- Business Change Request
- User Requirement Specifications
- Use Cases

### 2) Functional Analysis
> - The Solution Designers and System Analysts will attempt to understand the required changes and perform a [[#Feasibility & Functional Analysis]], translating Business User Requirements to Functional Statements (Specifications)
> - Functional Specifications/Requirements (User stories/Use-Cases) will then be used to derive a series of technical documents to dictate System-Level modifications and changes

#### Pre-Requisites
- User Requirements Specifications
- Existing Functional Specifications & UML Diagrams
- Optional: Business Change Request & Use Cases

##### Stakeholders
- Solution Designers
- System Analysts

##### Deliverables
- Functional Specifications
- Updated/New UML Diagrams (i.e. Activity, State, Sequence, Class, System/Infra-Architecture or Entity-Relationship Diagrams but not limiting to, depending on functional needs)

### 3) Walkthrough with Business Users & Development Team
> - Carried out assuming the Dev Team are not Solution Developers or System Analysts
> - Solution Developers and System Analysts will attempt to educate the Business Users and Dev Team on the necessary changes to the system to support the required business model, and help stakeholders to visualise the modified system processes
> - If more amendments are required on the functional specifications, repeat [[#2) Functional Analysis]]
- Business Users may approve proposed changes using a Change Request form

Change Request form:
![[Pasted image 20230104201531.png]]

#### Pre-Requisites
- Functional Specifications
- System Design / UML Diagrams

##### Stakeholders
- Business Users
- Solution Designers
- System Analysts
- Development Team

##### Deliverables
- Existing / Amended Functional Specifications
- System Design / UML Diagrams

### 4) Development
> - Development Team will take over the Recommendation of Rectification for the bugfix or the Functional Specifications & UML Diagrams for Business Change Request

#### Pre-Requisites
- Code Files
- Test Cases

#### Execution
1) Development Team (Project Manager / SCRUM Master) will proceed to distribute internally the module and code-level changes required to be done by each Developer (Programmer)
2) Individual Developer will proceed to check-out the source codes of the affected module from Code-Versioning-System (CVS) if the module is not new
3) Developer will proceed to code the functional changes or additions assigned to them
4) Upon completion of their respective parts, individual Developers are required to perform Unity Testing of the Modified Functional Modules which they are each responsible of

#### Development Testing
- Unit Testing will include test cases of:
	- Expected New Behaviour
	- Regression Testing (Existing Behaviour)

##### Stakeholders
- Solution Designers
- System Analysts
- Development Team

##### Deliverables
- Code Files
- Test Cases

### 5) Deployment
> - Developers will ensure that no new versions of code has been added on the code-base he or she was working on
> 	- If the code-base has been amended by another Developer, [[#Code Merging]] has to be performed

#### Code Merging
- Developers will check-out the version of source code which is checked-in later than his or her own version
- Developer will run a comparison check, using a document or file comparison tool, to identify differences
	- If the differences other than the Developer's own changes are required, merge the two files together to include the later version's changes

#### Execution
1) Developer will check-in his or her code files changes into the Code-Versioning-System
2) Developer informs Release Manager of the completion of functionality changes
3) Release Manager will document all the required codes and functionality changes in a Software Release Document, which contains the history of changes
4) Release Manager will then deploy the Code Versions which are marked for release into System-Integration / User-Acceptance software environment

#### User-Acceptance Test (UAT)
1) Release Manager (& possibly Development Team will collect all Unit Test Scripts (Test Cases) marked for the current release and perform a System Integration Test (SIT)
2) Upon success of SIT, Business Users will be invited to run through Test Scripts conducted for the System-Integration Test as User Acceptance Tests
3) Additional Test Cases may also be included upon request of Business Users
4) Business Users sign off on Software Release Document for releases
5) If errors occur at any stage of the System Integration or User Acceptance Tests, the Release Manager is required to rollback all codes in the Code Versioning System to a previous version independent of the release

##### Stakeholders
- Development Team
- Release Manager
- Business Users

##### Deliverables
- Consolidated Test Cases
- Additional Test Cases
- Signed-Off Software Release Document

#SoftwareEngineeringPractice 