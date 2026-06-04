# VLAN Design

## Overview

The network was divided into multiple VLANs to separate departments and improve security, scalability, and network management.

Each department operates inside its own broadcast domain.

---

## VLAN Structure

| VLAN ID | Name       | Purpose                     |
| ------- | ---------- | --------------------------- |
| 10      | MANAGEMENT | Management department       |
| 20      | TECHNICAL  | Technical department        |
| 30      | FINANCIAL  | Financial department        |
| 40      | EDUCATION  | Education department        |
| 99      | MGMT-ONLY  | Network management          |
| 999     | NATIVE     | Native VLAN for trunk links |

---

## Trunk Configuration

Trunk links were configured between:

* Core switch and router
* Core switch and access switches

802.1Q encapsulation was used to carry multiple VLANs across trunk interfaces.

Only required VLANs were allowed on trunk links to improve security.

---

## Native VLAN

VLAN 999 was configured as the native VLAN.

The default VLAN 1 was intentionally avoided as a basic security best practice.

---

## Access Ports

End-user devices were connected using access ports assigned to their corresponding VLANs.

This design provides:

* Logical separation
* Better traffic management
* Easier troubleshooting
* Reduced broadcast traffic
