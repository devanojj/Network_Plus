
### 2. Testing Disaster Recovery
*   **Tabletop Exercise:** A low-impact, discussion-based test. The IT team sits in a conference room, someone reads a disaster scenario, and everyone talks through their roles and the recovery plan. No actual systems are touched.
*   **Validation Test:** Actually failing over to the backup site or restoring servers from backup to prove the technical procedures work.

### 3. Connection Methods
*   **In-Band Management:** Managing a router or switch over the standard production network (e.g., SSHing into a switch via the office Wi-Fi). If the network goes down, you lose management access.
*   **Out-of-Band (OOB) Management:** A dedicated, separate network just for managing devices. Often uses a dedicated "management port" on the switch, connected to a totally separate management switch. If the main network crashes, you can still reach the equipment.
*   **Console Connection:** The ultimate OOB method. Taking a laptop and physically plugging a serial console cable directly into the device.

---

## DOMAIN 4.0: Network Security (Final Gaps)

### 1. Compliance & Regulations
*   **PCI DSS (Payment Card Industry Data Security Standard):** Strict rules for networks that process, store, or transmit credit card data.
*   **GDPR (General Data Protection Regulation):** Massive EU privacy law regarding the protection of personal data of EU citizens.
*   **Data Locality / Sovereignty:** Legal requirements that dictate data must physically remain stored on servers within the borders of a specific country.

### 2. Deception Technologies
*   **Honeypot:** A single fake system (e.g., a fake file server) deliberately left vulnerable to attract attackers and study their methods or trigger early warning alarms.
*   **Honeynet:** An entire fake network of honeypots designed to look like a complete corporate infrastructure.

### 3. Physical Social Engineering
*   **Tailgating:** Following someone closely through a badge-access door without swiping your own badge.
*   **Shoulder Surfing:** Literally looking over someone's shoulder to steal passwords or sensitive info on their screen.
*   **Dumpster Diving:** Searching through physical trash to find IP addresses, passwords written on sticky notes, or network diagrams.

---

## DOMAIN 5.0: Network Troubleshooting (Final Gaps)

### 1. Hardware Tools
*   **Toner (Tone Generator & Probe):** Used to trace a specific wire through a chaotic bundle in a server room. One piece puts an audio tone on the wire, the wand makes a noise when it gets near that specific wire.
*   **Cable Tester:** Plugs into both ends of a copper cable to verify continuity, correct pinouts (no crossed wires), and that all 8 pins are connected.
*   **Visual Fault Locator (VFL):** A very bright laser you shine down a fiber optic cable. If the cable is broken or bent too sharply, the red light will visibly leak out of the cable jacket.
*   **Network Tap:** A physical device inserted inline on a network link that copies all traffic to a monitoring port. Better than Port Mirroring (SPAN) because it cannot drop packets if the switch CPU gets too busy.

### 2. Software Tools & Commands
*   **`nslookup` vs `dig`:** Both test DNS resolution. `nslookup` is older and works on Windows/Linux. `dig` is vastly superior, provides much more detail, and is the standard on Linux/macOS.
*   **`netstat`:** Shows all active TCP/UDP connections on a computer, and which application/PID is using which port. Great for finding out if malware is calling out.
*   **`arp` (command):** `arp -a` shows your local computer's ARP cache (IP-to-MAC address mappings). Useful for detecting ARP poisoning.
*   **`ipconfig` / `ifconfig` / `ip`:** `ipconfig` (Windows). `ifconfig` (older Linux/macOS). `ip addr` or `ip a` (modern Linux replacement for ifconfig).
