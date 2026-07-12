#domain/1-0-Networking-Concepts

**Transmission Control Protocol** - Layer 4 - Transport - Segment 

==3 way handshake== 
1. **SYN:** Client says _"I want to connect"_
2. **SYN-ACK:** Server replies _"OK, I got that, ready to connect"_
3. **ACK:** Client confirms _"Great, let's go"

==Connection Termination (Four-Way Close)==  
Ending a TCP session is a separate process from starting one:
1. **FIN:** "I'm done sending data" Device 1 
2. **ACK:**  "Acknowledged" Device 2 
3. **FIN:** "I'm done too" Device 2 
4.  **ACK:** connection closed Device 1

==Windowing== 
TCP flow control mechanism. Rather than waiting for an ACK after every single segment, TCP allows the sender to transmit multiple segments up to a limit called the **window size** before pausing for acknowledgment. The _receiver_ advertises it

==TCP Flags==
*   **SYN:** Synchronise (starts connection)
*   **ACK:** Acknowledgment (confirms receipt)
*   **FIN:** Finish (graceful termination)
*   **RST:** Reset (immediate, ungraceful termination/connection refusal)
*   **PSH:** Push (pushes data directly to the application layer, bypassing buffers) (Used for time-sensitive, interactive data)
*   **URG:** Urgent (tells receiver to process this data immediately) (Rare in modern practice)