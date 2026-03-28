# Active Directory Lab

## Overview
This project documents the full build of an Active Directory environment using Windows Server in a virtualized lab. The goal of this lab was to understand domain services, user and organizational structure, DNS integration, and client preparation.

## Objective
- Build a domain controller from scratch
- Configure Active Directory Domain Services (AD DS)
- Design and implement an Organizational Unit (OU) structure
- Validate DNS and domain functionality
- Prepare a Windows client for domain integration

## Technologies Used
- Windows Server
- Active Directory Domain Services (AD DS)
- DNS
- Oracle VirtualBox
- PowerShell
- Git / GitHub

## Lab Structure

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
- Screenshots ? ./screenshots/
- [Step 10 Log](./logs/step-10-ad-verification.txt)
- [Step 11 Log](./logs/step-11-client-build-notes.txt)

### Automation
- [Screenshot Sync Script](./scripts/sync-screenshots.ps1)

## Featured Steps

### [Step 06 – Domain Promotion](./documents/06-adds-and-domain-promotion.md)
- Installed AD DS and promoted server to domain controller
- Created domain: relentixtest.local

### [Step 08 – OU and Admin Setup](./documents/08-admin-account-and-ou-creation.md)
- Created Organizational Units:
  - IT
  - HR
  - Servers
  - Service Accounts
  - Workstations
- Created domain admin account (gquero)

### [Step 10 – Final AD Validation](./documents/10-final-ad-validation.md)
- Verified domain functionality
- Confirmed DNS configuration
- Validated OU structure and admin placement

## Key Takeaways
- Understood how Active Directory integrates with DNS
- Learned importance of static IP addressing for domain controllers
- Implemented structured OU design for scalability
- Gained hands-on experience with domain validation and troubleshooting

## Author
Gabriel Quero
