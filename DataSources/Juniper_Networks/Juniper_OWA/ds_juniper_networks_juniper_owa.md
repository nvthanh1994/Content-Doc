Vendor: Juniper Networks
========================
Product: Juniper OWA
--------------------
| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|  27   |   14   |     3      |      1      |    1    |

|    Use-Case    | Event Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  app-login<br> ↳[juniper-owa](Ps/pC_juniperowa.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br> | [<ul><li>16 Rules</li></ul><ul><li>11 Models</li></ul>](RM/r_m_juniper_networks_juniper_owa_Abnormal_Authentication_&_Access.md) |
|          [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md)          |  app-login<br> ↳[juniper-owa](Ps/pC_juniperowa.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br> | [<ul><li>7 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_juniper_networks_juniper_owa_Compromised_Credentials.md)    |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  app-login<br> ↳[juniper-owa](Ps/pC_juniperowa.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>4 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_juniper_networks_juniper_owa_Data_Access.md)    |
|    [Evasion](../../../UseCases/uc_evasion.md)    |  app-login<br> ↳[juniper-owa](Ps/pC_juniperowa.md)<br> | T1090.003 - Proxy: Multi-hop Proxy<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_juniper_networks_juniper_owa_Evasion.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  app-login<br> ↳[juniper-owa](Ps/pC_juniperowa.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_juniper_networks_juniper_owa_Malware.md)    |
|    [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)    |  app-login<br> ↳[juniper-owa](Ps/pC_juniperowa.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_juniper_networks_juniper_owa_Privilege_Abuse.md)    |
|    [Privileged Activity](../../../UseCases/uc_privileged_activity.md)    |  app-login<br> ↳[juniper-owa](Ps/pC_juniperowa.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_juniper_networks_juniper_owa_Privileged_Activity.md)    |
|    [Ransomware](../../../UseCases/uc_ransomware.md)    |  app-login<br> ↳[juniper-owa](Ps/pC_juniperowa.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_juniper_networks_juniper_owa_Ransomware.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                   | Execution | Persistence                                                                                                                                      | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |