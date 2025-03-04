Vendor: Oracle
==============
### Product: [Public Cloud](../ds_oracle_public_cloud.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|   3   |   2    |     2      |      1      |    1    |

| Event Type         | Rules                                                                                                                                                                                                                                                                                               | Models                                                                                                                                                                 |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| netflow-connection | <b>T1046 - Network Service Scanning</b><br> ↳ <b>NETFLOW-OsH-SweepScan-A</b>: Abnormal for asset to access 20 assets in 10 seconds<br><br><b>T1021 - Remote Services</b><br> ↳ <b>A-RLA-AA-F</b>: First asset-to-asset communication<br> ↳ <b>A-RLA-AA-A</b>: Abnormal asset-to-asset communication |  • <b>A-NETFLOW-OsH-Scanners</b>: Assets that access multiple assets within seconds in the organization<br> • <b>A-RLA-AA</b>: Asset to asset communication (DISABLED) |