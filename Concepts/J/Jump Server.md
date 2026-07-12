#domain/1-0-Networking-Concepts

(Bastion host) gateway that remote admin connect through to reach internal servers. Centralised authentication, session logging, limited attack surface


Harder to compromise and placed in the [[DMZ]] or management [[VLAN]]

| Feature               | Jump Box | [[Access Gateway]] |
| --------------------- | -------- | ------------------ |
| Secure intermediary   | Yes      | No                 |
| Administrative access | Yes      | No                 |
| End-user access       | No       | Yes                |
| Hardened system       | Yes      | No                 |