# Enterprise VLAN, LACP & DHCP Network Lab

## 📌 Project Overview
This project simulates a small enterprise network using Cisco switches and routers in a virtual environment (Packet Tracer).

The design focuses on real-world networking concepts including:
- VLAN segmentation
- Inter-VLAN routing using Layer 3 switch
- EtherChannel (LACP) for redundancy and bandwidth aggregation
- DHCP services with relay (ip helper-address)
- Trunking between core and access switches

---

## 🏗️ Network Topology

The network consists of:

- 1 Layer 3 Core Switch
- 2 Access Switches (SW-1, SW-2)
- 1 Router (Internet simulation)
- 1 DHCP Server (External)
- 6 PCs distributed across VLANs

---

## 🧩 VLAN Design

| VLAN ID | Name   | Network           | Purpose   |
|----------|--------|------------------|-----------|
| 10       | HR     | 10.10.10.0/24    | HR Dept   |
| 20       | IT     | 10.10.20.0/24    | IT Dept   |
| 30       | STAFF  | 10.10.30.0/24    | Staff     |

---

## ⚙️ Key Technologies Used

- VLANs (Segmentation)
- Inter-VLAN Routing (Layer 3 Switch)
- EtherChannel (LACP)
- DHCP Relay (ip helper-address)
- Trunk Links (802.1Q)
- Cisco IOS Switching

---

## 🔌 Switch Design Summary

### Core Switch
- Layer 3 routing enabled (`ip routing`)
- SVIs configured for VLANs 10, 20, 30
- DHCP relay configured using `ip helper-address`
- EtherChannel links to access switches

### Access Switches (SW-1 / SW-2)
- VLAN-based port assignment
- Trunk links to core switch via Port-Channels
- End devices assigned to VLANs

---

## 🔍 Verification Commands

Use the following commands to verify the network:

```bash
show vlan brief
show ip interface brief
show interfaces trunk
show etherchannel summary
```
---

## 🎯 Learning Outcomes

This project provides hands-on experience in:

- Designing and implementing an enterprise network topology
- Configuring VLANs for network segmentation and isolation
- Implementing Inter-VLAN routing using a Layer 3 switch
- Setting up EtherChannel (LACP) for link redundancy and bandwidth aggregation
- Configuring DHCP services with relay (ip helper-address)
- Understanding and applying Cisco switching concepts in real environments

---
