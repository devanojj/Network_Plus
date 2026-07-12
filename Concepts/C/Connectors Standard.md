#domain/1-0-Networking-Concepts


| Connector   | Cable Type                          | Typical Use                         | Notes                         |     |
| ----------- | ----------------------------------- | ----------------------------------- | ----------------------------- | --- |
| RJ45        | Twisted Pair                        | All Ethernet (patch cords)          | 8P8C modular plug             |     |
| [[LC]]      | Fiber (most common) (Local Connect) | Modern switches, [[SFP]]/SFP+       | Smallest form-factor, duplex  |     |
| [[SC]]      | Fiber (Subscriber connect)          | Older equipment, telecom            | Push-pull, duplex             |     |
| [[ST]]      | Fiber (Straight tip)                | Legacy installations                | Bayonet mount                 |     |
| [[MPO]]/MTP | Fiber (parallel)                    | 40/100G+ Ethernet                   | Multi-fiber (8/12/24 strands) |     |
| [[F-type]]  | Coaxial                             | Cable modems, TV                    | Screw-on                      |     |
| [[BNC]]     | Coaxial (legacy)                    | Old 10BASE2 networks                | Bayonet, twist-lock           |     |
| [[MPO]]     | Fiber                               | Switches                            | 40G/100G                      |     |
| MT-RJ       | Fibre                               | Mechanical Transfer Registered Jack | (Not needed)                  |     |


*MPO/MTP:* Multi-fiber Push On, terminates multiple fibres in a single connector. Mechanical Transfer Push On, higher performance version of MPO. 


| Acronym  | Definition                | Speed |
| -------- | ------------------------- | ----- |
| [[QSFP]] | Quad SFP                  |       |
| [[SFP]]  | Small form pluggable      | 1G    |
| SFP+     | Small form pluggable plus | 16G   |


[![Four Common Types of Fiber Optic Connectors | by Angelina1874 | Medium|516](https://miro.medium.com/0*yx5EPU51whLFYfAn.)



MPO 
[![What is an MPO Connector?|383](https://www.mssdatasolutions.com.au/media/wysiwyg/What-is-an-MPO-connector-920x376.jpg)



QSFP
![[Pasted image 20260607161903.png|379]]
SFP on one end + QSFP on the other = incompatible form factors → link stays down even when cabling, length, and interface status are fine.

