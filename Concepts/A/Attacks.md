#domain/4-0-Network-Security

**==VLAN hopping==**
Access data on another VLAN, typically by manipulating traffic with an unauthorised VLAN ID
Caused by switch spoofing + double tagging
Native VLAN misconfiguration enables double tagging
Change native VLAN to unused VLAN, disable auto-trunking on access ports

**==MAC flooding==**
Overwhelming a switch with a large volume of frames from fake source addresses, leading the switch to broadcast traffic to all ports

**==ARP spoofing==**
Malicious ARP packets to a target device, falsely claiming to be a trusted device by associating their own MAC address with the IP address of the trusted device. 

**==ARP poisoning==** 
Device's ARP cache contains incorrect IP-to-MAC address mappings
After an **ARP cache has been poisoned**, the victim's device sends traffic to the attacker instead of the legitimate device.

==**DNS Spoofing (The Overarching Goal)**== 
The act of masquerading as a legitimate DNS server or forging DNS responses to redirect users to a malicious IP address instead of the real one.

**==DNS Poisoning (A Specific Attack Method)**== 
Injecting fake records directly into a **DNS Resolver's cache** so that _everyone_ using that resolver gets redirected until the cache expires.

**==IP Spoofing==**
An attacker creates IP packets with a forged source IP address. This is often used in DDoS attacks to hide the origin of the attack and make it harder to block.

**==DoS/DDoS==**
An amplification attack is a common DDoS technique where an attacker uses a small request to a public server (like DNS or NTP) that generates a much larger response, directing that response to the victim's IP address.

**==Directly poison DNS on client file system==**
Host file is poisoned, bypass DNS 

**==Teardrop==**
DoS attack using malformed IP fragmentation, under DoS attacks
Mostly historical due to modern OS protections





