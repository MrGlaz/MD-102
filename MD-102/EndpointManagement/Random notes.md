
**Policy for Office Apps** = configure feedback settings + privacy controls

**App Configuration Policy** = iOS/iPadOS (regardless enrolled or not)

**Configuration profiles** and **Compliance policies** require a device to be managed by Intune.

**Device configuration profile** = onboard devices to xxx MS product (ex : Defender for Endpoint)
* **Delivery Optimization** template >> reduces bandwidth consumption when devices download applications and updates.
* Configure OS updates, and use DDM (Declarative Device Management) with a target OS version and time to enforce the update by a defined deadline

**App Protection policies** = secure apps managed/unmanaged devices but do not allow configuration
- prevent saving company data to personal storage location
- restrict copy-and-paste functions

**Data Protection** setting has option to prevent printing of organizational data (set to block, default is allowed).

**Access requirement** = device access : pin, biometrics and credentials.

Security baselines = set up base line rules for security (do not enroll devices)

**Conditional launch** = device and OS settings.
**Conditional Access** = access controls to the data.

Line of Business (LOB) app

VPN solution = secures communications

Microsoft Defender = endpoint security (not apps or data)

Notion de : directly address app-level data protection

**Compte DEM (Device Enrollement Manager)** = enroll up to 1000 devices with 1 account, up to 150 DEM accounts per tenant

Feature update policy = allows to upgrade to W11


**Device configuration profile**: applies general settings to devices (Wi-Fi, VPN, restrictions, certificates, etc.), not update-related at all.

**Feature update profile**: controls which Windows _version_ (e.g., 23H2 → 24H2) devices are allowed to upgrade to and when. Cannot be postponed.

**Quality update policy**: controls the rollout timing of monthly cumulative/security patches for an already-installed Windows version.

**Update ring policy**: an older, all-in-one policy that controls both feature and quality update deferral/scheduling together for a group of devices (the predecessor to splitting it into the two policies above). Allow to postpone update

**Windows feature update device readiness report** = shows devices with statuses

**Windows feature update device comptaiblity risks report** = about apps or drivers

Endpoint Analytics to generate a hardware readiness report (for compability)