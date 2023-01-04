
## Types
---
### Business-As-Usual (BAU) Bugfix
- Business Users have found that software system is not performing according to expected behaviour.
- Users will submit a support ticket to the maintenance / development team for further testing and Root Cause Analysis

### Bugfix Resolution
#### Root-Cause Analysis (RCA)
1) Development Team will understand the expected behaviour from Business Users (may require further discussion)
2) Development Team will also ensure the expected behaviour stated by Business Users tally with the User Requirements & Functional Specifications and possibly signed-off UAT cases
3) If existing User Requirements & Functional Specifications and UAT cases do not tally with descriptions provided by Business Users, Software System is deemed to have a "Logic Gap". 
	- Business users are then recommended to submit a new Business Change Request
4) Development Team will first have to replicate the unexpected-behaviour/bug at System Integration Test Environments, by series of Test Cases
5) The source code of the System Integration Test area/module that is identified to be buggy  is to be investigated
6) Derive conclusion of the Root Cause Analysis and provide a Recommendation of Rectification for the bug
7) Proceed to Development phase (Just like [[Change Requests |Change Request Management]])