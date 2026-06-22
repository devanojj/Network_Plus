**Maximum transmission unit** 

Maximum amount of data that can be transmitted over a network without fragmentation
Default is 1500 bytes

**Fragmentation:** If a packet exceeds the MTU of a network link, routers along the path will break it up into smaller "sub-packets" so it can successfully transmit. These are reassembled at the final destination.


MTU limits aren't just between the sender and receiver; packets must conform to the MTU of _every_ router and switch along the communication pathway.

**The DF Flag:** An application or protocol can set a "Don't Fragment" flag inside the IP header, strictly forbidding the network from breaking the packet apart


**The ICMP Response:** If a router receives a packet that is larger than its MTU interface _and_ the DF flag is set, the router will drop the packet. It then sends an **ICMP (Internet Control Message Protocol)** message back to the sender stating the packet was too large and couldn't be fragmented

**IPv4:** Supports network-level fragmentation by routers along the path.

**IPv6:** **Does NOT permit fragmentation by routers.** If an IPv6 packet is too large for a link, it is dropped and an ICMPv6 "Packet Too Big" message is sent back to the sender so the sender can adjust the size. _(This is a highly testable concept!)_