#domain/1-0-Networking-Concepts

## **What is Software-Defined Networking (SDN)?**

- decouples the network control logic (the "brains") from the physical forwarding hardware (the "muscle").
- Allows network administrators to manage, provision, and automate the entire network fabric dynamically through a centralized software platform 


## **SDN vs. Traditional Networking**

| Feature               | **Traditional Networking**                                                    | **Software-Defined Networking (SDN)**                                                                                  |
| :-------------------- | :---------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------- |
| **Control Plane**     | Distributed (configured and run on every individual device).                  | Centralised (managed by a software SDN Controller).                                                                    |
| **Configuration**     | Manual, command-by-command (CLI) on a device-by-device basis.                 | Automated and programmable via central controller APIs.                                                                |
| **Adaptability**      | Slow to scale; path changes require protocol convergence across many routers. | Agile; controller instantly reprograms traffic flows network-wide.                                                     |
| **Vendor Lock-in**    | High (proprietary command sets and operating systems).                        | Lower (controller abstracts hardware using open standards like OpenFlow).                                              |
| **Data Plane**        | Distributed (configured and run on every individual device).                  | Actually *forwards* traffic based on control plane decisions                                                           |
| **Management Plane**  | Distributed (configured and run on every individual device).                  | Administrative access only (SSH, web console, API config). NOT decision-making.                                        |
| **Application Plane** | Doesn't exist                                                                 | Sits above control plane; business apps/services request network behavior via APIs (e.g., "give me low-latency path"). |






