# 🌐 Dynamic NAT Configuration – Cisco Packet Tracer

## 📌 Project Overview
This project demonstrates Dynamic Network Address Translation (NAT) using Cisco Packet Tracer.

Dynamic NAT translates private IP addresses into public IP addresses using a pool of available global IP addresses. Unlike Static NAT, the mapping is created dynamically when internal devices initiate communication.

The topology consists of two routers, two switches, and six PCs connected across two different networks.

## 🎯 Objectives
- Understand Dynamic NAT concepts.
- Configure NAT inside and outside interfaces.
- Create a pool of global IP addresses.
- Configure an ACL to identify traffic eligible for translation.
- Test communication between different networks.
- Verify dynamic NAT translations.

## 🖥️ Network Topology
The network contains:

- **2 Routers:** Router0 and Router1
- **2 Switches:** Switch0 and Switch1
- **6 PCs:** PC0, PC1, PC2, PC3, PC4, and PC5

## 🌐 IP Addressing Table

| Device | IP Address |
|---|---|
| Router0 LAN Gateway | 192.168.1.254 |
| PC0 | 192.168.1.1 |
| PC1 | 192.168.1.2 |
| PC2 | 192.168.1.3 |
| Router0–Router1 Link | 10.0.0.1 / 10.0.0.2 |
| Router1 LAN Gateway | 193.168.1.254 |
| PC3 | 193.168.1.1 |
| PC4 | 193.168.1.2 |
| PC5 | 193.168.1.3 |

**Left LAN:** `192.168.1.0/24`  
**Router-to-Router Network:** `10.0.0.0`  
**Right LAN:** `193.168.1.0/24`

## 🔌 Network Topology Diagram

![Dynamic NAT Topology](2.image%20of%20topology.png)

## ⚙️ Technologies Used
- Cisco Packet Tracer
- Cisco IOS
- Dynamic Network Address Translation (NAT)
- IPv4 Addressing
- Access Control Lists (ACLs)
- NAT Address Pools

## 🔑 Dynamic NAT Configuration

The following is an example configuration for Router0.

### 1. Configure the NAT Inside Interface

```text
enable
configure terminal

interface gigabitEthernet 0/0
ip nat inside
exit
```

### 2. Configure the NAT Outside Interface

```text
interface serial 0/0/0
ip nat outside
exit
```

### 3. Create an ACL for the Internal Network

```text
access-list 1 permit 192.168.1.0 0.0.0.255
```

### 4. Create a NAT Pool

```text
ip nat pool NAT-POOL 10.0.0.10 10.0.0.20 netmask 255.255.255.0
```

### 5. Link the ACL to the NAT Pool

```text
ip nat inside source list 1 pool NAT-POOL
```

**Important:** These commands are examples only. The NAT pool must use a suitable range of global addresses that is valid for your network design. The actual interface names, NAT pool, routing, and address ranges must match your Packet Tracer configuration.

## 🧪 Testing
1. Configure IP addresses and default gateways on all PCs.
2. Configure routing between the routers.
3. Configure NAT inside and outside interfaces on Router0.
4. Configure the ACL and NAT pool.
5. Generate traffic from the internal network.
6. Verify translations using:

   `show ip nat translations`

7. Check NAT statistics using:

   `show ip nat statistics`

## 📚 Learning Outcomes
- Understanding Dynamic NAT.
- Learning the difference between Static NAT and Dynamic NAT.
- Configuring NAT pools and ACLs.
- Understanding inside-local and inside-global addresses.
- Verifying dynamic address translations.
- Troubleshooting NAT and routing.

## ⚠️ Important Notes
- Dynamic NAT uses a pool of global IP addresses.
- Available translations depend on the size of the pool.
- Routing must be configured correctly for end-to-end communication.
- The NAT pool must not conflict with existing network addresses.
- NAT translations are generally created when matching traffic is generated.

## 📝 Project Type
Networking and Network Security Lab – Cisco Packet Tracer

---
⭐ If you find this project useful, consider starring this repository!
