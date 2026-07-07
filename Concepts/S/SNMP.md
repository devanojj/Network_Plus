*Simple network management protocol*
- Used for monitoring CPU, memory usage, interface status, device failure, alters (traps)
- For devices like routers, switches, firewalls, servers and printers
- Application 

*SNMP Manager*
- Central monitor system, sends requests. Sometimes called a [[NMS]], receives notifications called traps on UDP port 162 

*SNMP Agent*
- Runs on a managed device, answers manager requests, collects device info. Software on the device. Manager _sends_ requests _to_ port 161 on the agent. Sends traps to the manager on UDP port 162.

*[[MIB]] 

Polling when manager asks device for status. 
Trap is when device sends an alert without being asked.


*SNMPv1 / SNMPv2*c
- Uses community strings like public / private for authentication 
- No encryption

*SNMPv3*
- Authentication, Encryption and Integrity 


SMTPS = SMTP over SSL 
- This is deprecated uses TCP port 465 
- STARTTLS is the upgrade


SNMP can read [[VLAN]] and port-assignment data from managed switches remotely — no CLI/console access needed. This can be done with SNMP OIDs (Object Identifier)
OID example : 1.3.6.1.2.1.14.2


[[NMS]] use this to map [[VLAN]]s → switch ports for automated inventory and compliance checks

Tools is used for evaluating network efficiency and identifying potential bottlenecks


SNMP Trap sends info when :the event that a failure or predefined threshold was crossed?



