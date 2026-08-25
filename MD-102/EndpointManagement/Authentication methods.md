PKI = Public Key Infrastructure

Windows Hello for Business
Key certificate trust
TPM

![[Authentication methodes.png]]

Note structure : **Decision Drivers** (Deployment Type, Security Hardware, and PKI Requirements):

| **Environment Scenario**     | **Recommended Trust Type** | **On-Prem PKI Needed?**  | **Deployment Effort** |
| ---------------------------- | -------------------------- | ------------------------ | --------------------- |
| **Cloud-Only**               | **Cloud Kerberos trust**   | **No**                   | **Low**               |
| **Hybrid (No PKI)**          | **Cloud Kerberos trust**   | **No**                   | **Medium**            |
| **Hybrid (DC Certs Only)**   | **Key trust**              | Yes (Domain Controllers) | **Medium**            |
| **Hybrid (DC + User Certs)** | **Certificate trust**      | Yes (DCs & Users)        | **High**              |
**Cloud-Only** or **Hybrid without PKI** = **Cloud Kerberos trust**
PKI/On-Prem AD = **TPM 2.0** (hardware-backed)

**Cloud-only tenants**: No trust type is required;
**Hybrid tenants — new deployments**: Cloud Kerberos trust.
**Hybrid tenants — existing PKI**: Key trust is an option if you already issue DC certificates. Certificate trust suits environments that also issue user certificates for other purposes.
**User experience**: All three models let users sign in with PIN or biometrics;

