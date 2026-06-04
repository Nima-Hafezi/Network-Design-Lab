# Subnetting Design

## Overview

The main network `192.168.10.0/24` was divided into 4 equal subnets using `/26` subnetting.

Each subnet provides:

* 64 total IP addresses
* 62 usable host addresses

This design was selected to:

* Separate departments logically
* Improve network organization
* Reduce broadcast traffic
* Simplify management and troubleshooting

---

## Subnet Allocation

| Department | VLAN | Network ID        | Subnet Mask     | Gateway        | Broadcast      |
| ---------- | ---- | ----------------- | --------------- | -------------- | -------------- |
| Management | 10   | 192.168.10.0/26   | 255.255.255.192 | 192.168.10.1   | 192.168.10.63  |
| Technical  | 20   | 192.168.10.64/26  | 255.255.255.192 | 192.168.10.65  | 192.168.10.127 |
| Financial  | 30   | 192.168.10.128/26 | 255.255.255.192 | 192.168.10.129 | 192.168.10.191 |
| Education  | 40   | 192.168.10.192/26 | 255.255.255.192 | 192.168.10.193 | 192.168.10.255 |

---

## Important Devices

| Device            | IP Address    |
| ----------------- | ------------- |
| Core Switch       | 192.168.10.66 |
| DHCP Server       | 192.168.10.67 |
| Management Laptop | 192.168.99.10 |

---

## Notes

* VLAN 99 was used as a dedicated management VLAN.
* Printer IPs were assigned manually using the last usable address in each subnet.
* Default gateways were configured on router sub-interfaces.
