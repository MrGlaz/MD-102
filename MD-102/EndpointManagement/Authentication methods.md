PKI = Public Key Infrastructure

Windows Hello for Business
Key certificate trust
TPM

![[Authentication methodes.png]]

Tier 1 (no PKI)
Cloud Kerberos auth - hybrid - uses Entra Kerberos

Tier 2 (DC certs)
Key trust

Tier 3 (DC-user)
Certificate Trust
TPM 2.0 on W11 for compliance


**Cloud-only tenants**: No trust type is required;
**Hybrid tenants — new deployments**: Cloud Kerberos trust.
**Hybrid tenants — existing PKI**: Key trust is an option if you already issue DC certificates. Certificate trust suits environments that also issue user certificates for other purposes.
**User experience**: All three models let users sign in with PIN or biometrics;

