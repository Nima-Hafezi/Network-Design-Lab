# Project Notes

## Project Goal

The purpose of this project was to design and simulate a small enterprise network using Cisco Packet Tracer while applying practical networking and security concepts.

---

## Key Concepts Practiced

* VLAN segmentation
* Inter-VLAN Routing
* DHCP and DHCP Relay
* Access Control Lists (ACL)
* SSH remote management
* Subnetting
* Network documentation

---

## Router-on-a-Stick

Router-on-a-Stick was selected for Inter-VLAN Routing because:

* It is simple to implement in small networks
* It reduces hardware requirements
* It is commonly used in networking labs and educational environments

---

## DHCP Relay

A centralized DHCP server was used for easier IP address management.

Since DHCP broadcasts do not cross VLAN boundaries, `ip helper-address` was configured on router sub-interfaces.

---

## Management VLAN

VLAN 99 was created as a dedicated management VLAN to separate network administration traffic from normal user traffic.

---

## Security Considerations

Basic security practices implemented in this project include:

* SSH instead of Telnet
* Restricted trunk VLANs
* Dedicated native VLAN
* ACL-based traffic filtering
* Controlled management access

---

## Skills Improved During This Project

* Network design
* Troubleshooting
* VLAN configuration
* Cisco CLI usage
* Network documentation
* Basic security implementation
