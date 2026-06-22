Section of a DNS database that stores records used to resolve domain names into IP addresses.

 *Forward Lookup Zone*
- Primary role: **Maps hostnames to IP addresses**
- Normal DNS resolution (name → IP)
- Example: example.com → 192.168.1.1
- Database, [[A]] record lives inside this


*Reverse Lookup Zone*
- **Maps IP addresses to hostnames**
- Used for verification and security purposes
- Example: 192.168.1.1 → example.com
- Database, where [[PTR Record]] lives