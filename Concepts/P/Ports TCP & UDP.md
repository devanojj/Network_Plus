#domain/1-0-Networking-Concepts


| Portocol                      | Port         |
| ----------------------------- | ------------ |
| HTTP                          | [[TCP]] 80   |
| [[TFTP]]                      | UDP  69      |
| [[NTP]]                       | UDP 123      |
| [[SNMP]] Agent                | UDP 161      |
| [[SNMP]] Manager              | UDP 162      |
| LDAP                          | TCP 389      |
| HTTPS                         | TCP 443      |
| Syslog                        | UDP 514      |
| SMTP/TLS                      | TCP 587      |
| [[LDAPS]]                     | TCP 636      |
| SQL Server                    | TCP 1433     |
| RDP                           | TCP 3389     |
| SIP non-encrypted             | TCP/UDP 5060 |
| SIP encrypted                 | TCP/UDP 5061 |
| FTP Data Connection           | TCP 20       |
| FRP Control Connection        | TCP 21       |
| SSH/SFTP                      | TCP 22       |
| [[Telnet]]                    | TCP 23       |
| [[SMTP]]                      | TCP 25       |
| [[DNS]]                       | TCP/UDP 53   |
| DHCP Server                   | UDP 67       |
| DHCP Client                   | UDP 68       |
| [[SMB]]                       | TCP 445      |
| [[NetBIOS]] (Name Service)    | UDP 137      |
| [[NetBIOS]] (Datagram)        | UDP 138      |
| [[NetBIOS]] (Session Service) | TCP 139      |
| Syslog (encrypted)            | TCP 6514     |
| DoT                           | TCP 853      |
| TACAS+                        | TCP 49       |
| iSCSI                         | TCP 3260     |
| IMAP                          | TCP 143      |
| SMTPS (Modern)                | TCP 587      |
| [[POP3]] (Don't need)         | TCP 110      |
| [[POP3S]] (Don't need)        | TCP 995      |






File Transfer Protocol (FTP) 20/21
Secure File Transfer Protocol (SFTP) 22
Secure Shell (SSH) 22
Telnet 23
Simple Mail Transfer Protocol (SMTP) 25
Domain Name System (DNS) 53
Dynamic Host Configuration Protocol (DHCP) 67/68
Trivial File Transfer Protocol (TFTP) 69
Hypertext Transfer Protocol (HTTP) 80
Network Time Protocol (NTP) 123
Simple Network Management Protocol (SNMP) 161/162
Lightweight Directory Access Protocol (LDAP) 389
Hypertext Transfer Protocol Secure (HTTPS) 443
Server Message Block ([[SMB]]) 445
Syslog 514
Simple Mail Transfer Protocol Secure (SMTPS) 587
Lightweight Directory Access Protocol over SSL (LDAPS) 636
Structured Query Language (SQL) Server 1433
Remote Desktop Protocol (RDP) 3389
Session Initiation Protocol (SIP) 5060/5061


Ports tell us **what services are running on network servers**. Services listen on specific ports (HTTP on 80/443, SSH on 22, RDP on 3389, etc.)