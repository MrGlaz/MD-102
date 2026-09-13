
>**Windows Autopatch**
- Cloud-native service = **fully automates** Windows update management end-to-end
- Removes need to manually manage update rings/deferral periods
- Automated deployment via **predefined deployment rings**

**Key functions:**
- Monitors device health pre/post-update
- Auto-pauses updates on problematic devices
- Manages restart timing/scheduling
- Tracks compliance, reports issues
- **Best for:** orgs wanting hands-off patch management, no manual ring/deferral upkeep
- Configure once → ongoing automated management

>**Device requirements** for Windows Autopatch:
- **Windows 10 21H2** or **Windows 11 (all supported versions)**
- **Professional, Enterprise**, or **Education** edition
- **Enrolled in Intune** with device-based enrollment (not user-based)
- **Microsoft 365 Apps** installed (for Office patching)
- **Adequate disk space** (typically 10GB free)

> **Tenant** requirements:
- **Intune Premium** licensing or bundled licenses (Microsoft 365 E3/E5, etc.)
- **Microsoft 365 Apps** in your environment (Autopatch coordinates both Windows and Office updates)

Enable in Intune : **Tenant Administration** > **Windows Autopatch**