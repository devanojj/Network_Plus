**Address Resolution Protocol**
Layer 2
Responsible for MAC addressing


| ARP Type               | What it does                                                                                                                                              |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ARP Cache**          | A temporary table in RAM that stores IP-to-MAC mappings to improve performance.                                                                           |
| **Gratuitous ARP**     | An ARP message sent by a device to announce its own IP/MAC mapping to the network, often used to detect IP conflicts or update switches after a failover. |
| **Reverse ARP (RARP)** | Used by diskless workstations to request their own IP address based on their known MAC address (mostly legacy).                                           |
| **Proxy ARP**          | When a router answers an ARP request for an IP address that is not on the local network, acting as a gateway for the requester.                           |
