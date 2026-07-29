#domain/1-0-Networking-Concepts
==**Neighbour Discovery Protocol (NDP)**==

Replaces [[ARP]] in [[IPv6]]. Uses ICMPv6 messages for router discovery, address resolution, and autoconfiguration.

### 1. Router Discovery
* **Router Solicitation (RS)**: Sent by a host looking for local routers.
  * *Destination:* `ff02::2` (**All-Routers** multicast)
* **Router Advertisement (RA)** *(ICMPv6 Type 134)*: Sent by routers to convey network prefix info and default gateway details.
  * *Destination:* `ff02::1` (**All-Nodes** multicast) or unicast to requesting host.

### 2. Address Resolution (Replaces ARP)
* **Neighbor Solicitation (NS)**: Requests MAC address for a target IPv6 address.
  * *Destination:* Solicited-node multicast address.
* **Neighbor Advertisement (NA)**: Responds with MAC address info.
  * *Destination:* Unicast to requesting host.

### Key Multicast Destination Addresses
| Address | Scope | Description |
|---|---|---|
| **`ff02::1`** | All-Nodes | Reaches **all IPv6 devices** on the local link (used by RAs) |
| **`ff02::2`** | All-Routers | Reaches **all IPv6 routers** on the local link (used by RSs) |


| Message                          | Purpose                                        | Used When                                                                 |
| -------------------------------- | ---------------------------------------------- | ------------------------------------------------------------------------- |
| Router Solicitation (RS)     | A host asks routers for network information    | A device joins a network and needs an IPv6 address/prefix                 |
| Router Advertisement (RA)    | A router provides network information          | Router announces IPv6 prefix, default gateway, autoconfiguration settings |
| Neighbour Solicitation (NS)  | A device asks "Who owns this IPv6 address?"    | Finding MAC addresses, duplicate address detection, reachability checks   |
| Neighbour Advertisement (NA) | A device replies with its IPv6/MAC information | Responding to NS requests                                                 |
