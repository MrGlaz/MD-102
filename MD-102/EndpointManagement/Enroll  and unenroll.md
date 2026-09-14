
**Bucket 1 : needs the device MDM-enrolled, full stop (ownership irrelevant):**

- ==Device configuration profiles ==(Settings Catalog, ADMX, Wi-Fi/VPN/cert profiles, restrictions)
- ==Device compliance policies== — and any Conditional Access grant control of "require device marked compliant"
- ==Endpoint security== (antivirus, disk encryption/BitLocker, firewall, ASR, EDR onboarding, App Control for Business)
- Windows Hello for Business, Windows LAPS, Endpoint Privilege Management
- Remote device actions: wipe, retire, restart, sync, locate, rotate BitLocker key, rotate LAPS password
- Certificate profiles (SCEP/PKCS)
- Enrollment restrictions (they gate the enrollment attempt itself)
- ==Windows Autopilot== (it _is_ the enrollment path)

**Bucket 2 : works on an unenrolled device, because it's app-layer (MAM), not device-layer:**

- ==App protection policies== — DLP controls (cut/copy/paste, save-as) and Conditional Launch (PIN, jailbreak/root block, min OS version)
- ==App configuration policies==, but only the "managed apps" flavor — the "managed devices" flavor of app config still needs enrollment
- ==Conditional Access grant controls==: "require app protection policy" or "require approved client app" — these are the CA controls that _don't_ imply enrollment
- A selective wipe of just the managed app's corporate data via the app protection policy — different tool from device Retire/Wipe, and it's the answer when a question wants data removed from a device that was never enrolled
- ==Microsoft Tunnel for MAM== — extends VPN access to MAM-only apps on unenrolled devices