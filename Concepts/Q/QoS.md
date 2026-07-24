#domain/5-0-Network-Troubleshooting

## **What is Quality of Service (QoS)?**

- A suite of technologies that allows network administrators to prioritise critical traffic (e.g., real-time voice and video) over less time-sensitive data (e.g., web browsing or email) on a congested network link.
- QoS manages bandwidth, delay (latency), packet loss, and variation in delay (jitter).


| Feature        | **Traffic Shaping**                                                                      | **Traffic Policing**                                                                     |
| :------------- | :--------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------- |
| **Action**     | **Buffers** excess packets in memory and sends them later, smoothing out traffic bursts. | **Drops** or re-marks (downgrades) excess packets immediately.                           |
| **Profile**    | Produces a smooth, steady output rate.                                                   | Produces a jagged, hard-capped rate.                                                     |
| **TCP Impact** | Minimizes packet drops, reducing TCP retransmissions.                                    | Forces packet drops, leading to TCP retransmissions and possible global synchronization. |
| **Use Case**   | Best for outbound (egress) WAN interfaces where smoothing traffic is desired.            | Best for inbound (ingress) interfaces (e.g., ISPs enforcing a bandwidth cap).            |
| **Drawback**   | Introduces delay/latency due to buffering; requires memory resources.                    | Causes packet loss, which degrades real-time applications (voice/video).                 |


## **Real-Time Traffic Requirements (VoIP / Video)**

Real-time applications are highly sensitive to network performance. To maintain acceptable quality, networks must meet these thresholds:

- **One-way Latency**: $\le 150 \text{ ms}$ (the time it takes for a packet to travel from source to destination).
- **Jitter** (Variation in packet arrival times): $\le 30 \text{ ms}$.
- **Packet Loss**: $\le 1\%$.
