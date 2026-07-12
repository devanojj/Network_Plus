#domain/1-0-Networking-Concepts

*Generic Routing Encapsulation*
- Tunneling protocol that encapsulates packets in a network protocol inside another
- No security itself 
- Used to connect networks over the Internet
- IP protocol 47
- Not encrypted by itself, it just **wraps/encapsulates** packets so they can be carried across a network
-  Often **combined with IPSec** to add encryption since GRE alone provides none
- used to carry non-IP or private-addressed traffic across the public internet, link two private networks over the internet as if they were directly connected.

Tunneling traffic over unsupported types of networks

[[VPN]]