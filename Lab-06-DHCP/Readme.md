# DHCP Server Configuration – Cisco Packet Tracer

## Overview

Configured a dedicated Server-PT device as a DHCP server to automatically assign IP addresses to four PCs through a Cisco 2960 switch.

## Devices Used

- 1 Router (PT800)
- 1 Server-PT
- 1 Cisco 2960 Switch
- 4 PCs

## IP Addressing

| Device | IP Address |
|---|---|
| Router | 192.168.1.1 |
| DHCP Server | 192.168.1.2 |
| PC0–PC3 | DHCP |
| Subnet Mask | 255.255.255.0 |

## Configuration

**Router:**
- Configured LAN interface.
- IP Address: `192.168.1.1`
- Enabled interface using `no shutdown`.

**DHCP Server:**
- Enabled DHCP service.
- Pool Name: `LAN_POOL`
- Start IP: `192.168.1.10`
- Default Gateway: `192.168.1.1`
- DNS: `8.8.8.8`
- Subnet Mask: `255.255.255.0`

**Switch CLI:**

```cisco
enable
configure terminal
hostname SW1

interface range fa0/1-6
switchport mode access
no shutdown

end
write memory
```

**PC Configuration:**

- Desktop → IP Configuration → DHCP.
- Repeated for all four PCs.

## Verification

```bash
ipconfig
ping 192.168.1.1
ping 192.168.1.2
```

## Key Learnings

- DHCP server configuration.
- Automatic IP address assignment.
- DHCP DORA process.
- Router and switch connectivity.
- DHCP client-server communication.

## Cybersecurity Relevance

Learned about DHCP-related threats such as Rogue DHCP Servers, DHCP Starvation and DHCP Spoofing.

**Tools:** Cisco Packet Tracer  
**Domain:** Networking | Cybersecurity | CCNA  
**Author:** Tarun SU
