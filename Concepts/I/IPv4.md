## **IPv4 Address Structure**

- **32-bit address** represented in dotted-decimal format.
- Composed of **4 octets** (8 bits each), separated by periods (e.g., `192.168.1.1`).
- Each octet can have a decimal value ranging from `0` to `255`.
- Total address space: $2^{32} \approx 4.3 \text{ billion}$ addresses.
- Divided into a **Network ID** (identifies the network segment) and a **Host ID** (identifies the specific device interface). The boundary between them is defined by the [[Subnetting with Subnet Mask|Subnet Mask]].

---

## **IPv4 Address Classes**

Historically defined under classful addressing, which divides the address space into five classes (A, B, C, D, and E):

| Class | First Octet Range | Default Subnet Mask | CIDR | Purpose / Typical Use |
| :--- | :--- | :--- | :--- | :--- |
| **Class A** | `1` – `126` | `255.0.0.0` | `/8` | Large organizations (16,777,214 hosts per network) |
| **Class B** | `128` – `191` | `255.255.0.0` | `/16` | Medium-sized organizations (65,534 hosts per network) |
| **Class C** | `192` – `223` | `255.255.255.0` | `/24` | Small organizations (254 hosts per network) |
| **Class D** | `224` – `239` | N/A (No host portion) | N/A | **Multicast** traffic groups |
| **Class E** | `240` – `255` | N/A | N/A | Experimental and research purposes |

> [!NOTE]
> The range starting with `127` (i.e., `127.0.0.0/8`) is reserved for loopback testing. Specifically, `127.0.0.1` is used to test the local TCP/IP protocol stack of a host.

---

## **Private IPv4 Address Ranges (RFC 1918)**

Private IP addresses are reserved for internal use within a private network and are **non-routable on the public Internet**. Internal networks use [[NAT]] to translate private addresses to public ones for internet access.

| Class | Private Address Range | CIDR Block | Total Addresses |
| :--- | :--- | :--- | :--- |
| **Class A** | `10.0.0.0` – `10.255.255.255` | `10.0.0.0/8` | 16,777,216 |
| **Class B** | `172.16.0.0` – `172.31.255.255` | `172.16.0.0/12` | 1,048,576 |
| **Class C** | `192.168.0.0` – `192.168.255.255` | `192.168.0.0/16` | 65,536 |

---

## **APIPA (Automatic Private IP Addressing)**

- **Address Range**: `169.254.0.1` to `169.254.255.254` (CIDR: `169.254.0.0/16`).
- **Function**: Automatically assigned by the client OS when a device is configured to obtain an IP via [[DHCP DORA|DHCP]] but cannot contact or receive a response from a DHCP server.
- **Limitation**: Allows communication **only** with other local hosts on the same physical link/subnet that also have APIPA addresses. It does not assign a default gateway, meaning APIPA packets **cannot cross a router** (non-routable).

---

## **Special and Reserved Addresses**

- **Network Address**: The first address in a subnet where all host bits are `0` (e.g., `192.168.1.0`). Used to represent the network itself in routing tables. Cannot be assigned to a host.
- **Broadcast Address**: The last address in a subnet where all host bits are `1` (e.g., `192.168.1.255`). Used to send data to all hosts on that subnet. Cannot be assigned to a host.
- **Limited Broadcast**: `255.255.255.255`. Sent to every device on the local network segment. Routers do not forward this packet.
- **Directed Broadcast**: A broadcast targeted at a specific remote subnet (e.g., a packet sent to `192.168.2.255` from the `192.168.1.0/24` network). By default, modern routers drop directed broadcasts to prevent Denial of Service (DoS) amplification attacks (like Smurf attacks).

---

## **IPv4 Transmission Types**

1. **Unicast**: One-to-one communication. A packet is sent from one source address to a single destination host address.
2. **Broadcast**: One-to-all communication. A packet is sent from one source to all hosts on the local network segment (using either the local subnet broadcast address or `255.255.255.255`).
3. **Multicast**: One-to-many communication. A packet is sent from a single source to a group of interested devices subscribed to a Class D multicast destination address (e.g., `224.0.0.9` for RIPv2, `224.0.0.5` for OSPF). Efficiently reduces bandwidth consumption compared to sending multiple unicast packets.
