#domain/3-0-Network-Operations

Inspects DHCP messages and allows (OFFER, ACK) only from designated ports.

All other ports are untrusted and messages are dropped. Stops rouge DHCP servers assigning incorrect IP configurations to clients. 

This also feeds into Dynamic [[ARP]] Inspection ([[DAI]]) for ARP spoofing prevention 

Only trusted ports (connected to legitimate DHCP servers) are allowed to send DHCP server messages. It builds a database of legitimate IP-to-MAC bindings.

Operates on the data link layer
