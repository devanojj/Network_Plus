#domain/1-0-Networking-Concepts

**Simple mail transfer protocol** 

Sending email messages between mail servers 
Sending email messages from a client device

Port TCP 25


- SMTP submission (client-to-server, authenticated): port 587 
- SMTPS (implicit TLS): port 465 - **Port 587 = enable transport encryption (STARTTLS) for client auth/submission — not "encrypt the email" on the client** 
- If a server advertises AUTH (PLAIN/LOGIN) without encryption, credentials are sent in cleartext → fix = enforce transport encryption on 587, not message-level encryption

