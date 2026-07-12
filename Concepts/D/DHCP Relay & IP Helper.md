#domain/3-0-Network-Operations


- **The Problem**: [[DHCP]] Discover and Request packets are sent as local broadcasts (`255.255.255.255`). Routers block broadcasts by default. If a DHCP server is on a different subnet/VLAN than the client, the client cannot obtain an IP.
- **The Solution**: A **DHCP Relay Agent** (or **IP Helper** on Cisco switches/routers).
  - Configure the router interface facing the client with the IP helper command: `ip helper-address <DHCP_Server_IP>`.
  - The router intercepts the client's local broadcast DHCP Discover, wraps it in a **unicast IP packet** (changing the destination to the DHCP server's IP), and routes it to the server.
  - The server replies back to the router via unicast, and the router forwards the response to the client.