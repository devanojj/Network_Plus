#domain/2-0-Network-Implementation

**Spanning tree protocol** 
Layer 2 protocol to prevent loops in a switched network
Calculates whenever a port changes 
802.1D


==States==
*Blocking -* No forwarding, no MAC learning, only listens to [[BPDU]]
*Listening -* No forwarding, no learning, participating in STP to identify roles 
*Learning -* Not forwarding yet, building MAC table
*Forwarding -* Normal operation
*Disabled -* Port is off 
