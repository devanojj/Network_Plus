### Network Implementation 
100HDx = 100MBps Half Duplex 
100FDx = 100MBps Full Duplex


| Antenna gain                                       | Radiation pattern            | Range   | Coverage area                 | Typical use                                             |
| -------------------------------------------------- | ---------------------------- | ------- | ----------------------------- | ------------------------------------------------------- |
| Low dBi (e.g., omnidirectional ~2-5 dBi)           | Wide, spherical/donut-shaped | Shorter | Broad, covers all directions  | Open office, general AP coverage                        |
| High dBi (e.g., directional/Yagi/dish, 10-20+ dBi) | Narrow, focused beam         | Longer  | Concentrated in one direction | Point-to-point links, long hallways, bridging buildings |
*Higher dBi doesn't mean more power just more focused area*


### Networking Concepts 
Public cloud $\rightarrow$ users access application through a web interface and data is stored locally 

Wireless extenders have to be in the same bubble as the original AP.

NAS $\rightarrow$ structured as a network with multiple storage devices

[[OSI]] Layer 4 uses segments as the PDU protocol data unit 

Site-to-Site VPN $\rightarrow$ AES and SHA512 is best as maximum security is required  

### Network Operations
[[RPO]] $\rightarrow$ 1st to check after a disaster

[[Nslookup]] $\rightarrow$ Fails, needs to create reverse look up zone. It failed due to missing [[PTR Record]]. The reverse look up zone on the DNS confirms the PTR


### Network Troubleshooting 
Types of POE (Type 3 POE++ vs Type 4 POE++)

Reflection or signal bounce makes signals bounce of items, hard metal causes this
Other material like water or brick causes 

[[STP]] will have crosstalk, CAT6 will prevent cross talk

[[Tcpdump]] can be used to troubleshoot packet headers + content in ASCII or HEX


### Network Security 


