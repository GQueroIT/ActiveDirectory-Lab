\# Step 13 - Domain Join and Client Validation



---



\## Objective



In this step, I joined CLIENT01 to the relentixtest.local domain and validated that domain authentication was working correctly from the client machine.



---



\## Technologies Used



\- Windows Server 2022

\- Windows 10

\- Active Directory Domain Services (AD DS)

\- Active Directory Users and Computers (ADUC)

\- PowerShell

\- Command Prompt



---



\## Key Concepts



\- Domain Join

\- DNS Resolution

\- Computer Objects in Active Directory

\- Organizational Unit Placement

\- Domain Authentication



---



\## Client Network Configuration



CLIENT01 was configured with a static IP address on the internal lab network and pointed to DC01 for DNS resolution.



\- IP Address: 192.168.56.20

\- Subnet Mask: 255.255.255.0

\- DNS Server: 192.168.56.10



This allowed the client to resolve and communicate with the domain controller correctly before the domain join process.



---



\## Connectivity Validation



Before joining the domain, I verified that CLIENT01 could communicate with DC01 by using:



\- `ipconfig`

\- `ping 192.168.56.10`

\- `nslookup relentixtest.local`



These checks confirmed that the client was on the correct network and using the domain controller for DNS.



---



\## Domain Join



CLIENT01 was joined to the `relentixtest.local` domain using domain administrator credentials. After the join was completed successfully, the client machine was restarted so the change could take effect.



---



\## Domain Login Validation



After restart, I signed into CLIENT01 using a domain user account to confirm that domain authentication was functioning correctly and that a user profile could be created successfully on the joined workstation.



---



\## Active Directory Validation



On DC01, I verified that the `CLIENT01` computer object appeared in Active Directory. I then moved the computer object into the `Workstations` OU to keep the environment organized according to the lab structure.



---



\## PowerShell Verification



The following PowerShell commands were used to validate the computer object:



```powershell

Get-ADComputer -Identity CLIENT01

Get-ADComputer -Filter \* -SearchBase "OU=Workstations,DC=relentixtest,DC=local"

```



---



\## Screenshots



All screenshots for this step are located in:



`/screenshots/step-13/`



---



\## Notes



This step transitioned the lab from basic Active Directory configuration into real client-to-domain interaction. It confirmed that the environment was functioning as an actual domain rather than only a server-side setup.

