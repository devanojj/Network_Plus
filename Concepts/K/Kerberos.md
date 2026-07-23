#domain/1-0-Networking-Concepts

- Network authentication protocol — uses tickets, not passwords over the wire
- Key Distribution Center (KDC) issues Ticket Granting Tickets (TGTs)
- Port 88
- Used in Active Directory / Windows domain environments
- Provides mutual authentication (client and server verify each other)

It allows nodes communicating over an non secure network to securely prove their identity. It prevents passwords from being sent over the network, protecting against both eavesdropping and replay attacks.