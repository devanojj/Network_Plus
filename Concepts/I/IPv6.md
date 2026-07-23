#domain/1-0-Networking-Concepts

**==Compress IPv6==** 
Remove any leading zeros then make compress only one group of zeros to ::
`2001:0db8:0000:0000:0000:ff00:0042:0001` 
`2001:db8::ff00:42:1`

**==[[Tunneling]] 6to4==** 
IPv6 packets within a IPv4 header

**==Dual-stack IP==** 
Both IPv4 and IPv6 protocols on network devices to facilitate seamless migration from IPv4 to IPv6.

**==[[NAT64]]==**
IPv6-only devices to communicate with IPv4-only servers

Any IPv6 address that starts with `2` or `3` (i.e., `2000::/3`) is a Global Unicast Address (GUA), meaning it is globally routable on the Internet.

**::1 loop back address**
**FE80::/10 local link address** 
**FE00::/8 multicast
FC00::/7 unique local
2000::/3 global unicast

IPv6 has no broadcast address

An unique local address (ULA) is the IPv6 equivalent of an IPv4 private IP address.

IPv6 addresses are 128 bits total. Prefix length defines how many bits are the network portion; the rest is the host/interface portion.

|Prefix|Use|Notes|
|---|---|---|
|**/64**|Standard local subnet|Remaining 64 bits = interface ID. Nearly every LAN subnet uses this.|
|**/48**|Typical ISP allocation to a site|Leaves 16 bits for the site to create its own /64 subnets (2^16 possible subnets).|
|**/128**|Single specific device|No network portion at all — one host only. Example: loopback `::1/128`.|

**Mental model:** ISP gives you a /48 (the whole building) → you carve out /64s (individual subnets/apartments) → /128 is one exact device inside.

