Vendor: Web Application Firewall
================================
### Product: [Web Application Firewall](../ds_web_application_firewall_web_application_firewall.md)
### Use-Case: [Phishing](../../../../UseCases/uc_phishing.md)

| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|   2   |   2    |     1      |      9      |    9    |

| Event Type | Rules                                                                                                                                         | Models                                                                                                  |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| vpn-logout | <b>T1566 - Phishing</b><br> ↳ <b>EM-FNum-in</b>: Abnormal number of incoming emails<br> ↳ <b>EM-BSum-in</b>: Abnormal size of incoming emails |  • <b>EM-BSum-in</b>: Sum of bytes in incoming emails<br> • <b>EM-FNum-in</b>: Count of incoming emails |