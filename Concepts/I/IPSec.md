#domain/1-0-Networking-Concepts
IPsec tunnel mode encapsulates the entire original IP packet (including original IP header) inside a new IP packet with a new outer header.

IPsec transport mode only protects the payload between the original two endpoints, leaving the original IP header visible — used for host-to-host VPNs (less common).

3 main security protocols 
[[ESP]] 
[[AH]]
[[IKE]] / [[ISAKMP]]