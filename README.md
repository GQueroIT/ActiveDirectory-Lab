# Active Directory Lab

## Overview
This project documents the full build of an Active Directory environment using Windows Server in a VirtualBox lab. The lab focuses on domain controller deployment, DNS integration, organizational structure design, and client system preparation.

## What This Project Demonstrates
- Deployment of a Windows Server Domain Controller (DC01)
- Installation and configuration of Active Directory Domain Services (AD DS)
- DNS configuration and validation within a domain environment
- Organizational Unit (OU) design for structured administration
- Creation and validation of domain administrative accounts
- Preparation of a Windows client for domain integration

## Lab Environment

### Domain Details
- Domain: relentixtest.local
- Domain Controller: DC01
- Client (Planned): CLIENT01

### Network Design
- Adapter 1: NAT (internet access)
- Adapter 2: Host-only (internal lab network)
- DC Static IP: 192.168.56.10
- DNS: Domain Controller (127.0.0.1)

## Project Structure

### Documentation
- [Step 00 – Lab Overview](./documents/00-lab-overview.md)
- [Step 01 – Repo and Screenshot Structure](./documents/01-repo-and-screenshot-structure.md)
- [Step 02 – Git and GitHub Setup](./documents/02-git-and-github-setup.md)
- [Step 03 – VirtualBox and Lab Prep](./documents/03-virtualbox-and-lab-prep.md)
- [Step 04 – Windows Server VM Creation](./documents/04-windows-server-vm-creation.md)
- [Step 05 – Network Configuration and Static IP](./documents/05-network-configuration-and-static-ip.md)
- [Step 06 – AD DS and Domain Promotion](./documents/06-adds-and-domain-promotion.md)
- [Step 07 – Post Promotion Validation](./documents/07-post-promotion-validation.md)
- [Step 08 – Admin Account and OU Creation](./documents/08-admin-account-and-ou-creation.md)
- [Step 09 – Core AD Verification](./documents/09-core-ad-verification.md)
- [Step 10 – Final AD Validation](./documents/10-final-ad-validation.md)
- [Step 11 – Windows Client Installation](./documents/11-windows-client-installation.md)

### Configuration
- [IP Addressing Plan](./configs/00-ip-addressing-plan.md)
- [Hostname Plan](./configs/01-hostname-plan.md)
- [OU Structure](./configs/02-ou-structure.md)

### Evidence
- Screenshots: ./screenshots/
- [Step 10 Validation Log](./logs/step-10-ad-verification.txt)
- [Step 11 Client Build Log](./logs/step-11-client-build-notes.txt)

### Automation
- [PowerShell Screenshot Sync Script](./scripts/sync-screenshots.ps1)

## Featured Work

### Domain Controller Deployment
- Installed AD DS and promoted server to domain controller
- Configured relentixtest.local domain
- Verified domain functionality post-installation

### OU Structure and Administration
- Designed and implemented:
  - IT
  - HR
  - Servers
  - Service Accounts
  - Workstations
- Created and validated domain admin account (gquero)

### Final Validation
- Verified Active Directory Users and Computers
- Confirmed DNS functionality
- Validated OU structure and account placement

## Key Takeaways
- Domain Controllers must use static IP addressing for stability
- Active Directory relies heavily on DNS for functionality
- OU structure is critical for scalable administration
- Proper validation ensures a stable domain environment before client integration

## Author
Gabriel Quero
