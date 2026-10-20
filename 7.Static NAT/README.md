# 🌐 Static NAT Configuration – Cisco Packet Tracer

## 📌 Project Overview
This project demonstrates Static Network Address Translation (NAT) using Cisco Packet Tracer.

Static NAT maps a private IP address to a specific public IP address. This mapping remains fixed and allows devices on an internal network to communicate with external networks using translated IP addresses.

The topology consists of two routers, two switches, and six PCs connected across two networks.

## 🎯 Objectives
- Understand Static NAT concepts.
- Configure inside and outside NAT interfaces.
- Map private IP addresses to public IP addresses.
- Understand how NAT translates IP addresses.
- Test connectivity between two networks.
- Learn basic Cisco networking and NAT configuration.

## 🖥️ Network Topology
The network contains:

- **2 Routers:** Router0 and Router1
- **2 Switches:** Switch0 and Switch1
- **6 PCs:** PC0, PC1, PC2, PC3, PC4, and PC5

## 🌐 IP Addressing Table

| Device | IP Address |
|---|---|
| PC0 | 192.168.1.1 |
| PC1 | 192.168.1.2 |
| PC2 | 192.168.1.3 |
| Router0 LAN Gateway | 192.168.1.254 |
| PC3 | 193.168.1.1 |
| PC4 | 193.168.1.3 |
| PC5 | 193.168.1.2 |
| Router1 LAN Gateway | 193.168.1.254 |

**Left Network:** `192.168.1.0/24`  
**Right Network:** `193.168.1.0/24`

## 🔌 Network Topology Diagram

![Static NAT Topology](2.image%20of%20topology.png)

## ⚙️ Technologies Used
- Cisco Packet Tracer
- Cisco IOS
- Static Network Address Translation (NAT)
- IPv4 Addressing
- Router Configuration
- Network Connectivity Testing

## 🔑 Static NAT Configuration

### Example Configuration

Static NAT maps one inside-local address to one inside-global address.

```text
enable
configure terminal

interface gigabitEthernet 0/0
ip nat inside
exit

interface serial 0/0/0
ip nat outside
exit

ip nat inside source static 192.168.1.1 200.0.0.1
```

**Note:** These commands are examples. Use the actual interface names and IP addresses configured in your Packet Tracer topology.

### Command Explanation
- `ip nat inside` identifies the internal network interface.
- `ip nat outside` identifies the external network interface.
- `ip nat inside source static` creates a permanent one-to-one IP address mapping.

## 🧪 Testing
1. Configure IP addresses and default gateways on all PCs.
2. Configure router interfaces and routing between networks.
3. Identify the inside and outside NAT interfaces.
4. Configure the required Static NAT mappings.
5. Test connectivity using `ping`.
6. Verify NAT translations using:

   `show ip nat translations`

7. Check NAT statistics using:

   `show ip nat statistics`

## 📚 Learning Outcomes
- Understanding Static NAT.
- Learning private-to-public IP address translation.
- Configuring NAT inside and outside interfaces.
- Understanding one-to-one address mapping.
- Troubleshooting network connectivity.
- Verifying NAT translations on Cisco routers.

## ⚠️ Important Note
The topology image shows the LAN addressing, but it does not display the exact NAT mappings or router-to-router link addresses.

Static NAT requires suitable routing, correct interface configuration, and valid address mappings. Update the example commands to match your actual Packet Tracer configuration.

## 📝 Project Type
Networking and Network Security Lab – Cisco Packet Tracer

---
⭐ If you find this project useful, consider starring this repository!
