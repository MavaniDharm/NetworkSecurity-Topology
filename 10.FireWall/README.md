# 🔥 Firewall Topology – Cisco ASA 5506-X

## 📌 Project Overview
This project demonstrates a network topology using a Cisco ASA 5506-X firewall in Cisco Packet Tracer. The firewall separates the network into three security zones: Inside Network, DMZ Network, and Outside Network.

## 🎯 Objectives
- Understand firewall architecture and network segmentation.
- Configure Inside, DMZ, and Outside security zones.
- Learn IP addressing and interface configuration.
- Understand how firewalls control traffic between networks.
- Practice basic network security concepts.

## 🖥️ Network Components
- Cisco ASA 5506-X Firewall
- Cisco 2960-24TT Switches
- PCs and Server
- Cisco Packet Tracer

## 🌐 IP Addressing Scheme

| Network | Device | IP Address |
|---|---|---|
| Inside | PC0 | 192.168.1.1 |
| Inside | PC1 | 192.168.1.2 |
| Inside | PC2 | 192.168.1.3 |
| Inside | ASA Firewall Interface | 192.168.1.254 |
| DMZ | PC3 | 10.0.0.1 |
| DMZ | PC4 | 10.0.0.2 |
| DMZ | PC5 | 10.0.0.3 |
| DMZ | ASA Firewall Interface | 10.0.0.254 |
| Outside | PC6 | 182.16.0.10 |
| Outside | PC7 | 182.16.0.11 |
| Outside | Server0 | 182.16.0.12 |
| Outside | ASA Firewall Interface | 182.16.0.254 |

## 🗺️ Network Topology
The network consists of three separate segments:

1. **Inside Network:** Contains internal client devices.
2. **DMZ Network:** Contains devices placed in a separate network zone.
3. **Outside Network:** Represents an external network containing clients and a server.

The Cisco ASA firewall connects all three segments and provides a central point for traffic control.

## 🔐 Security Concepts
- Firewall-based network segmentation
- Inside, DMZ, and Outside security zones
- Traffic filtering between network segments
- IP addressing and subnet planning
- Basic firewall security policies

## 🧪 Testing
The topology can be tested using:
- Ping connectivity tests between devices.
- Verification of IP addresses and default gateways.
- Firewall interface and routing checks.
- Access-control testing between the three network zones.

**Note:** Successful connectivity depends on the actual firewall configuration and security policies.

## 🛠️ Tools Used
- Cisco Packet Tracer
- Cisco ASA 5506-X Firewall
- Cisco 2960 Switches

## 📚 Learning Outcomes
- Understood the role of a firewall in network security.
- Learned the purpose of Inside, DMZ, and Outside network zones.
- Practiced network segmentation and IP addressing.
- Explored basic firewall traffic-control concepts.

## 👨‍💻 Author
**Dharm Mavani**

Cybersecurity Student | Networking & Network Security Learner

## ⚠️ Disclaimer
This project is created for educational purposes in a simulated lab environment.
