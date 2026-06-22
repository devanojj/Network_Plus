**Certificate Signing Request**
Before a server can obtain a signed digital certificate from a [[CA]], the server administrator must generate a CSR locally on the machine. 

This request packages the server's identity details and its newly generated **Public Key** to send to the CA for signing.

The admin sends the CSR to the CA. The CA signs it and returns the completed digital certificate.


The server administrator generates the key pair (Public and Private) locally _before_ sending the public portion inside the CSR to the CA. The CA does not generate the private key for you!

The CSR is simply the vehicle used to securely request the binding of an identity to a public key by a trusted third party (the Certificate Authority).