#domain/4-0-Network-Security

**Certificate Authority**
System for creation, management and revocation of digital signatures, examples - Let's Encrypt, DigiCert

Trusted entity within [[PKI]] that issues and signs digital certificates, binding a public key to an identity


| *Root CA*                                                  | *Intermediate CA*                                                                                                                                                      |
| ---------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Top of the trust chain, self-signed, ultimate trust anchor | Sits below root, issues end-entity certificates. Keeps the root CA offline and protected<br>The intermediate issues cert to web server and then your browser trusts it |

2 ways to check if a certificate has been revoked : [[CRL]] / [[OCSP]]






