#domain/1-0-Networking-Concepts

Part of Wi-Fi [[802.11]]
Avoid collisions 
Listen before talk access method 

==**Carrier Sense Multiple Access with Collision Avoidance**==

Tries to avoid collisions by listening before transmitting, uses random backoff timers and may use request to send to reserve the channel. 


It uses a "listen before talk" method. If the channel is clear, it still uses a random backoff timer before transmitting just to be safe. In highly congested environments, it may also use an **RTS/CTS (Request to Send / Clear to Send)** mechanism to formally reserve the wireless channel before sending data.