# 🌐 PAT (Port Address Translation) – Cisco Packet Tracer

## 📌 Project Overview
This project demonstrates Port Address Translation (PAT), also known as NAT Overload, using Cisco Packet Tracer.

PAT allows multiple devices on a private network to share a single translated IP address by using different port numbers to identify their connections.

The topology contains two routers, two switches, and six PCs connected across two networks.

## 🎯 Objectives
- Understand Port Address Translation (PAT).
- Learn the difference between Static NAT, Dynamic NAT, and PAT.
- Configure NAT inside and outside interfaces.
- Allow multiple internal devices to share one translated IP address.
- Understand how port numbers distinguish network connections.
- Verify NAT translations using Cisco IOS commands.

## 🖥️ Network Topology
The network consists of:
- **2 Routers:** Router0 and Router1
- **2 Switches:** Switch0 and Switch1
- **6 PCs:** PC0, PC1, PC2, PC3, PC4, and PC5

## 🌐 IP Addressing Table

| Device | IP Address |
|---|---|
| Router0 LAN Gateway | 192.168.1.254 |
| PC0 | 192.168.1.3 |
| PC1 | 192.168.1.2 |
| PC2 | 192.168.1.1 |
| Router1 LAN Gateway | 193.168.1.254 |
| PC3 | 193.168.1.3 |
| PC4 | 193.168.1.1 |
| PC5 | 193.168.1.2 |

**Left LAN:** `192.168.1.0/24`  
**Right LAN:** `193.168.1.0/24`

## 🔌 Network Topology Diagram

![PAT Network Topology](2.image%20of%20topology.png)

## ⚙️ Technologies Used
- Cisco Packet Tracer
- Cisco IOS
- Port Address Translation (PAT)
- NAT Overload
- IPv4 Addressing
- Access Control Lists (ACLs)
- Network Connectivity Testing

## 🔑 PAT Configuration

Example configuration for Router0:

### 1. Configure NAT Interfaces

```text
enable
configure terminal

interface gigabitEthernet 0/0
ip nat inside
exit

interface serial 0/0/0
ip nat outside
exit
```

### 2. Identify the Internal Network

```text
access-list 1 permit 192.168.1.0 0.0.0.255
```

### 3. Enable PAT Using the Outside Interface Address

```text
ip nat inside source list 1 interface serial 0/0/0 overload
```

**Note:** These are example commands. Use the actual interface names and addresses configured in your Packet Tracer project. The outside interface must have a valid IP address, and routing must be configured correctly.

## 🧪 Testing
1. Configure IP addresses and default gateways on all PCs.
2. Configure routing between Router0 and Router1.
3. Configure NAT inside and outside interfaces on Router0.
4. Apply the ACL and PAT configuration.
5. Generate traffic from multiple PCs on the internal network.
6. Verify translations using:

   `show ip nat translations`

7. Check NAT statistics using:

   `show ip nat statistics`

8. Confirm that multiple internal connections use the translated address with different port mappings.

## 📚 Learning Outcomes
- Understanding PAT and NAT Overload.
- Sharing one translated IP address across multiple connections.
- Understanding the role of port numbers in translation.
- Configuring NAT interfaces and ACLs.
- Verifying NAT translations.
- Troubleshooting routing and NAT issues.

## ⚠️ Important Notes
- PAT allows multiple internal connections to share one translated IP address.
- The outside interface must be correctly configured.
- Routing must be configured for successful communication.
- The actual PAT configuration should match the
