
> **Management status** (handled by Intune)
> **Foundational identity** (handled by Microsoft Entra ID)


![[troubleshoots.png|533]]

### In Intune

Review the client logs when you need to identify the exact failure point. The Intune Management Extension stores app-related logs under `C:\ProgramData\Microsoft\IntuneManagementExtension\Logs`. These logs show policy processing, app workload activity, detection checks, applicability checks, and script execution.

### Using Microsoft Edge for iOS/Android (recommended)

Microsoft Edge has a hidden diagnostic page built specifically for Intune administrators.
1.  `about:intunehelp` or `edge://intunehelp`


> **Policy troubleshooting workflow — quick notes**

1. **Verify assignment** = correct group, user/device is member, check filter conditions
2. **Check device eligibility** = enrolled, compliant, licensed, platform matches policy target
3. **Review status reports** = per-device/per-setting status, look for errors
4. **Sync device** = manual sync often fixes stale "pending" status
5. **Troubleshooting + Support blade** = detailed enrollment/compliance/assignment view, codes
6. **Check conflicts** = other policies on same device with overlapping/conflicting settings
7. **Fix root cause**



> Collect device logs
* Windows Update Log = Get-WindowsUpdateLog
* CBS.log = `C:\Windows\Logs\CBS\`, system component installation, which feature updates use extensively
* SetupDiag.exe = Microsoft tool that analyzes setup issues.
* DISM logs = provide detail on update staging operations.

> Deployment conflicts

![[Pasted image 20260912232909.png]]