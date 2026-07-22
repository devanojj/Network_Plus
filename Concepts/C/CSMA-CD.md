#domain/1-0-Networking-Concepts

- **Carrier Sensing** — a device listens to the network before transmitting to check if the line is free
- **Multiple Access** — multiple devices share the same communication medium
- **Collision Detection** — if two devices transmit simultaneously and a collision occurs, they detect it, stop, wait a random back-off time, and retransmit
- Part of Ethernet [[802.3]] (Wired)


It detects collisions _after_ they happen. Devices transmit data if the line seems clear. If two devices transmit at the exact same time and a collision occurs, they **detect it**, immediately stop transmitting, wait a random back-off time, and then try to retransmit.

CSMA/CD is a legacy concept primarily associated with older half-duplex hubs. 

Modern full-duplex switches largely eliminate the need for CSMA/CD because collisions do not happen on full-duplex links.