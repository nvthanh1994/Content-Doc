#### Parser Content
```Java
{
Name = O365-email-alert-out
  Conditions = [ """"activity_type":"Send"""" ]
  Fields = ${MSParserTemplates.O365-email-alert.Fields} [
    """"user":"({sender}[^"\s@]{1,2000}@[^"\s@]{1,2000})""",
    """"user":"({external_address}[^"\s@;,]{1,2000}@({external_domain}[^"\s@;,]{1,2000}))""",
  ]
}
O365-email-alert = {
  Vendor = Microsoft
  Product = Office 365
  Lms = Direct
  DataType = "dlp-email-alert"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """exabeam_host=([^=]{1,2000}@\s{0,100})?({host}\S+)""",
    """"_time":"({time}\d{1,100}-\d{1,100}-\d{1,100}T\d{1,100}:\d{1,100}:\d{1,100}\.\d{1,100}[\+\-]\d{1,100})""",
    """"name":"({subject}[^"]{1,2000}?)\s{0,100}"""",
    """"activity_type":"({activity}Receive|Send)""",
    """"user":"({user_email}[^"\s@]{1,2000}@[^"\s@]{1,2000})""",
    """"user_name":"({user_fullname}[^"\s]{1,2000}\s{1,100}[^"]{1,2000})""",
    """"message":"({additional_info}.+?)\s{0,100}",""",
    """"(internal|external)_recipients":"({recipients}({recipient}[^"\s@;,]{1,2000}@[^"\s@;,]{1,2000})[^"]{0,2000})"""",
    """ from ({sender}[^"\s@]{1,2000}@[^"\s@]{1,2000})""",
  ]

```