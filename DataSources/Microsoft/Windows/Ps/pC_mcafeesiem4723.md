#### Parser Content
```Java
{
Name = mcafee-siem-4723
    Vendor = Microsoft
    Product = Windows
    Lms = Direct
    DataType = "windows-password-change"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """McAfee_SIEM:""", """An attempt was made to change an account's password.""" ]
    Fields = [
      """({event_name}An attempt was made to change an account's password)""",
      """"src_ip":"({src_ip}[^"]{1,2000})""",
      """"dst_ip":"({dest_ip}[^"]{1,2000})""",
      """"id":\d{0,100}({event_code}4723)""",
      """"firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """"DomainID":"({domain}[^"]{1,2000})""",
      """"HostID":"({host}[^"]{1,2000})""",
      """"UserIDSrc":"({user}[^"]{1,2000})""",
      """"Security_ID":"({user_sid}[^"]{1,2000})""",
      """"Source_Logon_ID":"({logon_id}[^"]{1,2000})""",
      """"UserIDDst":"({target_user}[^"]{1,2000})""",
      """"action":"({outcome}[^"]{1,2000})"""
    ]
    DupFields = [ "host->dest_host" ]
  }
```