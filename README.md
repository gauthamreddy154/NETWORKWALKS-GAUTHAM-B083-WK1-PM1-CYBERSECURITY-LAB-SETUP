<div align="center">

# CYBERSECURITY LAB ENVIRONMENT SETUP
</div>

---


## PROJECT OVERVIEW
In this project I am setting up a *virtual cybersecurity and penetration testing laboratory* using virtualBox and kali linux.
The purpose is  to create a environment which will be isolated from our machine so that we can use cybersecurity tools and other security related tools without harming our system.
As this lab is configured in a private virtual network we will be able to add additional machines and later used as targets for authorized security testing.

---

## Objectives
The main objectives of this project are as follows:

- Installing 7-ZIP
- installing/importing kali Linux as a virtual machine
- Creating a NAT network for the lab
- configuring network connictivity for kali Linux
- assigning a Ip address to VM
- Verify network connectivity
- take clean VM snapshot

  ---

  ## Lab configuration
  | COMPONENT  | CONFIGURATION |
  |------------|---------------|
  | HOST OS    | windows 11    |
  | HOST RAM   |    16GB       |
  | processor  | intel core i5 |
  | HYPERVISOR | VirtualBox 7.2|
  | security OS| kali Linux 2026.2|
  | Kali RAM   |   2048MB      |
  | Virtual network| NAT network |
  | Network address| 10.0.0.0 |
  | Kali IP address | 10.0.0.2/24 |
  | Default Gateway | 10.0.0.1 |
  | DNS server  | 8.8.8.8  |

  ---

# How the lab was created

## step 1: Installed 7-ZIP
   FOR EXTRACTION OF Kali Linux.

---

## Step 2: Installed virtualBox
    installed as hypervisor.

---

## step 3: NATNetwork was created

      Configuration:
Network Name: NatNetwork
IPv4 Prefix:  10.0.0.0/24
DHCP:         Enabled
IPv6:         Disabled


![]<img width="1920" height="974" alt="Oracle VirtualBox Manager 11-09-2026 19_19_59" src="https://github.com/user-attachments/assets/460544a7-9329-4361-8d5d-a4f26b0e7283" />


---

## step4: Kali Linux was imported in virtual BOX and configured
The VM network adapter was configured as follows:

```text
Adapter 1
Attached to: NAT Network
Network:     NatNetwork
Adapter Type: Intel PRO/1000 MT Desktop

---

The VM was allocated
RAM:2048MB



---

## step5: Kali Linux network was configured as follows

Ip address: 10.0.0.2
 subnet Mask: 225.225.225.0
Gateway: 10.0.0.1
DNS:8.8.8.8



---













  


