#domain/1-0-Networking-Concepts

- **What it does:** It prevents security appliances or switches from falling victim to resource exhaustion by limiting the rate of incoming broadcast packets or MAC addresses allowed on a port.

- **The Threat it Prevents:** Specifically used to mitigate **MAC Flooding attacks** (where an attacker floods a switch with random MAC addresses to fill up its CAM/MAC table) or general **Broadcast Storms**. When a standard switch's MAC table overflows, it fails open and acts like a hub, broadcasting all data out of all ports—allowing an attacker to easily sniff private traffic.