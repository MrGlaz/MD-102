Onboard devices to xxx MS product (ex : Defender for Endpoint)
* **[[Delivery Optimization]]** template >> reduces bandwidth consumption when devices download applications and updates.
* Configure OS updates, and use DDM (Declarative Device Management) with a target OS version and time to enforce the update by a defined deadline

Can be configured to delay the visibility of software updates for up to 90 days.

> **Device configuration require MDM enroll / no enroll = no profile, regardless of assignment
 
- Proactively **pushes settings** to devices (Wi-Fi, VPN, restrictions, certs, security settings) — configures, doesn't just check (that's compliance policies)
- **Platform-specific** — one profile = one platform (Windows, iOS, Android, macOS); can't mix
- **Profile types**: Settings Catalog (modern, most flexible), Templates (pre-built), Administrative templates (GPO-style, Windows-only), Custom (OMA-URI/Plist, last resort)
- Assigned to **groups** (user or device) = can narrow with **filters**
- Status tracked **per-device and per-setting** in reports
- **Scope tags** control which admins can see/manage the profile (RBAC)


> **Unenrolled devices**

- Device config profiles **cannot** apply — there's no MDM channel to deliver them
- BYOD/unmanaged devices instead get **App Protection Policies** or **App Configuration Policies** (app-level, not device-level) — different mechanism entirely
- **Entra registered ≠ Intune enrolled** — a device can be registered in Entra ID (light BYOD touch) without being MDM-enrolled; profiles still won't apply