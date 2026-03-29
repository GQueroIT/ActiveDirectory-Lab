# Step 09 - Core Active Directory Verification

---

## Objective

In this step, I verified that the core Active Directory environment is working properly after completing the domain setup.

The goal here was to make sure everything is stable before moving forward.

---

## Technologies Used

Windows Server 2022

Active Directory Users and Computers (ADUC)

Command Prompt

DNS Manager

---

## Key Concepts

Active Directory Validation

Domain Services Verification

DNS Resolution

Authentication Testing

Directory Integrity

---

## Configuration / Implementation

### 1. Verify Domain Controller Status

Confirmed that DC01 is running as a Domain Controller.

Verified domain:

relentixtest.local

---

### 2. Verify Organizational Units

Opened Active Directory Users and Computers.

Confirmed all OUs are present:

IT

HR

Workstations

Servers

Service Accounts

---

### 3. Verify User Accounts

Confirmed the administrative account exists:

gquero

Verified it is placed in the correct OU.

---

### 4. Verify Group Membership

Opened Command Prompt and ran:

whoami /groups

Confirmed the account is part of Domain Admins.

---

### 5. Verify DNS Functionality

Opened DNS Manager.

Confirmed the forward lookup zone exists:

relentixtest.local

Verified the required DNS records are present.

---

### 6. Verify Authentication

Logged into the system using domain credentials.

Confirmed successful authentication against the domain.

---

## Validation / Verification

Confirmed the Domain Controller is working correctly.

Verified OU structure and account placement.

Validated DNS functionality.

Confirmed successful domain authentication.

---

## Evidence

Screenshots for this step:

screenshots/step-09/

---

## Key Takeaways

This step confirmed that the Active Directory environment is fully operational.

DNS plays a critical role in domain communication and authentication.

Verifying everything at this stage helps prevent issues later in the lab.

---