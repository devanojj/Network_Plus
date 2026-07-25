#domain/2-0-Network-Implementation

**==Open Shortest Path First==**
- Link State
- Cost (based on bandwidth)
- AD = 110
- Dijkstra's SPF algorithm
Area 0 this is the backbone where all other areas must connect to 

OSPF adjacency requirements: matching area ID, Hello/Dead timers, subnet/mask, authentication, MTU. Process IDs and router-IDs do NOT need to match.


==**Designated Router**==  
Reduce unnecessary routing traffic. Instead of every router exchanging LSAs (Link-State Advertisements) with every other router, all routers send updates to the DR.
- **DR:** Central router that manages LSA exchanges on the segment.
- **BDR (Backup Designated Router):** Standby router that takes over if the DR fails.
- **Election:** Based on the highest OSPF interface priority (default is 1). If priorities are equal, the highest Router ID wins. A priority of **0** means the router cannot become the DR or BDR.