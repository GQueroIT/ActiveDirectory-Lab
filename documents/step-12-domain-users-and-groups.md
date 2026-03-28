\## Step 12 - Domain Users and Security Groups Configuration



\### Objective



In this step, I configured a structured Active Directory environment by creating domain security groups and standard user accounts. I then assigned users to the appropriate groups to simulate a real-world organizational structure.



\### Technologies Used



\- Windows Server 2022

\- Active Directory Domain Services (AD DS)

\- Active Directory Users and Computers (ADUC)

\- PowerShell



\### Key Concepts



\- Organizational Units (OUs)

\- Security Groups

\- Group Membership

\- Role-Based Access Control (RBAC)



\### Group Creation



I created the following security groups:



\*\*IT OU:\*\*

\- IT\_Admins

\- IT\_Staff



\*\*HR OU:\*\*

\- HR\_Users



All groups were configured as:

\- Group Scope: Global

\- Group Type: Security



\### User Account Creation



I created the following domain users:



\*\*IT Department:\*\*

\- jsantiago (Jose Santiago)

\- mrivera (Maria Rivera)



\*\*HR Department:\*\*

\- arodriguez (Ana Rodriguez)



Each account was configured with:

\- A standard password

\- Password set to never expire (lab environment)

\- No forced password change on first login



\### Group Membership Assignment



I assigned users to their respective groups:



\- jsantiago -> IT\_Staff

\- mrivera -> IT\_Staff

\- arodriguez -> HR\_Users



\### Verification



I verified group membership using:



\- Active Directory Users and Computers (Member Of / Members tabs)

\- PowerShell



```powershell

Get-ADGroupMember "IT\_Staff"

Get-ADGroupMember "HR\_Users"



\## Screenshots



All screenshots are located in:



/screenshots/step-12/



\## Notes



This step establishes a proper Active Directory structure that will be used later for permissions, Group Policy, and domain login testing.

