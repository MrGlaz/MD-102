The rule that decides which setting wins when multiple policies touch the same thing.

**Cross-policy-type rules:**
- **Compliance policy settings > Configuration profile settings**
- **Endpoint Security policies > (legacy) Device Configuration profiles**


**MAM / App Protection policies :**
- Deployed **first** = wins, stays applied
- Second one = shows as conflicting
- If both land **simultaneously** → most **restrictive** value wins

**GPO vs Intune (hybrid-joined devices) — classic exam trap:**

- **Group Policy wins by default**, even if Intune is also managing the device
- To flip it: enable **MDMWinsOverGP** (a Policy CSP setting) → forces Intune to override GPO for that setting
- Only applies to settings in the **Policy CSP** — not a blanket override for everything


> Compliance > Config.
> Endpoint Security > old Config.
> Config vs Config = conflict, not precedence.
> GPO > Intune unless you flip MDMWinsOverGP.