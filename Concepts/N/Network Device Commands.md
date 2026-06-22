~~**MAC address table**~~ 
~~`show mac-address-table` → maps MAC addresses to switch ports (L2 table) - Switch-only command; used to verify port associations or track a device -~~ 
~~*Distractor trap:* `arp -a` is a host OS command (Windows/Linux), NOT a Cisco switch command~~ 

~~**ARP table**~~ 
~~`show arp` → maps IP addresses to MAC addresses - Used on routers and L3 switches. Different from `show mac-address-table`~~ 
~~*Key distinction:* MAC table = port-based (L2); ARP table = IP-based (L3)~~ 

~~**Routing table** - `show ip route` → displays routing table with networks and next-hop addresses~~ 

~~**Interface statistics**~~ 
~~`show interface` → interface status (up/down), IP, bandwidth, errors, packet loss, collisions - Used for diagnosing connectivity issues or high error rates~~ 

~~**Running configuration**~~ 
~~`show running-config` → full active config: IPs, routing protocols, VLANs, ACLs - Correct Cisco IOS syntax;~~

~~**VLAN information**~~ 
~~`show vlan` → VLAN IDs, names, and port-to-VLAN assignments - Switch-only; used to verify VLAN membership and troubleshoot VLAN issues~~ 

~~**PoE status**~~ 
~~`show power` → PoE budget available vs. drawn, per-port wattage - Used on PoE-capable switches to diagnose power delivery issues      not needed Cisco commadns-~~  




**Connectivity testing**

- `ping` — ICMP reachability test
- `traceroute` (Linux/macOS) / `tracert` (Windows) — hop-by-hop path
- `pathping` (Windows) / `mtr` (Linux) — combines ping + traceroute, shows packet loss per hop over time
- `curl` — test HTTP/HTTPS/API reachability

**Host network config**

- `ipconfig` (Windows) / `ifconfig` or `ip` (Linux/macOS) — view/configure interface IPs
    - switches: `/all`, `/release`, `/renew`, `/flushdns`
- `hostname` — display local machine's network name
- `arp` (`arp -a`) — view local ARP cache (IP-to-MAC)

**DNS tools**

- `nslookup` — query DNS records (interactive or one-off)
- `dig` (Linux/macOS) — more detailed DNS query tool

**Routing**

- `route` — view/modify local routing table

**Port/connection state**

- `netstat` / `ss` (Linux) — active connections, listening ports

**Packet capture/scanning**

- `tcpdump` — packet capture
- `nmap` — port scanning, host discovery

**Remote access**

- `telnet` — insecure remote terminal (port 23); also used to test if a TCP port is open
- `ssh` — secure remote terminal (port 22)