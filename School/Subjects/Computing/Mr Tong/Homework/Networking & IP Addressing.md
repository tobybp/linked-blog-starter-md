[[Computing]]
#19/11/25
## What is an IP Address?
- An IP address is a unique numerical identifier assigned to a device (host) on a network.
- Used to allow devices to communicate over the Internet or a local network.
- IPv4 format: four 8-bit octets (e.g., 142.67.210.8).
- Range: 0.0.0.0 to 255.255.255.255 (≈4.3 billion addresses).

---
## IPv4 vs IPv6
### IPv4
- 32-bit address.
- Limited supply → shortage due to growing number of devices.
### IPv6
- 128-bit address, written in hexadecimal (e.g., 3dfb:1730:4935:0007:0340:fe2f:fb71:48af).
- around 3.4 × 10³⁸ possible addresses.
- Designed to solve IPv4 exhaustion.

---
## Public vs Private (Non-Routable) IP Addresses
### Private ranges (non-routable):
- 10.0.0.0 – 10.255.255.255
- 172.16.0.0 – 172.31.255.255
- 192.168.0.0 – 192.168.255.255
These addresses can only be used within LANs or private WANs.
### Public addresses:
- Routable on the Internet.
- Assigned by ISPs.

---
## Unusable / Reserved IPv4 Addresses
- Network address: x.y.z.0
- Broadcast address: x.y.z.255
- Loopback addresses: 127.x.y.z

---
## Network ID and Host ID
An IP address contains:
- Network ID – identifies the network.
- Host ID – identifies the specific device on that network.
Example: 210.54.101.0/24
- `/24` means 24 bits are network ID.
- Remaining 8 bits are host ID → 254 usable hosts.

---
## Classful vs Classless Addressing (CIDR)
### Classful (old method)
- Addresses divided into fixed classes (A, B, C).
### Classless (modern method)
- Uses suffixes such as `/24`, `/16`, etc.
- More flexible allocation → reduces wasted addresses.

---
## Subnet Masks
A subnet mask identifies the network portion of an IP address.
- Network bits = 1s
- Host bits = 0s
Example: /28 subnet mask
- Binary: 11111111.11111111.11111111.11110000
- Leaves 4 host bits → 2⁴ = 16 addresses
- Usable hosts: 14 (subtract network + broadcast).
Purpose:
- Identify whether a destination is on the same network using a bitwise AND.

---
## Subnetting

- Dividing a network into smaller networks.
- Improves security and reduces collisions.
- Smaller broadcast domains.

---
## Network Address Translation (NAT)
Devices with private IPs cannot access the Internet directly.
### What NAT Does:
- Translates private IPs to a public IP.
- Allows multiple devices to share one public IP.
### How It Works:
- Router keeps a table of source and destination socket addresses.
- Returns incoming data to the correct internal device.

---
## Port Forwarding
- Used to make internal servers accessible externally.
- Forwards incoming requests on a specific port to the correct device.
- Provides additional filtering/security.

---
## Dynamic Host Configuration Protocol (DHCP)
### Purpose:
- Automatically assigns IP addresses to devices.
- Leases addresses for a limited time.
### Advantages:
- Reduces number of static IPs needed.
- Allows devices to move between networks.
- Reuses unused addresses.
### Why static IPs are uncommon:
- Harder to manage.
- Less flexible.
- DHCP simplifies network administration.

---
## Exam-Style Practice Questions

1. Explain why IPv6 was introduced.
2. 192.168.1.0/24 – How many usable hosts are available?
3. Distinguish between public and private IP addresses.
4. Explain how NAT allows multiple devices to share one public IP.
5. Describe how DHCP assigns an IP address to a device.
