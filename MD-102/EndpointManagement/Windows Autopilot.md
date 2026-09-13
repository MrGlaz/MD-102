
> Windows Autopilot requires the hardware ID of each machine to be uploaded before the machine can be used with Autopilot.

>> For a device to pull down its Autopilot deployment profile during OOBE, it first has to be **registered** in the Autopilot service — meaning its hardware hash was collected and imported into the tenant (via OEM registration, reseller, or `Get-WindowsAutopilotInfo`).

* User-driven = user credentials are required to enroll the device (device has a primary user)
* Self-deploy = only compliance policies targeting the device are applied (no primary user - shared device)

Scenarios
![[deployment scenarios.png]]

1. Connect device to the internet
2. Sign in with org acount
3. Device auto joins Entra ID and enrolls the device


Type of device enrollements :

| Scenario                         | Join Type                   | User Interaction                  | Key Requirement                                        | Notes                                                                          |
| -------------------------------- | --------------------------- | --------------------------------- | ------------------------------------------------------ | ------------------------------------------------------------------------------ |
| **User-driven**                  | Entra (preferred) or Hybrid | Full OOBE setup by user           | Device registered + profile assigned + MDM auto-enroll | Hybrid needs Intune Connector for AD + on-prem access                          |
| **Self-deploying**               | Entra only                  | None (or minimal for Wi-Fi)       | TPM 2.0 + attestation                                  | Ends at sign-in screen; kiosk-friendly ; zero-touch ; shared screens (no user) |
| **Autopilot Device preparation** | Entra only                  | Minimal                           | Win11 only, no hardware hash needed                    | Uses Enrollment Time Grouping                                                  |
| **Existing devices**             | Entra or Hybrid             | Runs at next OOBE                 | Reimage + Autopilot config file (e.g. ConfigMgr)       | Converts old devices to modern mgmt                                            |
| **Pre-provisioned**              | Entra or Hybrid             | User finishes final settings only | TPM 2.0 + attestation, no VMs                          | IT preps apps/policies in advance                                              |
| **Autopilot Reset**              | Entra only                  | None (wipe + reapply config)      | N/A                                                    | Keeps Entra ID + Intune enrollment                                             |


> Feature update deferral limit : 365 days
> Quality (security) update deferral : 30 days

[[Endpoint security]] > Disk encryption policy type is purpose-built for BitLocker (and FileVault on macOS), including silent encryption enforcement and automatic recovery key escrow to Azure AD.

[[Conditional Access]] to block app access/exposure of non-compliant devices

[[App protection policies]] (MAM) apply data-loss-prevention controls — like blocking cut/copy/paste and 'save as' into unmanaged apps — directly to the app, so they work even on personal, unenrolled devices.


>The process for configuring a pre-provisioned deployment is as follows:

1. Enable the **Allow pre-provisioned deployment** option in the desired Autopilot profile.
2. Start the device and allow it to enter the Windows out-of-box experience (OOBE).
3. At the first OOBE screen, press the Windows key five times to open the Autopilot provisioning workflow.
4. In the additional dialog options, select **Windows Autopilot provisioning**.
5. Verify the device information.
6. Select **Provision** to begin provisioning the device.
7. When the process is complete, select **Reseal**.

After the device receives its Autopilot profile, configuration information is stored in the device registry at `HKLM\SOFTWARE\Microsoft\Provisioning\Diagnostics\Autopilot`


Get diagnostics with PS :
`Set-ExecutionPolicy Bypass` 
`Install-Script Get-AutopilotDiagnostics -Force`
`Get-AutopilotDiagnostics -Online`

