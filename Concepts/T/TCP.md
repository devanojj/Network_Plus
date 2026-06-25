Transmission Control Protocol 
3 way handshake 

- **SYN** — Client says _"I want to connect"_
- **SYN-ACK** — Server replies _"OK, I got that, ready to connect"_
- **ACK** — Client confirms _"Great, let's go"

Layer 4 - Transport

Windowing is a TCP flow control mechanism. Rather than waiting for an ACK after every single segment, TCP allows the sender to transmit multiple segments up to a limit called the **window size** before pausing for acknowledgment.


4 Layers of the TCP stack - Transport layer, Internet layer, Application layer, Network interface layer