# 🔐 Standard ACL Configuration – Cisco Packet Tracer

## 📌 Project Overview
This project demonstrates the configuration of a Standard Access Control List (ACL) using Cisco Packet Tracer.

A Standard ACL filters network traffic based on the source IPv4 address. In this topology, two routers connect two different networks, allowing the administrator to control which source addresses can access the destination network.

## 🎯 Objectives
- Understand Standard ACLs in Cisco networking.
- Configure access control rules on a router.
- Permit or deny traffic based on source IP addresses.
- Understand wildcard masks.
- Test connectivity between different networks.
- Learn basic network access control.

## 🖥️ Network Topology

The network consists of:
- **2 Routers:** Router0 and Router1
- **2 Switches:** Switch0 and Switch1
- **6 PCs:** PC0, PC1, PC2, PC3, PC4, and PC5

## 🌐 IP Addressing Table

| Device | IP Address |
|---|---|
| Router0 | 192.168.1.254 |
| PC0 | 192.168.1.1 |
| PC1 | 192.168.1.2 |
| PC2 | 192.168.1.3 |
| Router1 | 65.0.0.254 |
| PC3 | 65.0.0.1 |
| PC4 | 65.0.0.3 |
| PC5 | 65.0.0.2 |

**Network 1:** `192.168.1.0/24`  
**Network 2:** `65.0.0.0/24`

## 🔌 Network Topology Diagram

![Standard ACL Topology](2.image%20of%20topology.png)

## ⚙️ Technologies Used
- Cisco Packet Tracer
- Cisco IOS
- Standard Access Control List (ACL)
- IPv4 Addressing
- Wildcard Masks
- Network Security

## 🔑 Standard ACL Configuration

The topology shows the following ACL rule:

```text
access-list 1 deny 192.168.1.0 0.0.0.255
