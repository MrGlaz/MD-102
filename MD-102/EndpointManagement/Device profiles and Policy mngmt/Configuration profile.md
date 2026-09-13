
> **Device configuration profiles** = the settings you push
> **Compliance policies** = the check that verifies them.

- A profile is a **template of settings** (BitLocker, password complexity, Wi-Fi config, etc.) you build once and **assign to devices or user groups**.

- On enrollment (or whenever assigned), the device **pulls and auto-applies** those settings — no manual config needed.

- **Proactive, not reactive**: profiles _configure_ the device to be a certain way; compliance policies just _check_ whether it already is that way. They're independent mechanisms — one does the work, the other grades it.


* **Device profiles**
Tied to the _device_; Wi-Fi, VPN, camera/Bluetooth, encryption; same settings for any user on that device.

* **User profiles**
Tied to the _user_; email, app settings, restrictions; follows the user across every device they sign into.

* **Administrative templates**
Group Policy-style settings for Windows, cloud-delivered; no on-prem infra needed; covers hundreds of advanced settings.

* **Custom profiles**
For settings not in standard profile types; built via OMA-URI or Plist; requires technical expertise, last resort only.


Filters use device properties like:
- **Device manufacturer** (Dell, HP, Lenovo, Apple)
- **Device model** (Surface Pro, MacBook Pro, iPad)
- **OS** (Windows 10 21H2, Windows 11 23H2)
- **Device ownership** (Corporate, Personal)
- **Device category** (custom tags you assign)


