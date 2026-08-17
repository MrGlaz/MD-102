- Maintain on-premises Active Directory infrastructure
- Need gradual migration to cloud identity
- Require access to both traditional and modern resources
- Need AD on prem + Entra Connect Sync


**GPO trigger (critical for hybrid-joined PCs)** — Group Policy: _Computer Config > Admin Templates > Windows Components > MDM > "Enable automatic MDM enrollment using default Azure AD credentials"_ must be enabled. Without this, hybrid-joined devices won't auto-enroll.

