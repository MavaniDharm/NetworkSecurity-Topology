# 🔐 Extended ACL Configuration – Cisco Packet Tracer

## 📌 Project Overview
This project demonstrates the configuration of an Extended Access Control List (ACL) using Cisco Packet Tracer.

The network consists of three departments: Sales, Marketing, and Admin. Extended ACLs are used to control traffic based on source IP address, destination IP address, and protocol.

The main objective of this project is to **block ping (ICMP) traffic from the Sales network to the Admin network**, while allowing other required network communication.

## 🎯 Objectives
- Understand Extended ACLs in Cisco networking.
- Control traffic between different departments.
- Block ICMP traffic from Sales to Admin.
- Learn how to filter traffic using source and destination IP addresses.
- Configure routers and routing between networks.
- Test ACL rules using the ping command.

## 🖥️ Network Topology

The network consists of:

- **3 Routers:** Router0, Router1, and Router2
- **3 Switches:** Switch0, Switch1, and Switch2
- **6 PCs:** PC0, PC1, PC2, PC3, PC4, and PC5
- **3 Departments:** Sales, Marketing, and Admin

## 🌐 IP Addressing Table

| Device | Department | IP Address |
|---|---|---|
| PC0 | Sales | 182.10.0.1 |
| PC1 | Sales | 182.11.0.2 |
| Router0–Router1 Link | WAN Link | 10.0.0.1 / 10.0.0.2 |
| PC2 | Marketing | 172.12.0.1 |
| PC3 | Marketing | 172.13.0.2 |
| Router1–Router2 Link | WAN Link | 11.0.0.1 / 11.0.0.2 |
| PC4 | Admin | 192.168.14.1 |
| PC5 | Admin | 192.168.15.2 |

**Note:** Verify the subnet masks and gateway addresses configured on each device in Packet Tracer.

## 🔌 Network Topology Diagram

![Extended ACL Topology](2.image%20of%20topology.png)

## ⚙️ Technologies Used
- Cisco Packet Tracer
- Cisco IOS
- Extended Access Control Lists (ACLs)
- IPv4 Addressing
- ICMP Protocol
- Inter-Router Routing
- Network Security

## 🔑 Extended ACL Configuration

### Example: Block Ping from Sales to Admin

The following example blocks ICMP traffic from the Sales network to the Admin network.

```text
enable
configure terminal
ip access-list extended BLOCK-SALES-PING
deny icmp 182.10.0.0 0.0.255.255 192.168.0.0 0.0.255.255 echo
permit ip any any
```

Apply the ACL to the appropriate router interface:

```text
interface <interface-id>
ip access-group BLOCK-SALES-PING in
```

**Important:** These commands are an example. Confirm the actual network ranges, subnet masks, and interface direction before applying the ACL.

## 🧪 Testing
1. Configure IP addresses and default gateways on all PCs.
2. Configure routing between Sales, Marketing, and Admin.
3. Test connectivity between the departments using `ping`.
4. Apply the Extended ACL to the appropriate interface.
5. Ping an Admin PC from a Sales PC.
6. Verify that the specified ICMP traffic is blocked.
7. Test whether permitted traffic, such as other IP traffic, still works.
8. Verify ACL rules using:

   `show access-lists`

## 📚 Learning Outcomes
- Understanding Extended ACLs.
- Filtering network traffic using source and destination IP addresses.
- Blocking specific protocols such as ICMP.
- Controlling communication between departments.
- Understanding ACL placement and direction.
- Troubleshooting network connectivity.

## ⚠️ Security Notes
- Extended ACLs can filter traffic by protocol, source, destination, and port.
- ACLs should be placed carefully to avoid blocking legitimate traffic.
- ACLs include an implicit `deny any` at the end.
- Test all ACL rules before using them in a production network.

## 📝 Project Type
Network Security Lab – Cisco Packet Tracer

---
⭐ If you find this project useful, consider starring this repository!
