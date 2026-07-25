#domain/1-0-Networking-Concepts

**==Virtual Private Network==** 

**==Clientless VPN==**
- Does NOT require VPN client software
- Uses a web browser (HTTPS)
- Limited access compared to full VPN
- Common for temporary users or contractors

**==[[IPsec]] VPN (Internet Protocol Security) - 3 Components==**
- [[AH]] 
- [[ESP]]
- [[IKE]]

**==Site-to-Site VPN==** 
- Connects one network to another network
- Always-on connection
- Commonly used between branch offices

[[GRE]] 

**==SSL/TLS VPN==**
- Operates at a higher layer (Layer 4-7) using the same technology as HTTPS
- **Clientless VPN**
- Accessible through a **web browser** with no dedicated VPN client needed

**==Tunneling==**
**Full tunnel** — ALL traffic from the client goes through the VPN, including general internet browsing
**Split tunnel** — only traffic destined for the corporate network goes through the VPN, everything else goes directly to the internet. More efficient but slightly less secure

**==Signal phrases==**
- "Two office locations permanently connected via routers/firewalls" → **site-to-site VPN**
- "Remote employee connects laptop to corporate network" → **client-to-site VPN**
- "Browser-based VPN access, no software install" → **clientless**
- "All traffic routes through VPN, including internet-bound" → **full tunnel**
- "Only corporate traffic routes through VPN, rest goes direct" → **split tunnel**






