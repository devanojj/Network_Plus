#domain/2-0-Network-Implementation

==**Native VLAN**== 
VLAN used to handle untagged frames on a truck port

==**Voice VLAN**==  
QoS for VoIP

==**Inter-VLAN routing**== 
One physical interface connects to a switch trunk port and handles traffic for multiple VLANs via 802.1Q tagging. Each [[Subinterface]] gets its own IP and VLAN ID.

12-bit VLAN ID field, limiting networks to 4,096 unique VLANs

==**Default VLAN**== 
By default, all ports on a switch belong to VLAN 1. It cannot be deleted or renamed.

==**Management VLAN:**== 
A specific VLAN dedicated to managing the network devices (SSH, HTTPS, SNMP traffic). Best practice is to change this away from VLAN 1.

==**VLAN Ranges***==
Normal range is 1-1005 (stored in `vlan.dat`). Extended range is 1006-4094 (usually requires VTP transparent mode on older switches).


