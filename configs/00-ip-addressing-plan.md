# IP Addressing Plan

## Domain Controller
- Hostname: DC01
- Role: Domain Controller / DNS Server
- Network Design: Adapter 1 NAT, Adapter 2 Host-only
- Static IP: [FILL IN YOUR ACTUAL DC01 STATIC IP]
- Subnet Mask: [FILL IN YOUR ACTUAL SUBNET MASK]
- Default Gateway: [FILL IN YOUR ACTUAL GATEWAY IF USED]
- Preferred DNS: [FILL IN YOUR ACTUAL DNS SETTING]

## Windows Client
- Hostname: CLIENT01
- Role: Windows 10 Domain Client
- Preferred DNS Target: DC01

## Notes
This lab uses a dual-NIC design in VirtualBox with NAT for internet access and Host-only networking for internal lab communication.
