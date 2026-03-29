# Step 03 - VirtualBox Setup and Lab Preparation

---

## Objective

In this step, I prepared the lab environment by installing and configuring VirtualBox. The goal was to create a stable virtualization environment that would support running Windows Server and client machines for the Active Directory lab.

---

## Technologies Used

Oracle VirtualBox

Windows 11 (Host Machine)

ISO Images (Windows Server / Windows Client)

---

## Key Concepts

Virtualization

Hypervisor Configuration

Resource Allocation

Network Adapter Configuration

Lab Environment Design

---

## Configuration / Implementation

### 1. Installed VirtualBox

I installed Oracle VirtualBox on my host machine to serve as the hypervisor for running virtual machines.

This allows multiple operating systems to run simultaneously in an isolated environment.

---

### 2. Downloaded Required ISO Files

I obtained the necessary ISO files for:

Windows Server

Windows Client

These ISO files will be used to install the operating systems inside the virtual machines.

---

### 3. Created Initial Virtual Machine Plan

I planned the lab environment to include:

DC01 as the Domain Controller

CLIENT01 as the client machine

This setup simulates a small enterprise network.

---

### 4. Configured VirtualBox Networking

I prepared the network design using:

NAT for internet access

Host-Only Adapter for internal lab communication

This design allows the virtual machines to communicate with each other while keeping the internal lab network separated from the outside network.

---

### 5. Allocated System Resources

I configured the virtual machine settings to support stable performance, including:

RAM allocation

CPU allocation

Virtual disk storage

This helps ensure the lab runs smoothly without unnecessary performance issues.

---

## Validation / Verification

Verified VirtualBox installation completed successfully

Confirmed ISO files were available and ready to mount

Verified planned VM network design was in place

Confirmed lab environment was prepared for server deployment

---

## Evidence

Screenshots for this step:

`screenshots/step-03/`

---

## Key Takeaways

Virtualization is essential for building safe and flexible lab environments

Proper planning makes later configuration steps easier

Network design must be thought through before server deployment

A stable lab foundation prevents avoidable issues later in the build

---