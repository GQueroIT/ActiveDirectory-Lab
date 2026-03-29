# Step 05 - Network Configuration and IP Setup

---

## Objective

In this step, I configured the network settings for DC01 by assigning a static IP address and defining the DNS server.  
This ensures consistent communication required for Active Directory.

---

## Technologies Used

- Windows Server 2022
- Oracle VirtualBox
- PowerShell / Command Prompt

---

## Key Concepts

- Static IP Addressing
- Subnet Mask
- DNS Configuration
- Network Adapter Settings
- Internal Lab Networking

---

## Configuration / Implementation

### 1. Identify Network Adapter

Accessed network settings on DC01 and selected the adapter connected to the Host-Only network.

This adapter handles internal communication between lab machines.

---

### 2. Assign Static IP Address

Configured the following IPv4 settings:

- IP Address: 192.168.56.10
- Subnet Mask: 255.255.255.0

This ensures the server maintains a consistent identity on the network.

---

### 3. Configure DNS Server

Set Preferred DNS Server to:

- 192.168.56.10

The Domain Controller must point to itself for DNS resolution.

---

### 4. Verify Network Configuration

Used:

ipconfig

Confirmed IP address, subnet mask, and DNS settings were applied correctly.

---

### 5. Test Basic Connectivity

Performed initial checks:

- Adapter is enabled
- No IP conflicts detected
- Network is stable

---

## Validation / Verification

- Verified static IP using ipconfig
- Confirmed DNS points to DC01
- Verified adapter is active
- Confirmed stable configuration

---

## Evidence

Screenshots for this step:

screenshots/step-05/

---

## Key Takeaways

- Domain Controllers require static IP addresses
- DNS must point to the Domain Controller
- Network configuration is foundational for Active Directory
- Incorrect settings will break domain functionality

---