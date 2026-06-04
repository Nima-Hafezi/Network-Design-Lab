# Troubleshooting Notes

## DHCP Clients Not Receiving Gateway

### Problem

Some DHCP clients received IP addresses but did not receive the correct default gateway.

### Cause

The default Packet Tracer `serverPool` configuration conflicted with the custom DHCP scopes.

### Solution

The default DHCP pool was disabled and custom DHCP scopes were configured manually.

---

## VLAN Communication Failure

### Problem

Devices in different VLANs could not communicate.

### Cause

Inter-VLAN Routing was not configured correctly on the router sub-interfaces.

### Solution

Router-on-a-Stick configuration was completed using 802.1Q encapsulation.

---

## SSH Access Failure

### Problem

SSH connections to the router failed.

### Cause

RSA keys and domain name were not configured before enabling SSH.

### Solution

Configured:

* `ip domain-name`
* RSA key generation
* SSH version 2

---

## Trunk Issues

### Problem

VLAN traffic was not passing correctly between switches.

### Cause

Incorrect trunk VLAN configuration.

### Solution

Configured:

* Trunk mode
* Allowed VLAN list
* Native VLAN 999

---

## ACL Blocking Traffic

### Problem

Ping requests between VLANs failed.

### Cause

ACL rules only allowed HTTP and HTTPS traffic.

### Solution

Verified that ACL filtering was working correctly as designed.
