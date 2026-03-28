# Step 12 - Domain Users and Security Groups Configuration

---

## Objective

In this step, I configured a structured Active Directory environment by creating domain security groups and standard user accounts. I then assigned users to the appropriate groups to simulate a real-world organizational structure.

---

## Technologies Used

- Windows Server 2022
- Active Directory Domain Services (AD DS)
- Active Directory Users and Computers (ADUC)
- PowerShell

---

## Key Concepts

- Organizational Units (OUs)
- Security Groups
- Group Membership
- Role-Based Access Control (RBAC)

---

## Group Creation

I created the following security groups:

### IT OU
- IT_Admins
- IT_Staff

### HR OU
- HR_Users

All groups were configured as:

- Group Scope: Global  
- Group Type: Security  

---

## User Account Creation

I created the following domain users:

### IT Department
- jsantiago (Jose Santiago)
- mrivera (Maria Rivera)

### HR Department
- arodriguez (Ana Rodriguez)

Each account was configured with:

- Standard password
- Password set to never expire (lab environment)
- No forced password change on first login

---

## Group Membership Assignment

Users were assigned to their respective groups:

- jsantiago → IT_Staff  
- mrivera → IT_Staff  
- arodriguez → HR_Users  

---

## Verification

Group membership was verified using:

### Active Directory Users and Computers
- Member Of tab
- Members tab

### PowerShell

```powershell
Get-ADGroupMember "IT_Staff"
Get-ADGroupMember "HR_Users"
```

---

## Screenshots

All screenshots for this step are located in:

`/screenshots/step-12/`

---

## Notes

This step establishes a proper Active Directory structure that will be used later for permissions, Group Policy, and domain login testing.