*WPS:*
Wi-Fi Protected Setup
Simplifies configuration of new wireless networks by allowing non-technical users to easily configure network security settings, by presses a button

*WEP:*
Wired Equivalent Privacy

*WPA:*
Wi-Fi Protected Access

*PSK:*
Pre-Shared Key used in WPA & WPA2

*WPA3-SAE:*
Simultaneous Authentication of Equals, used in WPA3-Personal, authentication method. Strong method of authentication.



WPA, WPS & WEP are security risk

| Protocol                            | Security Level                    | Key Details                                                                                                                                                                                                  |
| :---------------------------------- | :-------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **WEP** (Wired Equivalent Privacy)  | **Broken**                        | Deprecated and insecure. Uses the weak [[RC4]] encryption algorithm and can be cracked in minutes. **Never use it.**                                                                                         |
| **WPA** (Wi-Fi Protected Access)    | **Vulnerable**                    | An interim replacement for WEP. It introduced [[TKIP]] improvement but is also now considered insecure.                                                                                                      |
| **WPA2** (Wi-Fi Protected Access 2) | **Secure (Current Standard)**     | The current standard for wireless security. It uses **AES (Advanced Encryption Standard)**, which is very strong. This is the minimum you should be using.                                                   |
| **WPA3** (Wi-Fi Protected Access 3) | **Most Secure (Future Standard)** | The latest standard. It offers even stronger security, especially against offline brute-force attacks. It uses **SAE (Simultaneous Authentication of Equals)** for authentication, replacing the PSK method. |

WPA3 - can be used with QR code?

### Authentication Methods:
- **PSK (Pre-Shared Key) / WPA-Personal:** This is what you use at home. Everyone on the network shares the same password. It's vulnerable if the password is weak or is shared with untrusted guests.
- **Enterprise Mode / 802.1X:** This is used in corporate environments. It provides each user with a unique credential (e.g., username and password). It requires a **RADIUS server** to handle the authentication. When you connect, the access point communicates with the RADIUS server to verify your identity before granting access. **EAP (Extensible Authentication Protocol)** is the framework used in 802.1X to perform the authentication.


WPA2 / WPA3 Enterprise need a [[RADIUS]] server


