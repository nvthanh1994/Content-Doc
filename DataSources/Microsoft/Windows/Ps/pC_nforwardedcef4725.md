#### Parser Content
```Java
{
Name = n-forwarded-cef-4725
    Vendor = Microsoft
    Product = Windows
    Lms = NitroCefSyslog
    DataType = "windows-account-disabled"
    TimeFormat = "epoch"
    Conditions = [ "|McAfee|ESM", "43-26304725"]
    Fields = [ """\|McAfee\|[^|]{1,2000}?\|[^|]{1,2000}?\|43-2630({event_code}\d{1,100})(0|1)\|""",
      """({event_name}A user account was disabled)""",
      """\srt=({time}\d{1,100})""",
      """shost=({host}[^\s]{1,2000})""",
      """sntdom=({domain}[^\s]{1,2000})""",
      """suser=({user}.+?)\s{1,100}\w+=""",
      """duser=({target_user}.+?)\s{1,100}\w+=""",
      """nitroSource_Logon_ID=({logon_id}[^\s]{1,2000})""",
      """nitroSecurity_ID=({user_sid}[^\s]{1,2000})"""
    ]
    DupFields=[ "host->dest_host" ]
  }
```