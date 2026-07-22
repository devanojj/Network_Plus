#domain/2-0-Network-Implementation
==**Destination Network Address Translation**==

Let internet users reach a server sitting in the [[DMZ]]

Server has a private IP and the internet user has a public IP

The DNAT rewrites the destination address of the packets, used for inbound traffic
This is what [[Port forward]]ing means on consumer routers. 

The [[ACL]] also needs to be enabled for this to happen

[[SNAT]] does the opposite of this 
