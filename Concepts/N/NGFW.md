#domain/1-0-Networking-Concepts

==**Next Generation Firewall**== 

Deep-packet inspection firewall that moves beyond simple port and IP address blocking. It integrates multiple security features into a single platform to inspect and block modern, sophisticated threats.

It does everything an ACL does (Layer 3/4 routing and blocking) AND everything an IPS does (Layer 7 payload inspection). Additionally, it is **application aware**. It doesn't just see "Port 443"; it sees "This is YouTube" or "This is Facebook" and can apply policies based on the application, not just the port.

Consolidation. An NGFW is a router, a firewall (ACLs), an IPS, and a web filter all in one box.



| Feature             | OSI Layer   | What it inspects?                  | Does it block? | Primary Function                    |
| :------------------ | :---------- | :--------------------------------- | :------------- | :---------------------------------- |
| **Dynamic [[ACL]]** | Layer 3 & 4 | IP addresses and Ports             | Yes            | Basic traffic filtering / Routing   |
| **[[IPS]]**         | Layer 3 - 7 | Packet payload (contents)          | Yes            | Block known attack signatures       |
| **NGFW**            | Layer 3 - 7 | IPs, Ports, Payloads, Applications | Yes            | All-in-one unified security gateway |

