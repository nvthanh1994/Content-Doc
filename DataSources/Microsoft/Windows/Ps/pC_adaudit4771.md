#### Parser Content
```Java
{
Name = ad-audit-4771
  Vendor = Microsoft
  Product = Windows
  Lms = Direct
  DataType = "windows-4771"
  TimeFormat = "epoch_sec"
  Conditions = [ """ADAuditPlus""", """EVENT_NUMBER = 4771""", """Kerberos pre-authentication failed""" ]
  Fields = [
    """exabeam_host=([^=]{1,2000}@\s{0,100})?({host}[\w\-.]{1,2000})""",
    """TIME_GENERATED\s{0,100}=\s{0,100}({time}\d{1,100})""",
    """({host}[\w\-.]{1,2000}) ADAuditPlus""",
    """USERNAME\s{0,100}=\s{0,100}({user}[^\s\]]{1,2000})""",
    """CLIENT_IP_ADDRESS\s{0,100}=\s{0,100}({dest_ip}[A-Fa-f:\d.]{1,2000})""",
    """CLIENT_HOST_NAME\s{0,100}=\s{0,100}({dest_host}[^\]]{1,2000}?)\s{0,100}\]""",
    """DOMAIN\s{0,100}=\s{0,100}([^\/]{1,2000}\/)?({domain}[^\\\/]{1,2000}?)\s{0,100}\]""",
    """SOURCE\s{0,100}=\s{0,100}({src_host}[\w\-.]{1,2000})""",
    """RECORD_NUMBER\s{0,100}=\s{0,100}({record_id}\d{1,100})""",
    """EVENT_NUMBER\s{0,100}=\s{0,100}({event_code}\d{1,100})""",
    """USER_SID\s{0,100}=\s{0,100}\%\{({user_sid}[^\}]{1,2000})""",
    """ERROR_CODE\s{0,100}=\s{0,100}({result_code}[^\s]{1,2000})""",
    """EVENT_TYPE_TEXT\s{0,100}=\s{0,100}({outcome}.+?)\s{0,100}\]""",
  ]
}
```