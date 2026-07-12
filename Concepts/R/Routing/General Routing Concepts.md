| **Term**                         | Definition                                                                  |
| -------------------------------- | --------------------------------------------------------------------------- |
| **Routing Table**                | Database stored in a router containing paths to destination networks        |
| **Administrative Distance (AD)** | Trustworthiness of a routing source (lower = more preferred)                |
| **Metric**                       | Cost calculation used to determine the best path when multiple routes exist |
| **Convergence**                  | Time it takes for all routers to agree on network topology after a change   |
| **Default Route**                | Route used when no specific route exists (0.0.0.0/0)                        |
| **Static Route**                 | Manually configured route by administrator                                  |
| **Dynamic Route**                | Automatically learned through routing protocols                             |

### ==Route Selection Decision Hierarchy==
When a router receives a packet, it determines the best path using the following order of operations:
1. **Longest Prefix Match (LPM):** The router always selects the route with the most specific subnet mask (longest prefix length) matching the destination IP. (e.g., `/28` is preferred over `/24`).
2. **Administrative Distance (AD):** If multiple routes to the exact same destination have the same prefix length, the router compares the AD. The routing source with the lowest AD is trusted and installed in the routing table.
3. **Metric:** If multiple paths are learned from the same routing protocol (identical prefix length and AD), the router compares the metric values. The lowest metric wins. (If they are equal, load balancing may occur).

### ==Default Administrative Distance (AD) Table==

| Route Source                | Default AD | Trust Level    | Notes                                                  |
| :-------------------------- | :--------- | :------------- | :----------------------------------------------------- |
| **Directly Connected**      | 0          | Most Trusted   | The interface is physically up and has an IP address.  |
| **Static Route**            | 1          | Highly Trusted | Manually configured by an administrator.               |
| **External [[BGP]] (eBGP)** | 20         | Very Trusted   | Routing between different Autonomous Systems (AS).     |
| **[[EIGRP]] (Internal)**    | 90         | Trusted        | Cisco proprietary (or open standard hybrid).           |
| **[[OSPF]]**                | 110        | Medium         | Link-state routing protocol.                           |
| **[[IS-IS]]**               | 115        | Medium         | Link-state routing protocol (less common on Network+). |
| **[[RIP]]**                 | 120        | Low            | Distance-vector protocol. Max 15 hops.                 |
| **External [[EIGRP]]**      | 170        | Very Low       | Routes redistributed into EIGRP.                       |
| **Internal [[BGP]] (iBGP)** | 200        | Very Low       | BGP routing within the same Autonomous System.         |
| **Unreachable**             | 255        | Untrusted      | The router will never install this route.              |


> [!WARNING]
> **Common Exam Trap:** Do not confuse routing table lookups with Access Control Lists (ACLs). [[ACL]]s are evaluated top-down (first match wins). Routing tables are evaluated using Longest Prefix Match (most specific match wins), not top-down.


### ==Asymmetric Routing==
*   **What it is:** Outbound traffic from a source to a destination takes path A, but the return traffic takes path B.
*   **Why it breaks networks:** It causes failures on **stateful security devices** (like firewalls and NAT devices). Since these devices monitor connection states, they expect to see both the outbound request and the inbound response. If they only see one side, they assume it is an attack and drop the traffic.
*   **How to troubleshoot:** Run `traceroute` (or `tracert` on Windows) from both directions (source-to-destination and destination-to-source) to verify path symmetry.


### ==Key Troubleshooting Tools==
*   `route print` (Windows) / `netstat -r` (All platforms): Displays the local host's routing table.
*   `show ip route` (Cisco IOS): Displays the router's routing table.


## Metric 
OSPF - Cost (Bandwidth)
RIP - Hop count
BGP - Various path attributes



