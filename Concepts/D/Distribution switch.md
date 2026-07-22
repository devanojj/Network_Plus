#domain/1-0-Networking-Concepts

Aggregates access switches, implements routing, QoS policies and security, routing between VLANs


**==Quality of Service==**  
Classified and marked (DSCP tags) at the access layer, but the actual _policy enforcement_ (queuing, scheduling, traffic shaping) happens at the distribution layer.
Packets enter here with their [[DSCP]] markings already set and the distribution switch decides how to prioritise them across the network. 

Exam signal: _"policy enforcement"_ or _"traffic prioritisation across the network"_ → distribution layer.


==**Inter-VLAN routing**==
VLANs are segments defined at the access layer, but they can't communicate without a Layer 3 device. The distribution layer (a multilayer switch or router) performs inter-[[VLAN]] routing, acting as the default gateway for each VLAN. Exam signal: _"routing between VLANs"_ → distribution layer