Vendor: Microsoft
=================
### Product: [Network Policy Server](../ds_microsoft_network_policy_server.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|   4   |   3    |     2      |      2      |    2    |

| Event Type | Rules                                                                                                                                                                                                                                                                                                               | Models                                                                                                                                                |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| nac-logon  | <b>T1021 - Remote Services</b><br> ↳ <b>NAC-GAt-A</b>: Abnormal authentication type for peer group<br> ↳ <b>NAC-UAt-F</b>: First authentication type for user<br> ↳ <b>NAC-UAt-A</b>: Abnormal authentication type for user<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>AE-UA-F</b>: First activity type for user |  • <b>NAC-UAt</b>: Authentication Types for user<br> • <b>NAC-GAt</b>: Authentication Types for peer group<br> • <b>AE-UA</b>: All activity for users |