# Step 06 - Install Active Directory Domain Services (AD DS)

---

## Objective

In this step, I installed the Active Directory Domain Services (AD DS) role on DC01.

This prepares the server to be promoted to a Domain Controller in the next step.

---

## Technologies Used

Windows Server 2022

Server Manager

Active Directory Domain Services (AD DS)

---

## Key Concepts

Active Directory Domain Services (AD DS)

Server Roles and Features

Domain Controller Preparation

Forest and Domain Structure

---

## Configuration / Implementation

### 1. Open Server Manager

Launched Server Manager from the taskbar.

This is the central interface used to manage roles and features.

---

### 2. Add Roles and Features

Navigated to:

Manage → Add Roles and Features

Started the Add Roles and Features Wizard.

---

### 3. Select Installation Type

Selected:

Role-based or feature-based installation

This allows manual selection of server roles.

---

### 4. Select Server

Chose the local server:

DC01

Confirmed the correct target for installation.

---

### 5. Select Server Role

Selected:

Active Directory Domain Services (AD DS)

When prompted, added required features.

---

### 6. Features Section

Left default features selected.

No additional features were required.

---

### 7. Review AD DS Information

Reviewed the AD DS informational screen.

Confirmed understanding of domain services functionality.

---

### 8. Install Role

Clicked Install to begin the process.

---

### 9. Installation Complete

Waited for installation to complete successfully.

Did not restart the server at this stage.

---

## Validation / Verification

Confirmed AD DS role installed successfully

Verified no installation errors

Confirmed post-installation notification appeared

---

## Evidence

Screenshots for this step:

screenshots/step-06/

---

## Key Takeaways

AD DS must be installed before promoting a Domain Controller

This step installs the role but does not create a domain

The server is not a Domain Controller until promotion

Server Manager is used to manage roles and infrastructure

---