
Collects telemetry from enrolled Windows devices automatically once you enable data collection. This telemetry includes :
- application launch times
- crash frequency
- Startup impact scores
- resource consumption patterns.

> Intune > Reports > Endpoint Analytics

Requirements :
* Basic Intune licence
- Run Windows 11 or Windows 10 Pro, Enterprise, or Education editions.
- Devices must be enrolled in Intune or co-managed with Configuration Manager.
- (BYOD = more MAM than MDM so no data with Endpoint Analytics)

> Intune Advanced Analytics = Intune Suite or Intune Plan 2


Permission roles for viewing reports :
- Help Desk Operator
- Read Only Operator
- Endpoint Security Manager

Analytics can integrate with Azure Monitor for advanced scenarios (using Kusto Query Language)

> Compare metrics before and after remediation quantitatively.


> To activate Endpoint Advanced Analytics features
* Integrating Defender for Endpoint with Intune and onboarding devices enables Advanced Analytics features, such as Anomalies and Device timeline, to collect and display security and behavioral data.