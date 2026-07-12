#domain/3-0-Network-Operations

**Dynamic Host Configuration Protocol** 

Automates the assignment of IP addresses, subnet masks, default gateways, DNS servers, and other network parameters to hosts.

Operates over **UDP**:
Server listens on **UDP Port 67**.
Client listens on **UDP Port 68**.


*DHCP can automatically provide:*
- IP addres
- Subnet mask
- Default gateway (Option 3)
- DNS server addresses (Option 6)
- Domain name (Option 15)

*Additional options may be used for specialised devices:*
- Option 66 → TFTP server location
- Option 67 → Boot file name for PXE/network boot