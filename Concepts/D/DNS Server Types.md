#domain/1-0-Networking-Concepts


**==Authoritative DNS Server==**
- **Stores and provides original DNS records** for a domain
- Has definitive answers for queries about its zones
- Source of truth for domain records


**==Primary DNS Server==**
- An authoritative server that stores the writable copy of DNS zone file
- Where DNS records are created and modified
- Master copy of the zone file
- Also called Master DNS server


**==Secondary DNS Server==**
- **Backup server** holding a copy of DNS records
- Gets records through zone transfers from primary (State of Authority)
- Provides redundancy and load distribution
- Also authoritative 


**==Non-authoritative DNS Server==**
- Responds to queries using **cached or forwarded data**
- Does NOT hold original records
- Typically a recursive resolver or caching server
