#domain/4-0-Network-Security

**Certificate Authority**
System for creation, management and revocation of digital signatures, examples - Let's Encrypt, DigiCert

Trusted entity within [[PKI]] that issues and signs digital certificates, binding a public key to an identity


| *Root CA*                                                  | *Intermediate CA*                                                                                                                                                      |
| ---------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Top of the trust chain, self-signed, ultimate trust anchor | Sits below root, issues end-entity certificates. Keeps the root CA offline and protected<br>The intermediate issues cert to web server and then your browser trusts it |

2 ways to check if a certificate has been revoked : [[CRL]] / [[OCSP]]


**PKI (Public Key Infrastructure)**: framework for issuing/managing digital certificates that bind a public key to an identity 
**Self-signed certificate**: cert not issued by a trusted CA; browser/client won't inherently trust it (common in internal/test environments) 


> Out of scope > Root CA vs Intermediate CA trust chain, CRL, OCSP, specific CA vendors (Let's Encrypt, DigiCert) — Security+ depth, not in N10-009 objectives.






