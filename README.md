# Multi-VLAN Network Design with Wired and Wireless Client Isolation

A Cisco Packet Tracer project demonstrating VLAN segmentation, wired and wireless connectivity, and client isolation using a Layer 2 switch and an Access Point.

---

## Project Overview

This project simulates a small office network consisting of two departments connected to a Cisco 2960 switch. The network is divided into separate VLANs to isolate traffic between departments while allowing communication among devices within the same VLAN.

A wireless laptop is connected through an Access Point and assigned to the IT department, demonstrating how wireless clients can participate in a VLAN.

This project focuses on the fundamentals of VLAN configuration, network segmentation, and connectivity testing.

---

## Network Topology

### Devices Used

- Cisco 2960-24TT Switch
- Cisco Access Point
- 4 Desktop PCs
- 1 Wireless Laptop

```
                    Cisco 2960 Switch
         ┌────────────┬────────────┬────────────┐
         │            │            │            │
       PC0          PC1          PC2          PC3
   (VLAN 10)    (VLAN 10)    (VLAN 20)    (VLAN 20)
                                          │
                                    Access Point
                                          │
                                      Laptop2
                                     (VLAN 20)
```

---

## VLAN Configuration

### VLAN 10 — Sales Department

| Device | IP Address |
|---------|------------|
| PC0 | 192.168.10.1 |
| PC1 | 192.168.10.2 |

---

### VLAN 20 — IT Department

| Device | IP Address |
|---------|------------|
| PC2 | 192.168.20.1 |
| PC3 | 192.168.20.3 |
| Laptop2 | 192.168.20.2 |

Subnet Mask (All Devices)

```
255.255.255.0
```

---

## Verification

Connectivity was verified using the **Ping** command.

### Successful Tests

- Devices within VLAN 10 communicate successfully.
- Devices within VLAN 20 communicate successfully.
- The wireless laptop communicates with all devices in VLAN 20.

### Expected Failed Tests

Devices located in different VLANs are unable to communicate because no Layer 3 routing is configured.

This confirms that VLAN isolation is working as intended.

---

## Learning Outcome

Through this project, I gained practical experience configuring VLANs in Cisco Packet Tracer and understanding how Layer 2 switches isolate traffic between departments. I also learned how wireless clients can be integrated into a VLAN through an Access Point while maintaining proper network segmentation. Connectivity testing using ICMP verified that devices within the same VLAN could communicate successfully, while communication across different VLANs was intentionally blocked due to the absence of Layer 3 routing.

---
