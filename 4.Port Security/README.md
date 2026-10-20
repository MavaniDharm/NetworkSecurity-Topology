# 🔐 Port Security Configuration – Cisco Packet Tracer

## 📌 Project Overview
This project demonstrates the implementation of Port Security on a Cisco Catalyst 2960 switch using Cisco Packet Tracer.

Port Security helps protect a switch port by restricting which devices can connect to it based on their MAC addresses.

The topology includes one router, one switch, and two PCs connected to the same network.

## 🎯 Objectives
- Understand Cisco Switch Port Security.
- Restrict unauthorized devices from accessing the network.
- Learn MAC address-based access control.
- Configure switch ports to allow specific devices.
- Understand Port Security violation modes.
- Test network connectivity in Cisco Packet Tracer.

## 🖥️ Network Topology

The network consists of:

- **1 Router:** Router1
- **1 Switch:** Cisco 2960-24TT Switch0
- **2 PCs:** PC3 and PC4

## 🌐 IP Addressing Table

| Device | IP Address |
|---|---|
| Router1 | 192.168.1.254 |
| PC3 | 192.168.1.2 |
| PC4 | 192.168.1.1 |

**Network Address:** `192.168.1.0/24`  
**Subnet Mask:** `255.255.255.0`  
**Default Gateway:** `192.168.1.254`

## 🔌 Network Topology Diagram

![Port Security Topology](2.image%20of%20topology.png)

## ⚙️ Technologies Used
- Cisco Packet Tracer
- Cisco Catalyst 2960 Switch
- Switch Port Security
- MAC Address Filtering
- IPv4 Addressing
- Network Security Fundamentals

## 🔑 Port Security Configuration

Example configuration for a switch access port:

```text
enable
configure terminal
interface fastEthernet 0/1
switchport mode access
switchport port-security
switchport port-security maximum 1
switchport port-security mac-address sticky
switchport port-security violation shutdown
end
