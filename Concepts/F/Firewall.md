#domain/4-0-Network-Security

Hardware device or software application that monitors and controls incoming and outgoing network traffic based on predefined security rules.

==**Stateful vs. Stateless**== 
Stateful firewalls remember the context of active connections (if traffic goes out, the return traffic is automatically allowed). Stateless (like an ACL) evaluates every single packet individually based solely on rules, regardless of existing connections.

- Application Level Firewall or [[WAF]]
- [[NGFW]]/[[UTM]]


==**Implicit Deny**==
The last, invisible rule on every firewall or ACL: "If traffic isn't explicitly permitted above, drop it."


==**Geofencing**== 
Restricting access based on the geographic location (GPS or IP geolocation) of the user.

