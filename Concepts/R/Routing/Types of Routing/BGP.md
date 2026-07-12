#domain/2-0-Network-Implementation

- Path vector routing protocol
- Exterior gateway protocol (EGP) — routes between autonomous systems (AS)
- Slow convergence by design — prioritises stability over speed
- TCP port 179
- Uses **path attributes** to select routes; key attribute is **AS path** (shorter = preferred)
- eBGP = between different autonomous systems | iBGP = within the same AS
- Administrative Distance (AD): **eBGP = 20** (highly trusted), **iBGP = 200** (untrusted/internal backup)
- Path selection based on fewest AS hops