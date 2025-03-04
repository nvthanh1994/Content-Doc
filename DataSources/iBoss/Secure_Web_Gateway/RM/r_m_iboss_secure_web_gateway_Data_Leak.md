Vendor: iBoss
=============
### Product: [Secure Web Gateway](../ds_iboss_secure_web_gateway.md)
### Use-Case: [Data Leak](../../../../UseCases/uc_data_leak.md)

| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|   4   |   1    |     3      |      2      |    2    |

| Event Type           | Rules                                                                                                                                                                                                                                                                                                                                                                        | Models                                                                     |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| web-activity-allowed | <b>T1030 - Data Transfer Size Limits</b><br> ↳ <b>A-WEB-EXFIL-ASSET</b>: Large amount of data exfiltrated from host<br> ↳ <b>WEB-New-File-20</b>: User with no web activity history has uploaded 20MB or more<br><br><b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-OUa-Browser-F</b>: First activity using this web browser for the organization |  • <b>WEB-OUa-Browser</b>: Top web browsers being used in the organization |
| web-activity-denied  | <b>T1030 - Data Transfer Size Limits</b><br> ↳ <b>New-File-20-Block</b>: User with no web activity history was blocked from uploading 20MB or more                                                                                                                                                                                                                           |                                                                            |