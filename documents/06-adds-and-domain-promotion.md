\# Step 06 - Install Active Directory Domain Services (AD DS)



---



\## Objective



In this step, I installed the Active Directory Domain Services (AD DS) role on DC01.  

This prepares the server to be promoted to a Domain Controller in the next step.



---



\## Technologies Used



\- Windows Server 2022

\- Server Manager

\- Active Directory Domain Services (AD DS)



---



\## Key Concepts



\- Active Directory Domain Services (AD DS)

\- Server Roles and Features

\- Domain Controller Preparation

\- Forest and Domain Structure



---



\## Configuration / Implementation



\### 1. Open Server Manager



Launched Server Manager from the taskbar.



This is the central interface used to manage roles and features.



---



\### 2. Add Roles and Features



Navigated to:



Manage → Add Roles and Features



Started the Add Roles and Features Wizard.



---



\### 3. Installation Type



Selected:



Role-based or feature-based installation



This allows manual selection of server roles.



---



\### 4. Server Selection



Selected the local server:



DC01



Confirmed the correct server was targeted for installation.



---



\### 5. Select Server Roles



Checked:



Active Directory Domain Services (AD DS)



When prompted, selected:



Add Features



---



\### 6. Features Section



Left default features selected.



No additional features were required for this step.



---



\### 7. AD DS Information



Reviewed the AD DS information screen.



Confirmed understanding that this role enables domain services.



---



\### 8. Confirmation



Clicked Install to begin installation.



---



\### 9. Installation Complete



Waited for installation to complete successfully.



Did NOT restart the server yet.



---



\## Validation / Verification



\- Confirmed AD DS role installed successfully

\- Verified no installation errors

\- Confirmed post-installation notification appeared



---



\## Evidence



Screenshots for this step:



screenshots/step-06/



---



\## Key Takeaways



\- AD DS must be installed before promoting a Domain Controller

\- This step only installs the role — no domain exists yet

\- The server is not a Domain Controller until promotion

\- Server Manager is used to manage roles and infrastructure



---

