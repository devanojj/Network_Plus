#domain/1-0-Networking-Concepts

*   **In-Band Management:** Managing a router or switch over the standard production network (e.g., SSHing into a switch via the office Wi-Fi). If the network goes down, you lose management access.
*   **Out-of-Band (OOB) Management:** A dedicated, separate network just for managing devices. Often uses a dedicated "management port" on the switch, connected to a totally separate management switch. If the main network crashes, you can still reach the equipment.
*   **Console Connection:** The ultimate OOB method. Taking a laptop and physically plugging a serial console cable directly into the device.