*Open systems interconnection*

#### OSI Layer 1 - Physical - Bit 
Hub 
Network Cabling
Repeater


#### OSI Layer 2 - Data Link Layer - Frames 
Bridge 
Media converter
Switch 
Network Adapter 
NIC
ARP




#### OSI Layer 3 - Network - Packet 
[[ICMP]] / IP


#### OSI Layer 4 - Transport - Datagram / Segment
Issues where data packets are being delivered out of sequence and some packets are missing entirely. This is layer 4
[[UDP]] / [[TCP]]


#### OSI Layer 5 – Session Layer - Data 
**Purpose:** Establishes, manages, and terminates communication sessions between applications.

- Establishes sessions between applications
- Maintains and manages active sessions
- Synchronises communication using checkpoints
- Terminates sessions gracefully
- Handles session recovery after interruptions

**Examples:**

- NetBIOS sessions
- RPC (Remote Procedure Call)
- API session management



#### Layer 6 - Presentation Layer
**Purpose:** Translates, formats, encrypts, and compresses data so the Application Layer can use it.

- Data encryption and decryption
- Data compression and decompression
- Data translation between application and network formats
- Character encoding/translation (e.g., ASCII, Unicode, UTF-8)
- Data formatting and serialization
- Ensures data is presented in a format the Application Layer can understand

**Examples:**

- SSL/TLS encryption functions
- JPEG, PNG image formats
- MPEG video formats
- ASCII and Unicode character translation



#### Layer 7 Application Layer

HTTP / FTP / SMTP



