#domain/3-0-Network-Operations

Inspects DHCP messages and allows (OFFER, ACK) only from designated ports.

All other ports are untrusted and messages are dropped. Stops rouge DHCP servers assigning incorrect IP configurations to clients. 

This also feeds into Dynamic [[ARP]] Inspection ([[DAI]]) for ARP spoofing prevention 
Operates on the data link layer - Layer 2
