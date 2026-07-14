==**Scenario**==

Remote users need a secure link to a web-aware app on a perimeter (DMZ) server. Recommended solution: **SSL VPN** (minimises firewall config changes vs. IPSec). Authentication: certificate-based.

**==Question==**
What is the **minimum** certificate requirement for this configuration?
**Answer: A server-side certificate only**

**==Why?==**
SSL VPN works the same way as any HTTPS/TLS connection:

- The **VPN gateway (server)** presents a certificate to the client.
- This certificate:
    - Proves the server's identity to the client
    - Enables the encrypted TLS tunnel to be established
- This is **non-negotiable** — no SSL/TLS session can be built without it.

Client certificates are **optional**, used for **mutual TLS (mTLS)** — a stronger authentication method where _both_ sides prove identity. But that's an enhancement, not the baseline requirement.