#domain/1-0-Networking-Concepts

**Bootstrap protocol**
Older network protocol that automatically assigns an IP address to a client device when it boots up.

- **Primary Purpose:** Used by diskless workstations or network-booting computers to retrieve an IP address, subnet mask, default gateway, and the location of a boot file from a server.
    
- **How it works:** Operates over **UDP (ports 67 and 68)** via broad network broadcasts.
    
- **Why it matters today:** BOOTP is the direct predecessor to **DHCP**. Modern networks have almost entirely replaced BOOTP with DHCP because DHCP supports _dynamic_ IP allocation (leasing) rather than BOOTP's strictly _static_ IP mappings.