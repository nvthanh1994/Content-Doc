#### Parser Content
```Java
{
Name = json-4729
  DataType = "windows-member-removed"
  Conditions = [ """Security ID:""", """Logon ID:""", """A member was removed from a security-enabled""", """raw""", """event_id\":4729""", """computer_name""" ]
  Fields = ${WinParserTemplates.json-windows-events-2.Fields}[
    """({event_name}A member was removed from a security-enabled [\w\s]{1,2000} group)""",
    """A member was removed from a security-enabled\s{0,100}({group_type}[^\s]{1,2000})\s{1,100}group""",
    """MemberSid\\?"{1,20}:\\?"{1,20}({account_id}[^\\]{1,2000})\\?"""",
    """MemberName\\?"{1,20}:\\?"{1,20}({account_dn}CN=.+?,({account_ou}OU.+?DC=[\w-\\]{1,2000}?))\\?"""",
    """TargetSid\\?"{1,20}:\\?"{1,20}({group_id}[^\\]{1,2000})\\?"""",
    """TargetUserName\\?"{1,20}:\\?"{1,20}({group_name}[^\\]{1,2000})\\?"""",
    """TargetDomainName\\?"{1,20}:\\?"{1,20}({group_domain}[^\\]{1,2000})\\?""""
  ]
  DupFields = [ "host->dest_host" ]
}
json-windows-events-2 = {
  Vendor = Microsoft
  Product = Windows
  Lms = Direct
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """@timestamp\\?"{1,20}:\\?"{1,20}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,100}Z)""",
    """(?:winlog\.)?computer_name\\?"{1,20}:\\?"{1,20}({host}[^\\]{1,2000})""",
    """SubjectUserName\\?"{1,20}:\\?"{1,20}(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[^\\]{1,2000}))\\?"""",
    """SubjectUserSid\\?"{1,20}:\\?"{1,20}({user_sid}[^\\]{1,2000})\\?"""",
    """SubjectDomainName\\?"{1,20}:\\?"{1,20}(|-|NT Service|NT AUTHORITY|({domain}[^\\]{1,2000}))\\?"""",
    """SubjectLogonId\\?"{1,20}:\\?"{1,20}({logon_id}[^\\]{1,2000})\\?"""",
    """event_id\\?"{1,20}:({event_code}\d{1,100})""",
    """ProcessName\\?"{1,20}:\\?"{1,20}(?:|-|({process}({directory}(?:[^";]{1,2000})?[\\\/])?({process_name}[^\\\/":;\s]{1,2000}?)))\\?"""",
    """WorkstationName\\?"{1,20}:\\?"{1,20}(?:-|({src_host_windows}[^\s\\]{1,2000}))\\?"""",
    """Status\\?"{1,20}:\\?"{1,20}({result_code}[^\\]{1,2000})\\?"""",
    """ProcessId\\?"{1,20}:\\?"{1,20}({process_id}[^:\\]{1,2000}?)\\?"""",
    """LogonProcessName\\?"{1,20}:\\?"{1,20}({auth_process}[^\s\\]{1,2000})\s{0,100}\\?"""",
    """AuthenticationPackageName\\?"{1,20}:\\?"{1,20}({auth_package}[^\s\\]{1,2000})\\?""""
  ]

```