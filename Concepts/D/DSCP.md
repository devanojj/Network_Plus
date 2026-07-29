#domain/1-0-Networking-Concepts
 **==Differentiated Services Code Point==**
 
- 6-bit field inside the IP header
- Prioritise traffic for [[QoS]].

How the network knows [[VoIP]] packet is more urgent than a file download.


#### Key DSCP Classes to Know

| DSCP Class                    | Value                   | Traffic Type                                                                       | Queuing Method                                      |
| ----------------------------- | ----------------------- | ---------------------------------------------------------------------------------- | --------------------------------------------------- |
| **EF** (Expedited Forwarding) | 46                      | Voice (VoIP) — real-time, most delay-sensitive                                     | **Priority Queueing (PQ)** — strict, serviced first |
| **AF** (Assured Forwarding)   | AF11–AF43 (e.g. AF41)   | Video, business-critical data — needs guaranteed bandwidth but not strict priority | **Weighted Fair Queueing (WFQ)**                    |
| **CS** (Class Selector)       | CS0–CS7 (CS0 = default) | Backwards-compatible with old IP Precedence; CS0 = Best Effort                     | FIFO (no priority)                                  |
| **BE** (Best Effort)          | 0                       | Default — no special treatment (web, email, file downloads)                        | FIFO / RED                                          |