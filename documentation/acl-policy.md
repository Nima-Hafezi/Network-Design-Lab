# ACL Policy Documentation

## Overview

Access Control Lists (ACLs) were implemented to improve network security and control traffic between VLANs.

The ACL policies were designed to:

* Restrict unauthorized access
* Limit unnecessary traffic
* Protect management access to network devices

---

## Router Management Access

SSH access to the router is restricted to:

* Management Laptop (`192.168.99.10`)
* DHCP Server (`192.168.10.67`)

All other remote management access attempts are denied.

---

## User Traffic Restrictions

The Management, Financial, and Education VLANs are restricted to HTTP and HTTPS traffic only.

Allowed traffic:

* TCP port 80 (HTTP)
* TCP port 443 (HTTPS)

Blocked traffic:

* ICMP (Ping)
* Telnet
* Other unauthorized protocols

---

## Security Goals

The ACL implementation demonstrates:

* Basic traffic filtering
* Segmentation enforcement
* Controlled management access
* Principle of least privilege

---

## Testing

ACL functionality was verified by:

* Successful HTTP/HTTPS communication
* Blocked ICMP ping requests
* Restricted unauthorized SSH access
