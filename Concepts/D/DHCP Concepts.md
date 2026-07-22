#domain/3-0-Network-Operations

**==Scope==** 
The range of consecutive IP addresses that the DHCP server is allowed to distribute to clients on a specific subnet (e.g., `192.168.1.100` to `192.168.1.200`).


**==Exclusion Range==** 
Specific IP addresses within a scope that the DHCP server is instructed **not** to lease. These are reserved for statically configured devices like routers, switches, servers, and printers (e.g., exclude `192.168.1.1` to `192.168.1.20`).


**==Reservation (IP-MAC Binding)==**
A static mapping of a specific IP address to a device's unique MAC address. The client still requests its IP dynamically via DHCP, but the server guarantees it will *always* receive the exact same IP address. (Useful for network printers, NAS units, and application servers).


**==Lease Time==** 
The length of time a client is permitted to use an assigned IP address before it must renew it. Shorter lease times are preferred in high-turnover environments (e.g., guest Wi-Fi), whereas longer leases are suited for stable desktop environments.