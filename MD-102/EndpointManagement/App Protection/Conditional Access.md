Policies in Microsoft Entra ID enforce App Protection requirements at authentication time, preventing users from bypassing security by using native unmanaged mail or browser apps

- **Authentication Context** — tags specific _actions/resources_ (e.g., one SharePoint site, one sensitive app function) so CA policies can target that specific thing, not just the whole app

- **Continuous Access Evaluation (CAE)** — near real-time token revocation (user disabled, password changed, IP change) instead of waiting for token expiry

- **Grant Controls** — the _requirements to get in_: MFA, compliant device, hybrid join, approved app, or block

- **Session Controls** — the _restrictions once inside_: app-enforced limits, sign-in frequency, persistent session, Conditional Access App Control (via Defender for Cloud Apps)