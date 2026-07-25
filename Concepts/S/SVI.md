#domain/2-0-Network-Implementation

**==Switch Virtual Interface==**
Virtual interface configured on a switch that represents a whole VLAN
No physical port needed

To route traffic between VLAN 10 and VLAN 20, you had to send the traffic out of the switch, across a physical trunk cable, into a router's subinterface, and then back down to the switch. This takes up physical ports and can create a bandwidth bottleneck.


Modern enterprise networks use Multilayer Switches (switches that can perform Layer 3 routing). Instead of sending traffic to an external router, the switch handles the routing internally using SVIs.

1. You create **SVI 10** and assign it an IP address for VLAN 10.
2. You create **SVI 20** and assign it an IP address for VLAN 20.
3. When a computer on VLAN 10 wants to talk to a computer on VLAN 20, the traffic hits SVI 10, the switch routes it internally at lightning speed to SVI 20, and delivers it to the destination. No external router or physical cable is needed!


| Phrase in question                                                                       | Answer                                                                                                   |
| ---------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| "Layer 3 switch," "single device does switching and routing"                             | SVI                                                                                                      |
| "single trunk link to a router," "subinterfaces," "external router routes between VLANs" | Router-on-a-stick                                                                                        |
| "why is RoAS less preferred"                                                             | single physical link = bandwidth bottleneck / single point of failure vs. SVI's internal backplane speed |

