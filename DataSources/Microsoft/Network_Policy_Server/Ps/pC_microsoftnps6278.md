#### Parser Content
```Java
{
Name = microsoft-nps-6278
  Vendor = Microsoft
  Product = Network Policy Server 
  Lms = Direct
  DataType = "windows-nac-logon"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>6278</EventID>""", """<Message>Network Policy Server granted full access to a user""" ]
  Fields = [
    """SystemTime='({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """exabeam_host=([^=]{1,2000}@\s{0,100})?({host}[\w\-.]{1,2000})""",
    """<Computer>({host}[\w\-.]{1,2000})""",
    """({event_code}6278)""",
    """'SubjectUserName'>(?:({user_type}host)/)?(({domain}[^\\]{1,2000})\\+)?({user}[^<]{1,2000})""",
    """'SubjectDomainName'>(?:-|({domain}[^\s\<]{1,2000}))""",
    """'FullyQualifiedSubjectUserName'>(({domain}[^\\]{1,2000})\\+)?(?:-|({user}[^\s\\\<]{1,2000}))""",
    """'NASIdentifier'>(?:-|({location}[\w\-.]{1,2000}))""",
    """'CallingStationID'>(?:-|({src_mac}[^\<]{1,2000}))""",
    """'AuthenticationProvider'>(?:-|({auth_server}[^\<]{1,2000}))""",
    """'FullyQualifiedSubjectMachineName'>(?:-|({user_type}.+?))(\/[^\/\s]{1,2000})?<""",
    """'NASIPv6Address'>({dest_ip}[a-fA-F:\d.]{1,2000})""",
    """'NASIPv4Address'>({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """'EAPType'>(?:-|({auth_type}[^\<]{1,2000}))""",
    """'QuarantineState'>(?:-|({access_type}[^\<]{1,2000}))"""
  ]
}
```