#domain/2-0-Network-Implementation

A sub-interface is a logical division of a physical router interface, allowing one physical port to act as multiple virtual interfaces — each with its own IP address, VLAN tag, and configuration.

More than 1 IP to a single interface

Used in "Router on a Stick" setups. One physical router port is divided into multiple logical subinterfaces (e.g., `GigabitEthernet0/0.10` for VLAN 10, `0/0.20` for VLAN 20) to route traffic between different VLANs.





