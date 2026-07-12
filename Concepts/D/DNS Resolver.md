#domain/1-0-Networking-Concepts

Also known as the **Recursive Resolver**, it acts as the "middleman" or "valet" between a client application (like a web browser) and the global DNS infrastructure.

To accept a human-readable domain name (e.g., `google.com`) from a client, hunt down the matching IP address across the internet, and return that IP to the client.

When chasing down an unknown domain, the resolver sends **iterative** queries to Root, TLD, and Authoritative servers, following a chain of referrals until it finds the correct record.