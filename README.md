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
```
---

The VM was allocated
RAM:2048MB
<img width="1169" height="729" alt="Oracle VirtualBox Manager 11-09-2026 19_37_25" src="https://github.com/user-attachments/assets/41431d88-a5ee-4617-81e6-30618f582635" />



---

## step5: Kali Linux network was configured as follows
```text
Ip address: 10.0.0.2
 subnet Mask: 225.225.225.0
Gateway: 10.0.0.1
DNS:8.8.8.8
```
<img width="1920" height="974" alt="kali-linux-2026 2-virtualbox-amd64 (Snapshot 5)  Running  - Oracle VirtualBox 11-09-2026 21_01_13" src="https://github.com/user-attachments/assets/02d150ba-2be6-41e8-bbc1-2bf012eebfa1" />

---

## step6: A clean VM snapshot was taken
A clean VM snapshot acts as backup of our virtual machine.
```text
my fresh kali
```

---

## Lab verifacation

|      TEST       |      COMMAND      |     RESULT     |
|-----------------|-------------------|----------------|
| Ip address      |      `  ip a `      |  displayed incorrect|
|   Test gateway  |      `10.0.0.1`   |  successful  |
|  Test internet connectivity| ping 8.8.8.8 | successful |
|      Snapshot verification  | Restore snapshot and run `ip a` | successful |
### Corrected results
   Ip address:10.0.0.2

---

# Problems encountered and solutions
## Problem 1: Internet Connectivity after configuration
Internet connectivity was failed and the kali virtual machine was not showing Ip address in the terminal. this is how i fixed it
```text
Created adapter 2 and assigned bridged adapter which will directly link my virtual machine to wireless physical local Network.
```
<img width="1169" height="729" alt="Oracle VirtualBox Manager 11-09-2026 21_36_18" src="https://github.com/user-attachments/assets/bf929509-9375-4c20-9f26-d8ee8c86c5fc" />

---

## Problem 2. VirtualBox VT-x / Virtualization Error

The VM initially failed to start because hardware virtualization was disabled in the system firmware/BIOS.

The issue was resolved by:

1. Restarting the computer.
2. Entering BIOS/UEFI settings.
3. Enabling Intel VT-x / hardware virtualization.
4. Saving the configuration.
5. Restarting the computer.
6. Starting the Kali VM again.

After enabling virtualization, the VM started successfully.


---

# What i learned

### 1 Virtual machine networking
I learned how virtual box adapters connects our virtual machine to our physical local network and how additional adapters like bridged network play important role in this
### Benifits: can perform network scans and interact directly with other physical devices on your local Wi-Fi or Ethernet network using the bridged interface, while keeping secure internal traffic contained within the NAT network.
### Simultaneous Access: You keep internet access and inter-VM connectivity without sacrificing your ability to target external local devices.

---

### 2 Static Ip configuration
I learned how to configure and verify IPv4 addressing, subnet masks, gateways, and DNS settings in Kali Linux.

---

### 3 VM snapshots
I learned the importance of VM snapshots which acts as a backup when performing a test or experiment in the virtual mechine.

---

# Tools i used during setup
- **7-Zip:** [https://7-zip.org/download.html](https://7-zip.org/download.html)
- **VirtualBox:** [https://virtualbox.org/wiki/Downloads](https://virtualbox.org/wiki/Downloads)
- **Kali Linux:** [https://kali.org/get-kali](https://kali.org/get-kali)

---

# AUTHOR
```text
Gautham Reddy
Cybersecurity student B083
Instructor: Waqas Karim
cybersecurity profrssional NETWORKWALKS
```

---

##  Project Information

**Program Name:** Cybersecurity at Networkwalks | **Week:** 01 | **Project:** Cybersecurity & Pentesting Lab Setup | **Repository:** GitHub



























  


