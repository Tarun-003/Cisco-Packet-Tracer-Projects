# VLAN Configuration – Cisco Packet Tracer

## Overview

Configured multiple VLANs on a Cisco 2960 switch to logically separate departments and understand network segmentation.

## Devices Used

- 1 Cisco 2960 Switch
- 6 PCs

## IP Addressing

| VLAN | Department | Network |
|---|---|---|
| VLAN 10 | SALES | 192.168.10.0/24 |
| VLAN 20 | HR | 192.168.20.0/24 |
| VLAN 30 | IT | 192.168.30.0/24 |

## Configuration

```cisco
enable
configure terminal

vlan 10
name SALES
exit

vlan 20
name HR
exit

vlan 30
name IT
exit

interface range fa0/1-2
switchport mode access
switchport access vlan 10
exit

interface range fa0/3-4
switchport mode access
switchport access vlan 20
exit

interface range fa0/5-6
switchport mode access
switchport access vlan 30
exit

end
write memory
```

## Verification

```cisco
show vlan brief
show interfaces status
show mac address-table
```

## Key Learnings

- VLAN creation and configuration.
- Access port assignment.
- Network segmentation.
- Communication within the same VLAN.

## Cybersecurity Relevance

VLANs improve network organization and help isolate different departments.

**Tools:** Cisco Packet Tracer  
**Domain:** Networking | Cybersecurity | CCNA  
**Author:** Tarun SU
