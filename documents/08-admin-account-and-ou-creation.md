\# Step 08 - Administrative Account Creation and OU Structure



---



\## Objective



In this step, I created a dedicated administrative account and organized the Active Directory structure using Organizational Units (OUs).



This improves security, delegation, and overall directory organization.



---



\## Technologies Used



Windows Server 2022



Active Directory Users and Computers (ADUC)



---



\## Key Concepts



Organizational Units (OUs)



Administrative Accounts



Role-Based Access Control (RBAC)



Directory Structure Organization



Delegation of Control



---



\## Configuration / Implementation



\### 1. Open Active Directory Users and Computers



Launched:



Active Directory Users and Computers (ADUC)



---



\### 2. Create Organizational Units (OUs)



Created the following OUs under the domain:



IT



HR



Workstations



Servers



Service Accounts



---



\### 3. Create Administrative Account



Navigated to the IT OU.



Created a new user account:



Username: gquero



Assigned a secure password



Configured password settings



---



\### 4. Assign Administrative Privileges



Added the user to the following group:



Domain Admins



---



\### 5. Verify Account Permissions



Opened Command Prompt and ran:



whoami /groups



Confirmed Domain Admins membership is applied



---



\## Validation / Verification



Confirmed OU structure is visible in ADUC



Verified administrative account exists in the IT OU



Confirmed elevated privileges through group membership



Successfully authenticated using the new admin account



---



\## Evidence



Screenshots for this step:



screenshots/step-08/



---



\## Key Takeaways



OUs provide structure and organization within Active Directory



Administrative accounts should be separated from default accounts



Group membership controls access and privileges



Proper OU design supports scalability and delegation



---

