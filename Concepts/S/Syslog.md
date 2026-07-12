#domain/3-0-Network-Operations

- Used for sending and receiving a log or event message.
- Routers, switches, firewalls and servers
- UDP Port 514 (most common) can also be TCP 514
- Application Layer 7
- No built in encryption unless wrapped in TLS
- Essentially errors, warning and system messages 




Below not needed
0=Emergency (system unusable)
1=Alert (action must be taken)
2=Critical (critical conditions)
3=Error
4=Warning
5=Notice
6=Informational
7=Debug

Single device logs, storage compare to [[SIEM]]