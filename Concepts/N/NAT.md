**Network address translation** 
- Dynamic NAT maps private IP's to a pool of public IP's
- Static NAT maps one private IP to one public IP
- [[PAT]] is a specific form on NAT 
- [[NAT Cloud Gateway]]
- [[NAT64]]


| NAT Term | Description | Example |
|----------|-------------|---------|
| **Inside Local** | The private IP address of a device on your local network. | `192.168.1.5` |
| **Inside Global** | The public IP address your router uses to represent the inside device on the Internet (the translated IP). | `203.0.113.10` |
| **Outside Local** | The IP address of the external (destination) device as seen from the local network. Usually the same as the Outside Global address. | `142.250.190.78` |
| **Outside Global** | The real public IP address of the destination server on the Internet. Usually the same as the Outside Local address. | `142.250.190.78` |



==Exam signal / distractors==
- If question stresses "one-to-one, dedicated" → Static NAT
- If question stresses "pool of addresses" → Dynamic NAT
- If question stresses "single public IP, many internal devices, home router" → PAT
