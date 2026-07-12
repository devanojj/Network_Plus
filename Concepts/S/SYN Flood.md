#domain/1-0-Networking-Concepts

**Denial-of-Service (DoS)** attack that abuses the **TCP three-way handshake**.

An attacker sends **many SYN packets** to a server, often using **spoofed source IP addresses**.

1. Attacker → Server: SYN
2. Server → "Fake" Client: SYN-ACK
3. No ACK is returned

The server keeps these connections in a **half-open state**, waiting for the final ACK.

If enough fake SYN requests are sent:

- The server's connection table fills up.
- Legitimate users cannot establish connections.
- Service becomes slow or unavailable.