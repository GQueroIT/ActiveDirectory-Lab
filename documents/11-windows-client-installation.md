# Step 11 - Windows Client Installation and Preparation

---

## Objective

In this step, I installed and configured a Windows client machine to prepare it for domain integration.

The goal was to have a clean system ready to join the Active Directory domain.

---

## Technologies Used

Windows 10 / Windows 11

Oracle VirtualBox

---

## Key Concepts

Client Machine Setup

Operating System Installation

Network Configuration

Domain Preparation

Host Communication

---

## Configuration / Implementation

### 1. Create Windows Client Virtual Machine

Created a new virtual machine in VirtualBox.

Allocated CPU, RAM, and storage resources.

Attached the Windows ISO for installation.

---

### 2. Install Windows Operating System

Booted the virtual machine and completed the installation.

Configured basic system settings.

Created a local user account.

---

### 3. Configure Network Adapter

Configured the network adapter for the lab environment.

Ensured the client is on the same network as DC01.

---

### 4. Verify Network Connectivity

Opened Command Prompt and tested connectivity.

Pinged the Domain Controller successfully.

Confirmed communication is working.

---

### 5. Configure DNS Settings

Set the client DNS server to point to DC01.

Verified the configuration is applied correctly.

---

### 6. Prepare for Domain Join

Verified system configuration.

Confirmed the client can resolve:

relentixtest.local

Ensured the machine is ready to join the domain.

---

## Validation / Verification

Confirmed the client machine is installed and operational.

Verified network connectivity to the Domain Controller.

Validated DNS configuration and domain resolution.

Confirmed the system is ready for domain join.

---

## Evidence

Screenshots for this step:

screenshots/step-11/

---

## Key Takeaways

Proper client setup is required before joining a domain.

DNS configuration is critical for locating the Domain Controller.

Network connectivity must be verified before domain integration.

This step prepares the environment for a successful domain join.

---