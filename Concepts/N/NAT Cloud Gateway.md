#domain/2-0-Network-Implementation

- Lets devices create outbound connections 
- Blocks inbound connection 
- Translates private IP to public IP
- Cloud construct 



If an internal host started the connection:

```
PC ─────────► Internet
```

The reply is allowed because the NAT gateway already has a state entry.

```
Internet ─────────► PC
```

This is why NAT gateways provide a basic level of protection—they only allow traffic that is part of an existing connection.

---

## Can inbound connections ever work?

Yes, but **not through a basic NAT gateway alone**.

You need one of the following:

- **Port forwarding (Destination NAT/DNAT)**
- **Static NAT**
- A **firewall rule** permitting the traffic
- A **load balancer or reverse proxy** (common in cloud environments)

For example:

```
203.0.113.5:443
        │
        ▼
192.168.1.20:443
```

Without a rule like this, inbound traffic is dropped.