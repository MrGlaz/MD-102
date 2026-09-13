
> **Compliance policies
- Define security/health standards; Intune checks devices against them → **compliant / non-compliant / not evaluated**
- Non-compliant response: notify user, mark non-compliant, or block access
- **Bridges to Conditional Access**: Intune reports status to Entra ID → CA can require "compliant" before granting access (e.g., block Teams for non-compliant devices)
- Platform-specific: separate policies per OS (Windows, iOS, Android)

> **Three requirement categories:**

1. **Device health** — antivirus active, BitLocker/FileVault, secure boot, min OS version
2. **Device security** — password/PIN complexity, encryption at rest, firewall, password expiration
3. **System security** — TPM presence, jailbreak/root detection

- Must meet **all** enabled settings to stay compliant — any drift (e.g., BitLocker disabled, AV expired) → status updates automatically

> **Compliance + Conditional Access**
-  **Only report status** — they don't block anything by themselves
- **[[Conditional Access]]** enforces access based on that status
- **Flow:** Intune evaluates device → reports compliant/non-compliant to Entra ID → user tries to access resource (Teams, SharePoint, Exchange) → CA checks status → **compliant = access granted, non-compliant = access denied**
- **Self-service remediation:** user must fix device to regain access — no manual IT ticket needed
- Result: automated, policy-driven enforcement + consistent security posture, not reactive one-off responses