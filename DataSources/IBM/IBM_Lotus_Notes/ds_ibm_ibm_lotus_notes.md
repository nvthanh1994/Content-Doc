Vendor: IBM
===========
Product: IBM Lotus Notes
------------------------
| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|  20   |   14   |     4      |      2      |    2    |

|    Use-Case    | Event Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
|     [Cryptomining](../../../UseCases/uc_cryptomining.md)     |  database-update<br> ↳[ibm-lotus-database-update](Ps/pC_ibmlotusdatabaseupdate.md)<br><br> network-connection-successful<br> ↳[ibm-lotus-network-connection](Ps/pC_ibmlotusnetworkconnection.md)<br> | T1496 - Resource Hijacking<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_ibm_ibm_lotus_notes_Cryptomining.md)    |
| [Lateral Movement](../../../UseCases/uc_lateral_movement.md) |  database-update<br> ↳[ibm-lotus-database-update](Ps/pC_ibmlotusdatabaseupdate.md)<br><br> network-connection-successful<br> ↳[ibm-lotus-network-connection](Ps/pC_ibmlotusnetworkconnection.md)<br> | T1071 - Application Layer Protocol<br>T1090.002 - Proxy: External Proxy<br>T1571 - Non-Standard Port<br> | [<ul><li>18 Rules</li></ul><ul><li>14 Models</li></ul>](RM/r_m_ibm_ibm_lotus_notes_Lateral_Movement.md) |
|       [Ransomware](../../../UseCases/uc_ransomware.md)       |  database-update<br> ↳[ibm-lotus-database-update](Ps/pC_ibmlotusdatabaseupdate.md)<br><br> network-connection-successful<br> ↳[ibm-lotus-network-connection](Ps/pC_ibmlotusnetworkconnection.md)<br> | T1071 - Application Layer Protocol<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_ibm_ibm_lotus_notes_Ransomware.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                                                                                                                                                                           | Exfiltration | Impact                                                                  |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ----------------------------------------------------------------------- |
|                |           |             |                      |                 |                   |           |                  |            | [Non-Standard Port](https://attack.mitre.org/techniques/T1571)<br><br>[Proxy: External Proxy](https://attack.mitre.org/techniques/T1090/002)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              | [Resource Hijacking](https://attack.mitre.org/techniques/T1496)<br><br> |