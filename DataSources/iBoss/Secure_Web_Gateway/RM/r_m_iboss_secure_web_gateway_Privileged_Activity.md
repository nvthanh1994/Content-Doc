Vendor: iBoss
=============
### Product: [Secure Web Gateway](../ds_iboss_secure_web_gateway.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|   1   |   0    |     2      |      2      |    2    |

| Event Type           | Rules                                                                                                                                                   | Models |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| web-activity-allowed | <b>T1071.001 - Application Layer Protocol: Web Protocols</b><b>T1102 - Web Service</b><br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller |        |
| web-activity-denied  | <b>T1071.001 - Application Layer Protocol: Web Protocols</b><b>T1102 - Web Service</b><br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller |        |