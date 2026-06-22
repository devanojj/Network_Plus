## **What is Quality of Service (QoS)?**

- A suite of technologies that allows network administrators to prioritize critical traffic (e.g., real-time voice and video) over less time-sensitive data (e.g., web browsing or email) on a congested network link.
- QoS manages bandwidth, delay (latency), packet loss, and variation in delay (jitter).

---

## ~~**Classification and Marking**~~

~~To apply QoS, traffic must first be identified and tagged:~~
1. ~~**Classification**: The process of identifying and categorizing traffic based on specific criteria (e.g., source/destination IP, port number, protocol, or application type).~~
2. ~~**Marking**: The process of writing a QoS value into the packet or frame header. Marking packets allows subsequent network devices (routers/switches) to quickly identify the traffic class and apply the appropriate policy without performing complex re-classification.~~

### ~~**Layer 2 vs. Layer 3 Marking**~~

#### ~~**Class of Service (CoS)**~~
- ~~**Layer**: Layer 2 (Ethernet).~~
- ~~**Field**: Uses a **3-bit** Priority Code Point (PCP) field within the [[802.11|802.1Q]] VLAN header tag.~~
- ~~**Range**: $2^3 = 8$ priority values (`0` to `7`).~~
  - ~~`0` is Best Effort (default).~~
  - ~~`5` is typically reserved for Voice (VoIP).~~
  - ~~`7` is reserved for network control traffic.~~
- ~~**Limitation**: CoS values are lost when a frame traverses a router (Layer 3 boundary).~~

#### ~~**Differentiated Services Code Point (DSCP)**~~
- ~~**Layer**: Layer 3 (IP).~~
- ~~**Field**: Uses a **6-bit** field in the IPv4 Type of Service (ToS) byte or the IPv6 Traffic Class byte.~~
- ~~**Range**: $2^6 = 64$ priority values (`0` to `63`).~~
- ~~**Common Standards**:~~
  - ~~**Default (DF / CS0)**: `0` (Best Effort).~~
  - ~~**Expedited Forwarding (EF)**: `46` (DSCP value). Used for low-latency, low-jitter traffic. **Reserved for Voice payload**.~~
  - ~~**Assured Forwarding (AF)**: Divided into 4 classes with 3 drop-precedence levels each (e.g., `AF41` has lower drop probability than `AF43`).~~
- ~~**Advantage**: DSCP markings survive routing boundaries and persist end-to-end.~~

~~---~~

## ~~**Traffic Conditioning: Shaping vs. Policing**~~

~~When traffic exceeds the configured bandwidth limit, network devices enforce controls using either shaping or policing:~~

| Feature | **Traffic Shaping** | **Traffic Policing** |
| :--- | :--- | :--- |
| **Action** | **Buffers** excess packets in memory and sends them later, smoothing out traffic bursts. | **Drops** or re-marks (downgrades) excess packets immediately. |
| **Profile** | Produces a smooth, steady output rate. | Produces a jagged, hard-capped rate. |
| **TCP Impact** | Minimizes packet drops, reducing TCP retransmissions. | Forces packet drops, leading to TCP retransmissions and possible global synchronization. |
| **Use Case** | Best for outbound (egress) WAN interfaces where smoothing traffic is desired. | Best for inbound (ingress) interfaces (e.g., ISPs enforcing a bandwidth cap). |
| **Drawback** | Introduces delay/latency due to buffering; requires memory resources. | Causes packet loss, which degrades real-time applications (voice/video). |

~~---~~

## ~~**Congestion Management (Queuing)**~~

~~When a network interface receives packets faster than it can transmit them, they enter a queue. Different queuing algorithms manage how packets are prioritized:~~

- ~~**FIFO (First In, First Out)**: Default queuing. Packets are processed and sent in the exact order they arrive. No prioritization is performed, meaning bulk data can easily starve real-time traffic.~~
- ~~**Weighted Fair Queuing (WFQ)**: Dynamically splits bandwidth among conversations (flows) based on weight. Prevents high-bandwidth flows from completely starving low-bandwidth, interactive traffic.~~
- ~~**Class-Based Weighted Fair Queuing (CBWFQ)**: Allows administrators to define specific traffic classes (e.g., transactional, business-critical) and guarantee a minimum bandwidth percentage for each class.~~
- ~~**Low Latency Queuing (LLQ)**: Adds a **Strict Priority Queue (PQ)** to CBWFQ. Real-time traffic (like VoIP voice packets) placed in the priority queue is *always* serviced first, before any other queue. To prevent the priority queue from starving other queues, it is hard-policed to a maximum bandwidth limit.~~

~~---~~
*All Cisco*


## **Real-Time Traffic Requirements (VoIP / Video)**

Real-time applications are highly sensitive to network performance. To maintain acceptable quality, networks must meet these thresholds:

- **One-way Latency**: $\le 150 \text{ ms}$ (the time it takes for a packet to travel from source to destination).
- **Jitter** (Variation in packet arrival times): $\le 30 \text{ ms}$.
- **Packet Loss**: $\le 1\%$.
