#domain/1-0-Networking-Concepts

**==NIC Teaming / Port Aggregation==** 
Grouping multiple [[NIC]]s on a single server into one logical interface, another word for [[LACP]]


==**Multipathing**==
Creating multiple physical paths between server and its storage device 
Usually in [[SAN]] environment 

[[iSCSI]]


**==Active/Active==**
Multiple load balancers or servers handle traffic simultaneously. Provides maximum throughput and distributes the workload evenly.


**==Active/Passive==**
One primary node handles all traffic while the backup sits idle. If the primary fails, the passive node immediately takes over (failover).


==**Underlay**== 
The physical infrastructure (routers, switches, cables) that actually forwards and routes the packets.


==**Overlay**== 
A virtual, logical network built on top of the underlay using tunneling protocols (like VXLAN or SD-WAN tunnels). The overlay operates independently of the physical topology.