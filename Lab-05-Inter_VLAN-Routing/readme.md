# Inter-VLAN Routing – Cisco Packet Tracer

## Overview

Configured Inter-VLAN Routing using the Router-on-a-Stick method to enable communication between different VLANs through a single physical router interface.

## Devices Used

- 1 Router
- 1 Cisco 2960 Switch
- 6 PCs

## IP Addressing

| VLAN | Network | Default Gateway |
|---|---|---|
| VLAN 10 | 192.168.10.0/24 | 192.168.10.1 |
| VLAN 20 | 192.168.20.0/24 | 192.168.20.1 |

## Configuration

**Switch CLI:**

```cisco
enable
configure terminal

vlan 10
name STUDENTS
exit

vlan 20
name FACULTY
exit

interface range fa0/1-3
switchport mode access
switchport access vlan 10
exit

interface range fa0/4-6
switchport mode access
switchport access vlan 20
exit

interface fa0/24
switchport mode trunk
no shutdown
exit

end
write memory
```

**Router CLI:**

```cisco
enable
configure terminal

interface g0/0/0
no shutdown
exit

interface g0/0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0
exit

interface g0/0/0.20
encapsulation dot1Q 20
ip address 192.168.20.1 255.255.255.0
exit

end
write memory
```

## Verification

```cisco
show vlan brief
show interfaces trunk
show ip interface brief
show ip route
```

Test connectivity:

```bash
ping 192.168.20.10
```

## Key Learnings

- VLAN configuration.
- Trunk port configuration.
- Router-on-a-Stick.
- Subinterfaces and 802.1Q encapsulation.
- Communication between VLANs.

## Cybersecurity Relevance

Inter-VLAN routing helps understand traffic flow between network segments and where access control policies can be applied.

**Tools:** Cisco Packet Tracer  
**Domain:** Networking | Cybersecurity | CCNA  
**Author:** Tarun SU
