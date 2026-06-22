### Routing Loops (Layer 3) vs. Switching Loops (Layer 2)

*   **Layer 3 Routing Loops:**
    *   *Cause:* Misconfigured static routes or slow routing protocol convergence.
    *   *Handling:* Packets have a **Time to Live (TTL)** field in the IP header. Every router decrements the TTL by 1. When the TTL reaches 0, the packet is discarded, and the router sends an ICMP "Time Exceeded" message back to the sender.
    *   *Protocol mitigations:* [[Split Horizon]], Route Poisoning, and Holddown Timers.


*   **Layer 2 Switching Loops:**
    *   *Cause:* Redundant links between switches without Spanning Tree.
    *   *Handling:* Ethernet frames do **not** have a TTL field. They will loop forever, causing a broadcast storm that crashes the network.
    *   *Mitigation:* **Spanning Tree Protocol (STP)**.