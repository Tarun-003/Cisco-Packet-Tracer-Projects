# 📌 Lab 01 - Static Routing

## Objective

Configure static routing between two different LANs connected using two Cisco routers.

---

## Network Topology

![Topology](topology.png)

---

## Devices Used

- 2 Cisco Routers
- 2 Cisco Switches
- 6 PCs

---

## IP Addressing

### Left LAN

| Device | IP Address |
|---------|------------|
| Router0 | 192.168.1.254 |
| PC0 | 192.168.1.1 |
| PC1 | 192.168.1.2 |
| PC2 | 192.168.1.3 |

---

### Right LAN

| Device | IP Address |
|---------|------------|
| Router1 | 192.168.2.254 |
| PC3 | 192.168.2.1 |
| PC4 | 192.168.2.2 |
| PC5 | 192.168.2.3 |

---

### Router-to-Router Link

| Router | Interface | Address |
|---------|-----------|----------|
| Router0 | G0/0/1 | 10.0.0.1 |
| Router1 | G0/0/1 | 10.0.0.2 |

Subnet Mask

```
255.255.255.252
```

---

## Routing

### Router0

```
ip route 192.168.2.0 255.255.255.0 10.0.0.2
```

### Router1

```
ip route 192.168.1.0 255.255.255.0 10.0.0.1
```

---

## Verification

Successfully tested connectivity using:

- Ping PC0 → PC5 ✅
- Ping PC2 → PC3 ✅
- Ping Router0 → Router1 ✅

---

## Skills Learned

- Static Routing
- Router Configuration
- IPv4 Addressing
- Subnetting
- Default Gateway Configuration
- Network Troubleshooting

---

## Tools

- Cisco Packet Tracer
- Ubuntu Linux
- Git
- GitHub

---

## Author

**Tarun S U**
