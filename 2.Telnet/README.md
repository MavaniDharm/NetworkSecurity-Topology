# 🔐 Telnet Remote Access Configuration – Cisco Packet Tracer

## 📌 Project Overview
This project demonstrates how to configure Telnet remote access between routers in a network using Cisco Packet Tracer.

The topology consists of two routers, three switches, and six PCs. Telnet is used to remotely access Router1 from PCs connected to the network.

## 🎯 Objectives
- Configure Telnet remote access on a Cisco router.
- Understand router-to-router connectivity.
- Configure IP addressing on PCs and routers.
- Learn basic Cisco IOS configuration.
- Test remote router access using Telnet.
- Understand password-based authentication.

## 🖥️ Network Topology
The network contains:

- **2 Routers:** Router0 and Router1
- **3 Switches:** Switch0, Switch1, and Switch2
- **6 PCs:** PC0, PC1, PC2, PC3, PC4, and PC5

## 🌐 IP Addressing

| Device | IP Address |
|---|---|
| Router0 | 192.168.1.1 |
| PC0 | 192.168.1.2 |
| PC1 | 192.168.1.1 |
| Router1 | 200.168.1.254 |
| PC2 | 200.168.1.2 |
| PC3 | 200.168.1.1 |
| PC4 | 200.168.1.3 |
| PC5 | 200.168.1.4 |

**Note:** Verify that each device has a unique IP address within its subnet. Router and PC interfaces must not use duplicate IP addresses.

## 🔌 Network Topology Diagram

![Telnet Network Topology](2.image%20of%20topology.png)

## ⚙️ Technologies Used
- Cisco Packet Tracer
- Cisco IOS
- Telnet
- IPv4 Addressing
- Router Remote Access
- Basic Network Security

## 🔑 Telnet Configuration Concept

Telnet allows an administrator to access and manage a network device remotely through a command-line interface.

Example Cisco IOS configuration:

```text
enable
configure terminal
line vty 0 4
password 1234
login
transport input telnet
end
