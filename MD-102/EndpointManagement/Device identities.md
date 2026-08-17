In Entra ID
- [[Registration]] (best for BYOD) = workplace join
- [[Join]] (best fo cloud-only)
- [[Hybrid joined]] (best for hybrid env with ADSync) = domain+register (Need)



Entra ID : device enrollment - CA - Group targeting - SSO

Intune installs a MDM certificate on the device -> trusted connection

Best practices :
- plan group (mgmt) structure > then policies
- Least-privilege access
- 2FA
- Review identities and permissions


LAPS only on [[Join]] and [[Hybrid joined]]
+Must configure a LAPS policy in Intune (**Endpoint security** > **Account protection**)

### Require multi-factor authentication to register or join devices
Use a CA policy to grand control MFA

## Maximum number of devices per user
Default 50
Max 100

## Device identifiers for corporate-owned devices
Devices are automatically marked as corporate-owned when:

- Enrolled through Windows Autopilot
- Enrolled through Apple Automated Device Enrollment (ADE)
- Enrolled as Android Enterprise fully managed, dedicated, or corporate-owned work profile devices
- Purchased through Apple Business Manager or Apple School Manager

## Enterprise State Roaming
Sync app data accross Win devices


**CMDS**
Removing a device from Entra ID with `dsregcmd /leave` will immediately unenroll the device and Conditional Access and Intune Management won't work anymore.

