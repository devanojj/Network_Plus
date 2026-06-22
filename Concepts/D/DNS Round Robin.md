DNS-based load balancing technique. Instead of an `A` or `AAAA` record resolving to just one IP address, the DNS server holds multiple IP addresses for a single hostname


As different clients query the DNS server for the hostname, the DNS server hands out the IP addresses in a rotating, sequential order (Server A, then Server B, then Server C, then back to Server A).