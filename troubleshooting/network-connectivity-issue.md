\# Troubleshooting - Network Connectivity Issue (DC01 and CLIENT01)



---



\## Issue



During Step 13, CLIENT01 was unable to communicate with DC01 across the internal lab network.



This prevented normal validation and blocked domain join progress until the connectivity issue was isolated and corrected.



---



\## Symptoms



The following problems were observed:



\- Ping requests between DC01 and CLIENT01 failed

\- CLIENT01 appeared correctly configured at first glance

\- DC01 was not using the intended static address

\- Communication only succeeded after firewall rules were adjusted



---



\## Environment



\- Hypervisor: VirtualBox

\- Domain Controller: DC01

\- Client Machine: CLIENT01

\- Internal Lab Network: 192.168.56.0/24

\- Expected DC IP: 192.168.56.10

\- Expected Client IP: 192.168.56.20



---



\## Root Causes Identified



\### 1. DC01 was not using the correct static IP



The domain controller was found using the wrong address instead of the intended static configuration.



This created instability during client-to-server validation.



---



\### 2. Multiple network adapters created confusion during testing



The environment used both:

\- NAT

\- Host-only Adapter



This required careful confirmation that testing was occurring across the correct internal adapter.



---



\### 3. Windows Firewall blocked connectivity validation



Even after correcting the network configuration, ping traffic was still blocked until the firewall was disabled for testing.



---



\## Resolution Steps



\### Step 1 - Verify VirtualBox adapter alignment



Both VMs were reviewed to confirm that Adapter 2 was attached to:



\- Host-only Adapter

\- VirtualBox Host-Only Ethernet Adapter



This ensured both systems were placed on the same internal network.



---



\### Step 2 - Correct DC01 IP configuration



DC01 was reconfigured to use the proper static settings:



\- IP Address: 192.168.56.10

\- Subnet Mask: 255.255.255.0

\- Default Gateway: left blank

\- DNS Server: 192.168.56.10



---



\### Step 3 - Confirm CLIENT01 IP configuration



CLIENT01 was confirmed to be using:



\- IP Address: 192.168.56.20

\- Subnet Mask: 255.255.255.0

\- Default Gateway: left blank

\- DNS Server: 192.168.56.10



---



\### Step 4 - Test communication again



Connectivity tests were repeated using:



```cmd

ping 192.168.56.10

ping 192.168.56.20

```



At this point, communication was still blocked.



---



\### Step 5 - Disable firewall for testing



Firewall was temporarily disabled to verify whether Windows filtering was blocking ICMP traffic.



Example command used:



```powershell

netsh advfirewall set allprofiles state off

```



After this change, connectivity succeeded and validation could continue.



---



\## Result



After correcting the DC configuration and temporarily disabling firewall protection for testing, communication between DC01 and CLIENT01 was restored successfully.



This confirmed that the issue was not caused by VirtualBox after final adapter alignment, but by a combination of:



\- incorrect DC IP configuration

\- multi-adapter confusion during validation

\- Windows Firewall behavior



---



\## Evidence



Screenshots for this troubleshooting case are stored in:



`screenshots/troubleshooting/`



Included evidence:



\- CLIENT01 IP Config Correct

\- Communication Fix after Firewall Disable

\- DC IP Config Corrected

\- DC IP Config Wrong

\- DC Ping Fail



---



\## Key Takeaways



\- Active Directory labs depend on the domain controller having the correct static IP

\- The client and server must use the same internal VirtualBox network

\- NAT and Host-only adapters can cause confusion if the wrong adapter is inspected

\- Windows Firewall can block ping even when network configuration is otherwise correct

\- Troubleshooting should confirm configuration, isolate variables, and retest after each change

