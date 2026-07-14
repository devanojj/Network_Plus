#domain/1-0-Networking-Concepts

![[Pasted image 20260609134715.png|477]]


![[Pasted image 20260609134754.png|460]]


**Mesh**  every node has a direct connection to every other node; highest redundancy 
- **Multipathing** — multiple redundant paths exist between any two nodes
- **Load balancing** — traffic can be split/distributed across those multiple paths
- **More difficult routing**

**Star** all nodes connect to a central hub/switch; most common LAN topology 

**Hub-and-spoke**  WAN/VPN variant of star; single spoke failure does NOT bring down the network 

**Point-to-point**  direct link between two nodes; WAN links, VPN tunnels, remote access connections,  Wi-Fi is NOT point-to-point (point-to-multipoint) 

**Hybrid** — combines two or more standard topologies 

**Spine-and-leaf** — two-layer full-mesh used in data centres; spine tier is full mesh, leaf tier connects to all spines. (East-West, server to server)
Layer 3 used in spine and WAN


**Collapsed core** — merges core + distribution into one layer; used in small-medium networks; reduces complexity and cost


**North-south** between external networks (internet) and internal resources (servers/data centres) **East-west** — between devices within the same data centre or network 


![[Pasted image 20260609135348.png|475]]


**3 Tier Network Design** 
![[Pasted image 20260610134039.png|402]]


[[Core switch]]s connect to each other 
[[Distribution switch]]
[[Access switch]]


