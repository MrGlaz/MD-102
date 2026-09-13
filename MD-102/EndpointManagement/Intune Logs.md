Review the client logs when you need to identify the exact failure point. The Intune Management Extension stores app-related logs under `C:\ProgramData\Microsoft\IntuneManagementExtension\Logs`. These logs show policy processing, app workload activity, detection checks, applicability checks, and script execution.


`IntuneManagementExtension.log` = Agent check-in, policy request, policy processing, and reporting activity.

`AppWorkload.log` = App check-ins, app install attempts, applicability, and detection logging.

`AppActionProcessor.log` = Detection and applicability checks for app actions.

`AgentExecutor.log` =  PowerShell script execution details.

