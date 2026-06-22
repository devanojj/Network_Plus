[[Ping]]

*[[Tracert]]: Windows* | *Traceroute: Linux / macOS*
- It is used to examine hops, sends a packet along the path
- Use when ping partially works

*Nslookup \ dig*
- Checks for DNS name resolution & server responses 
- It is used when IP works but hostname doesn't (Layer 7)

*[[Netstat]] (Windows, Mac, Linux) | ss (Linux)*
- Checks for active connections & ports
- Listening services (Layer 4)

*Tcpdump | Wireshark*
- Checks packet contents, inspect traffic
- Sudo tcpdump

*[[Nmap]]*
- Check open ports, running services, for quick scans

*Route: Linux / macOS* | *Route print: Windows*
- Checks for routing table, network paths, can get default gateway

*Show mac-address-table* | *show interface*
- Commands for switch 

*Curl / wget*
- Application level 7, used for API testing 
- Curl testing endpoint 
- While wget can retrieve files
