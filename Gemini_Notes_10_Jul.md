## DOMAIN 2.0: Network Implementation

### 1. VLANs (Virtual LANs)
*   **Default VLAN:** By default, all ports on a switch belong to VLAN 1. It cannot be deleted or renamed.
*   **Management VLAN:** A specific VLAN dedicated to managing the network devices (SSH, HTTPS, SNMP traffic). Best practice is to change this away from VLAN 1.
*   **VLAN Ranges:** Normal range is 1-1005 (stored in `vlan.dat`). Extended range is 1006-4094 (usually requires VTP transparent mode on older switches).
*   **802.1Q Tagging:** The standard protocol that adds a 4-byte VLAN tag to ethernet frames crossing a trunk link.

### 2. Spanning Tree Protocol (STP)
*   **Root Bridge Election:** Switches exchange BPDUs (Bridge Protocol Data Units) to elect a Root Bridge. The switch with the lowest Bridge ID (Priority + MAC address) wins. Default priority is 32768.
*   **Port Roles:**
    *   **Root Port:** Best path to the root bridge (one per non-root switch).
    *   **Designated Port:** Forwarding port for a specific network segment.
    *   **Blocked Port:** Port disabled by STP to prevent loops.
*   **Cost Calculation:** Based on link speed. (e.g., 10 Gbps = cost 2, 1 Gbps = cost 4, 100 Mbps = cost 19).
*   **BPDU Guard:** A security feature that disables an edge port (like a user's PC connection) if it unexpectedly receives a BPDU, preventing rogue switches from disrupting the STP topology.

### 3. EtherChannel / Link Aggregation
Combines multiple physical links into one logical link for increased bandwidth and redundancy.
*   **LACP (Link Aggregation Control Protocol):** IEEE 802.3ad standard. (Modes: Active, Passive).
*   **PAgP (Port Aggregation Protocol):** Cisco proprietary. (Modes: Desirable, Auto).

### 4. SD-WAN (Software-Defined WAN)
*   **Application-Aware:** Can route traffic dynamically based on the specific application (e.g., sending VoIP over a high-quality MPLS link, and bulk data over a cheaper broadband link).
*   **Zero-Touch Provisioning (ZTP):** New routers automatically download their configuration from a central controller when plugged into the internet, requiring no local manual setup.
*   **Transport Agnostic:** Can use any combination of underlying WAN links (MPLS, LTE, Broadband) seamlessly.

### 5. IoT Considerations & Network Segmentation
*   **IoT protocols:** Zigbee, Z-Wave (low power, short range wireless for smart home/industrial devices).
*   **Segmentation:** IoT devices are notoriously insecure. They must be placed on isolated VLANs (Guest or IoT networks), separate from trusted corporate data and systems. SCADA/ICS/OT networks also require extreme isolation from the regular IT network.

---

## DOMAIN 3.0: Network Operations

### 1. DRP (Disaster Recovery) & BCP (Business Continuity)
*   **BCP vs. DRP:** BCP focuses on keeping the business operational during a crisis. DRP is the technical IT subset of the BCP, focused on restoring IT systems.
*   **Metrics:**
    *   **RPO (Recovery Point Objective):** How much data loss is acceptable? (Dictates backup frequency).
    *   **RTO (Recovery Time Objective):** How much downtime is acceptable? (Dictates the recovery strategy).
    *   **MTBF (Mean Time Between Failures):** Expected lifetime of a product before it fails (reliability metric).
    *   **MTTR (Mean Time to Repair):** Average time taken to fix a failed system.
*   **Recovery Sites:**
    *   **Cold Site:** Empty building with power and cooling, but no hardware or data. Takes weeks to activate.
    *   **Warm Site:** Has hardware ready, but data must be restored from backups. Takes days to activate.
    *   **Hot Site:** Exact replica of the primary site with live, synchronized data. Takes minutes/hours to activate.
*   **Active-Active vs. Active-Passive:** Active-Active uses multiple active nodes distributing the load. Active-Passive has a standby node that only takes over if the primary fails.

### 2. Change Management
The formalized process for making modifications to the network.
*   **Process flow:** Submit Request -> Analyze Impact -> CAB Approval -> Implement -> Test -> Document.
*   **CAB (Change Advisory Board):** A group of stakeholders that reviews and approves requested changes based on risk and business impact.
*   **Rollback Procedure:** A documented plan on how to revert the change if the implementation fails or causes issues.
*   **Maintenance Windows:** Pre-approved scheduled times (usually off-hours) when disruptive changes are allowed.

### 3. IaC (Infrastructure as Code) & Automation
*   **Data Serialization Formats:** Ways to represent data in code. You must be able to recognize these:
    *   **JSON:** Uses `{ }`, `[ ]`, and `"key": "value"` pairs.
    *   **YAML:** Uses indentation and whitespace. Human-readable.
    *   **XML:** Uses `<tags>...</tags>` like HTML.
*   **REST API Concepts:** Uses standard HTTP methods for CRUD (Create, Read, Update, Delete) operations.
    *   GET (Read), POST (Create), PUT (Update), DELETE (Delete).

### 4. Load Balancing Methods
*   **Round-Robin:** Requests are distributed sequentially to each server in order.
*   **Least Connections:** Sends the next request to the server with the fewest active connections.
*   **Weighted:** Some servers get more traffic based on their assigned weight (e.g., because they have more RAM/CPU).
*   **IP Hash:** Uses the client's IP address to mathematically determine which server they go to (ensures session persistence/stickiness).

### 5. Physical Infrastructure
*   **Rack Units (U):** Standard measurement for rack height. 1U = 1.75 inches.
*   **Aisle Containment:** Data centers arrange racks so all front intakes face one aisle (Cold Aisle) and hot exhausts face another (Hot Aisle) for cooling efficiency.
*   **Patch Panels & Punch-Down Blocks:** 110 block (newer, used for Cat5/6 data networks), 66 block (older, used for analog voice/telephone).

---

## DOMAIN 4.0: Network Security

### 1. Firewalls & Threat Mitigation
*   **Stateful vs. Stateless:** Stateful firewalls remember the context of active connections (if traffic goes out, the return traffic is automatically allowed). Stateless (like an ACL) evaluates every single packet individually based solely on rules, regardless of existing connections.
*   **Implicit Deny:** The last, invisible rule on every firewall or ACL: "If traffic isn't explicitly permitted above, drop it."
*   **UTM (Unified Threat Management) / NGFW (Next-Gen Firewall):** Combines traditional firewalling with IPS, anti-malware, URL filtering, and application-layer inspection into one appliance.
*   **Geofencing:** Restricting access based on the geographic location (GPS or IP geolocation) of the user.

### 2. Network Hardening Techniques
*   **Change Default Passwords:** The easiest and most critical step.
*   **Disable Unused Ports:** Shut down switch ports that aren't actively being used.
*   **DHCP Snooping:** Prevents rogue DHCP servers from handing out incorrect IP addresses.
*   **Dynamic ARP Inspection (DAI):** Prevents ARP poisoning/spoofing attacks.
*   **Port Security (MAC Filtering/Sticky MAC):** Restricts a switch port to only allow specific MAC addresses. "Sticky" automatically learns the first MAC address plugged in and locks it to that port.
*   **802.1X (NAC):** Port-based Network Access Control. Requires users to authenticate (via RADIUS) before the switch port will forward any data.

### 3. VPNs and IPSec
*   **Client-to-Site vs. Site-to-Site:** Client-to-site is a remote worker securely connecting to the office. Site-to-site connects two entire office networks together over the internet (acting as a virtual leased line).
*   **Split Tunnel vs. Full Tunnel:** In a split tunnel, only corporate traffic goes through the VPN, while regular internet browsing goes out the local connection. Full tunnel sends ALL traffic (corporate + internet) through the VPN.
*   **IPSec Core Components:**
    *   **AH (Authentication Header):** Provides data integrity and origin authentication, but NO encryption.
    *   **ESP (Encapsulating Security Payload):** Provides encryption (confidentiality), integrity, and authentication.
    *   **IKE (Internet Key Exchange):** Sets up the secure connection (Phase 1 and Phase 2 negotiations) and handles key management.
*   **Tunnel vs. Transport Mode:** Tunnel mode encrypts the entire original IP packet (payload + header) and adds a new IP header (used for site-to-site). Transport mode encrypts only the payload, keeping the original IP header visible (used for host-to-host).

### 4. Zero Trust Architecture (ZTA)
*   "Never trust, always verify." Assumes the internal network is just as hostile as the internet.
*   Requires policy-based authentication and strict authorization for every single request.
*   Relies heavily on **Least Privilege Access** (users get only the exact permissions needed) and **Micro-segmentation** (putting tiny firewalls/controls around individual workloads rather than just the network perimeter).

### 5. RADIUS vs. TACACS+
*   **RADIUS:** UDP protocol. Encrypts ONLY the password. Combines Authentication and Authorization. Standard across all vendors. Often used for network access (802.1X, Wi-Fi).
*   **TACACS+:** TCP protocol (reliable). Encrypts the ENTIRE payload. Separates Authentication, Authorization, and Accounting. Cisco proprietary (mostly). Often used for device administration (SSH access to routers/switches).

### 6. Incident Response & Social Engineering
*   **First Responder:** The first person to report or arrive at the scene of an incident. Their priority is securing the scene and preventing further damage, NOT necessarily fixing it immediately.
*   **Chain of Custody:** A chronological paper trail detailing who handled digital evidence, when, and where, to ensure it holds up in court.
*   **Captive Portal:** A web page that intercepts a user's web browsing and forces them to agree to terms, pay, or authenticate before accessing the guest Wi-Fi network.

---

## DOMAIN 5.0: Network Troubleshooting

### 1. Wireless Troubleshooting Scenarios
*   **Interference:** Usually caused by physical obstacles or other devices on the same frequency (microwaves, cordless phones, Bluetooth on 2.4GHz).
*   **Channel Overlap:** Occurs when adjacent APs use overlapping frequencies (e.g., Channels 1, 2, 3). In 2.4GHz, only use non-overlapping channels: **1, 6, and 11**.
*   **Signal Degradation:** Caused by distance or attenuation (passing through dense walls/metal). Fix: Add APs, adjust antenna types (omnidirectional vs directional).
*   **Roaming Misconfiguration:** When a client stays connected to a distant AP with a weak signal instead of seamlessly roaming to a closer, stronger AP. Can be fixed by adjusting TX power or ensuring consistent SSIDs and security settings.
*   **Client Disassociation:** Client drops off the network. Can be caused by mismatched security types (WPA2 vs WPA3) or incorrect PSK.

### 2. Network Performance Troubleshooting
*   **Latency vs. Jitter:** Latency is the delay in packets reaching their destination. Jitter is the *variation* in that delay. Jitter is a killer for real-time traffic like VoIP and video.
*   **Interface Errors:**
    *   **CRC Errors (Cyclic Redundancy Check):** Packets arrived corrupted. Usually indicates a bad physical cable, faulty NIC, or duplex mismatch.
    *   **Runts:** Packets smaller than the minimum 64 bytes. Often caused by collisions.
    *   **Giants:** Packets larger than the maximum 1518 bytes (unless Jumbo Frames are configured).
    *   **Drops:** The router/switch interface buffer is full due to congestion, so it simply discards incoming packets.
*   **Bottlenecking:** The entire network slows down because one single link or device (the bottleneck) cannot handle the throughput capacity.

### 3. Physical & Hardware Troubleshooting
*   **PoE Power Budget Exceeded:** A switch can only provide so much total wattage. If you plug in too many high-draw PoE devices (like PTZ cameras or high-end APs), some devices won't power on.
*   **Transceiver Mismatch:** Using an SFP module meant for Single-Mode Fiber (SMF) on a Multi-Mode Fiber (MMF) cable, or mismatched wavelengths.
*   **TX/RX Transposed:** On fiber optic cables, the transmit (TX) strand on one end must connect to the receive (RX) strand on the other. If reversed, the link will not come up.
