#### Parser Content
```Java
{
Name = s-dropbox-logins-activity
    Vendor = Dropbox
    Product = Dropbox
    Lms = Splunk
    DataType = "app-login"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """"event_category": "logins"""", """"info_dict":""", """"event_type_description":""" ]
    Fields = [
      """exabeam_host=([^=]{1,2000}@\s{0,100})?({host}[\w\-.]{1,2000})""",
      """"name":\s{0,100}"(?:N\/A|({user_fullname}[^"@,]{1,2000}))"""",
      """"name":\s{0,100}"(?:N\/A|(({domain}[^"@\\\s]{1,2000})\\+)?({user}[^"@\\\s]{1,2000}))"""",
      """"email":\s{0,100}"(?:N\/A|({user_email}[^@"\s]{1,2000}@[^@"\s]{1,2000}))""",
      """"time":\s{0,100}"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\d:+-]{1,2000})"""",
      """"event_type":\s{0,100}"({activity}[^"]{1,2000})"""",
      """"event_type_description":\s{0,100}"({additional_info}[^"]{1,2000})"""",
      """"ip_address":\s{0,100}"({src_ip}[a-fA-F\d.:]{1,2000})""",
      """"display_name":\s{0,100}"({user_agent}[^"]{1,2000})"""",
      """"display_name":\s{0,100}"Mozilla[^"]{0,2000}?({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)[^"]{0,2000}?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident)""",
    ]
  }
```