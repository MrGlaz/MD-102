Only Windows, doesn't work on Android, iOS

> A Remediations script package :
- A detection script (checks for a problem)
- An optional remediation script (fixes the problem)
- Metadata (name, description, settings, assignments)

> Requirements
* Entra joined of hybrid joined
* MDM enrolled, running Windows Enterprise, Pro, Edu
* Co-managed Win devices

> Licensing
* Starting from E3

> Update rings vs Feature update policies
- **Update rings** → control **_when + how_** updates install: timing, restart behavior, user notifications, deferral periods
- **Feature update policies** → control **_what + which_** Windows version devices get
- Used **together**, not separately = one governs the mechanics, the other governs the target OS version → combined = full control over deployment strategy


- **Update rings enable staged deployment**: Pilot, standard, and conservative rings allow time to validate updates before risks affect your entire organization. Deferral periods balance security with stability.

- **Quality updates deploy faster than feature updates**: Security updates should deploy with minimal deferral (0-7 days), while feature updates benefit from longer testing and higher deferral periods (30-90 days).

![[remediation.png]]