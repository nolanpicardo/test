# Part B – Networking: Small Office LAN Setup and Services

## Overview

This project was completed using **Cisco Packet Tracer** to design and simulate a small office network as part of a university assignment. It consists of two main tasks:

- **Task 1**: Creating and configuring a local area network (LAN) with wired and wireless devices using DHCP.
- **Task 2**: Adding DNS and HTTP services to the existing network and testing name resolution and web access.

---

## Task 1 – Small Office LAN Setup

The small office network includes:
- **5 wired PCs** and **1 wired printer** connected to a switch.
- **1 tablet** and **1 smartphone** connected via Wi-Fi to a **wireless router**.
- The wireless router also acts as a **DHCP server** and **default gateway** (`192.168.1.1/24`).

### Reserved IP Addresses via DHCP:

| Device       | IP Address      |
|--------------|-----------------|
| PC1          | 192.168.1.10    |
| PC2          | 192.168.1.11    |
| PC3          | 192.168.1.12    |
| PC4          | 192.168.1.13    |
| PC5          | 192.168.1.14    |
| Tablet (PC6) | 192.168.1.15    |
| Printer      | 192.168.1.253   |
| Radius Server| 192.168.1.4     |

### Wireless Configuration:

- **SSID**: `pollyvacherwireless`
- **Security**: WPA2 Enterprise with AES
- **Shared Key**: `P0llyVch3r`
- **RADIUS Server IP**: `192.168.1.4`
- **User Accounts**:
  - `user1` for tablet
  - `user2` for smartphone

###  Network Topology Screenshot

<img width="454" alt="image" src="https://github.com/user-attachments/assets/9d2a6ac6-754c-4fe0-a3c5-b5f40f3fd623" />

---

### Device-to-Device Connectivity Tests

Connectivity between devices was verified using the `ping` command. All devices responded successfully, confirming functional connections.

<img width="452" alt="image" src="https://github.com/user-attachments/assets/af2191e7-a60a-4e5e-bb43-29df0c73470e" />

<img width="452" alt="image" src="https://github.com/user-attachments/assets/1cc5bcc6-076e-42e0-98f1-6777a37c2572" />



---

## Task 2 – DNS and HTTP Server Integration

### Server Configuration:

| Server      | IP Address    |
|-------------|---------------|
| DNS Server  | 192.168.1.2   |
| HTTP Server | 192.168.1.3   |

- DHCP reservations were updated to assign static IPs to both servers.
- DNS server was configured with an **A record**:
  - `www.pollyvacher.ac.uk` ➝ `192.168.1.3`

### DNS Resolution Test

Used `nslookup` from both a PC and a smartphone to verify domain resolution.

<img width="265" alt="image" src="https://github.com/user-attachments/assets/ed9d296a-918d-4b13-9159-a8f4560f88c9" />


---

### HTTP Access Test

Opened the URL `www.pollyvacher.ac.uk` in a browser on:
- 1 PC
- 1 Smartphone

Both devices successfully loaded the web page hosted on the HTTP server.

<img width="452" alt="image" src="https://github.com/user-attachments/assets/bab41970-e0a0-4bd5-a4b3-0f91349ca878" />

<img width="452" alt="image" src="https://github.com/user-attachments/assets/13c0307a-9095-4859-9603-de278f12f684" />



---

## Conclusion & Reflection

This network successfully simulates a small office LAN with both wired and wireless access, centralised IP management through DHCP, and additional services such as DNS and HTTP. By completing this, I improved my understanding of:
- DHCP reservations
- Wireless security using WPA2 Enterprise
- RADIUS authentication
- DNS record management
- Basic network troubleshooting using `ping` and `nslookup`

---

## Appendix

All configuration screenshots and command outputs are included in the appendix of the main report (PDF).
