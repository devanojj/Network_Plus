#domain/1-0-Networking-Concepts

An [[IPv6]] method for a device to auto-generate its 64-bit interface ID directly from its 48-bit MAC address (no DHCP needed).

**Steps:**
1. Split the 48-bit MAC address in half (24 bits + 24 bits).
2. Insert **FF:FE** in the middle, bringing it to 64 bits.
3. Flip the **7th bit** of the first byte (the universal/local bit) to mark it as modified.

**Example:**

- MAC: `00:1A:2B:3C:4D:5E`
- Split: `00:1A:2B` + `3C:4D:5E`
- Insert FF:FE: `00:1A:2B:FF:FE:3C:4D:5E`
- Flip 7th bit of first byte: `02:1A:2B:FF:FE:3C:4D:5E`

**Exam angle:** EUI-64 is a known **privacy concern** — since the MAC is embedded/derivable from the IPv6 address, the device is trackable across networks. This is why modern OS's (e.g., Windows) use randomised interface IDs by default instead of EUI-64.