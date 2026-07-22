#domain/3-0-Network-Operations

**==[[DHCP]] Starvation==**
An attacker floods a DHCP server with fake DHCP Discover packets using spoofed MAC addresses, exhausting all available IP addresses in the scope. Legitimate clients are then unable to obtain an IP.

**==Mitigation==**
Port Security on the switch (limiting the number of unique MAC addresses allowed on a single switchport).



**==Rogue DHCP Server==** 
An unauthorised DHCP server is connected to the network and hands out incorrect IP configurations (e.g., listing the attacker's machine as the default gateway to perform a Man-in-the-Middle attack).

==**Mitigation**== 
DHCP Snooping on the switch. It designates switchports as Trusted (ports connected to legitimate DHCP servers/relays) or Untrusted (access ports connected to regular clients). The switch blocks all DHCP Offer and ACK packets arriving on untrusted ports.
