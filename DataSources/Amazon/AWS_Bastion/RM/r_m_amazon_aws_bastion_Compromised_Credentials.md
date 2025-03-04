Vendor: Amazon
==============
### Product: [AWS Bastion](../ds_amazon_aws_bastion.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|   6   |   2    |     3      |      2      |    2    |

| Event Type   | Rules                                                                                                                                                                                                                                                                                                                                                               | Models                                                      |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| failed-logon | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-04</b>: Failed logon by a service account<br> ↳ <b>SEQ-UH-05</b>: Failed interactive logon by a service account                                                                                                                                                                                                       |  • <b>AE-UA</b>: All activity for users                     |
| remote-logon | <b>T1078 - Valid Accounts</b><b>T1133 - External Remote Services</b><br> ↳ <b>UA-UC-Suspicious</b>: Activity from suspicious country<br> ↳ <b>UA-UC-Two</b>: Activity from two different countries<br><br><b>T1021 - Remote Services</b><br> ↳ <b>A-RLA-AA-F</b>: First asset-to-asset communication<br> ↳ <b>A-RLA-AA-A</b>: Abnormal asset-to-asset communication |  • <b>A-RLA-AA</b>: Asset to asset communication (DISABLED) |