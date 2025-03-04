#### Parser Content
```Java
{
Name = cef-vectra-alert
  Vendor = Vectra
  Product = Vectra Cognito Detect
  Lms = ArcSight
  DataType = "alert"
  TimeFormat = "epoch"
  Conditions = [ """|Vectra Networks|X Series|""" ]
  Fields = [
    """\Wrt=({time}\d{1,100})""",
    """\Wstart=({time}\d{1,100})""",
    """\Wdvc=({host}[\w\-.]{1,2000})""",
    """\Wdvchost=({host}[\w\-.]{1,2000})""",	
    """CEF:([^|]{0,2000}\|){4}({alert_type}[^|]{1,2000})""",
    """CEF:([^|]{0,2000}\|){5}({alert_name}[^|]{1,2000})""",
    """\Wcat=({category}[^=]{1,2000}?)\s{0,100}(\w{1,200}=|$)""",
    """\Wshost=({src_host}[\w\-.]{1,2000})\s""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]{1,2000})""",
    """\Wdst=({dest_ip}[a-fA-F\d.:]{1,2000})""",
    """\WexternalId=({alert_id}[^=]{1,2000}?)\s{0,100}(\w{1,200}=|$)""",
    """\WflexNumber2=({certainity}[^=]{1,2000}?)\s{0,100}(\w+=|$)""",
    """\WflexNumber1=({threat_id}[^=]{1,2000}?)\s{0,100}(\w{1,200}=|$)""",
    """saccount=(\w{1,2000}:)?(({user_email}[^@=]{1,2000}?@[^.]{1,2000}\.[^\s]{1,2000})|({account}[^=]{1,2000}?))\s{0,100}\s{0,100}(\w{1,100}=|$)""",
    """\scs4=({additional_info}[^|]{1,2000}?)\s\w{1,2000}="""
 ]
}
```