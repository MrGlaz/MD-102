
> **Group Policy analytics**:
- Intune admin center tool: analyzes on-prem GPOs → shows what migrates to cloud (Intune) configuration profiles
- Works by uploading **GPO backup files** exported from AD (via GPMC) → compared against Intune-supported settings database

> **Three migration categories:**
1. **Supported** = direct Intune equivalent, full feature parity → migrate first (quick wins)
2. **Partially supported** = cloud equivalent exists but with limitations (fewer capabilities) → requires judgment call: accept gap or find alternative
3. **Not supported** = no cloud equivalent (deprecated/on-prem-only) → options: custom profile (OMA-URI), alternative solution, or accept it won't apply

> **Migration strategy:**
- Phase migration: critical security settings first → business-critical w/ workarounds next → low-priority/redesign last
- Avoids high-risk all-at-once cutover
- Also useful for stakeholder communication (data-driven justification for changes)
- Purpose: full visibility before migrating → no missed/lost policies, informed decisions on gaps