# 🔀 RIP Routing – Three-Router Network

A Cisco Packet Tracer networking project demonstrating how to configure and implement **RIPv2 (Routing Information Protocol)** to enable communication between three different LAN networks through three interconnected routers.

---

## 📌 Project Overview

This project contains three LANs connected through three Cisco routers in a triangular topology.

Each router connects:

- One local LAN
- Two neighboring routers

RIPv2 is configured on all three routers to dynamically exchange routing information and learn remote networks.

### Network Topology

```text
                         ┌─────────────────────┐
                         │       LAN 10        │
                         │  192.168.10.0/24    │
                         │                     │
                         │   PC4     PC5       │
                         └──────────┬──────────┘
                                    │
                             192.168.10.254
                                    │
                                   R2
                              /           \
                             /             \
                    172.16.0.2           172.18.0.1
                         /                   \
                        /                     \
                 172.16.0.1               172.18.0.2
                      R0──────────────────────R1
                         172.17.0.1    172.17.0.2
                             │             │
                      192.168.20.254   192.168.30.254
                             │             │
                    ┌────────┴───┐     ┌───┴────────┐
                    │   LAN 20   │     │   LAN 30   │
                    │192.168.20.0│     │192.168.30.0│
                    │    /24     │     │    /24     │
                    │            │     │            │
                    │ PC0   PC1  │     │ PC2   PC3  │
                    └────────────┘     └────────────┘
