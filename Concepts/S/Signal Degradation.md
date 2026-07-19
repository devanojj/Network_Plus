| Term             | What it is                                                                   | Cause/Context                                                            |
| ---------------- | ---------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| **Crosstalk**    | Signal from one wire pair bleeds into an adjacent pair, causing interference | Poor twist ratio, cable damage, cables bundled too tightly               |
| **Interference** | External signal disrupts the cable's signal                                  | EMI from power lines, motors, fluorescent lights; RFI from radio sources |
| **Attenuation**  | Signal weakens/loses strength as it travels over distance                    | Cable run exceeds max distance spec (e.g., 100m for copper Ethernet)     |

==**CRC errors**==  
Frame corrupted in transit — failed cyclic redundancy check, points to cabling/interference problems

==**Runts**==
Frames smaller than 64 bytes — often from collisions or bad NIC

==**Giants**==
Frames larger than max Ethernet size (1518 bytes without jumbo frames)

==**Drops**==
Packets discarded, often due to congestion/buffer overflow