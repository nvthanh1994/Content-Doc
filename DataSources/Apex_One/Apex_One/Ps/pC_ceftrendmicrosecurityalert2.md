#### Parser Content
```Java
{
Name = cef-trendmicro-security-alert-2
  Product = Apex One
  Conditions = [ """CEF:""", """|Trend Micro|Apex Central|""" ]
  Fields = ${TrendMicroParserTemplates.cef-trendmicro-security-alert.Fields}[
    """\Wcs1=(?:N\/A|({alert_name}[^=]{1,2000}?))\s{1,100}\w+=""",
    """CEF:([^\|]{0,2000}\|){5}({alert_name}[^\|]{1,2000})\|(Unknown|({alert_severity}[^\|]{1,2000}))""",
    """cn2=({cn2}[^\s"]{1,2000})""",
  ]
  DupFields = [ "outcome->action", "alert_name->alert_type" ]
}
cef-trendmicro-security-alert = {
  Vendor = Trend Micro
  Lms = ArcSight
  DataType = "alert"
  TimeFormat = "MMM dd yyyy HH:mm:ss zZ"
  Fields = [
    """CEF:([^\|]{0,2000}\|){4}({alert_type}[^\|]{1,2000})\|({alert_name}[^\|]{1,2000})\|(Unknown|({alert_severity}[^\|]{1,2000}))""",
    """exabeam_time=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d{1,100}(\+|\-)\d\d:\d\d)""",
    """\WeventId=({alert_id}\d{1,100})""",
    """exabeam_host=({host}[\w.\-]{1,2000})""",
    """\Wdvc=({host}[^=]{1,2000}?)(\s{1,100}\w+=|\s{0,100}$|\s{0,100}")""",
    """\Wdvchost=({host}[^=]{1,2000}?)(\s{1,100}\w+=|\s{0,100}$|\s{0,100}")""",
    """rt=({time}\w+\s{1,100}\d\d \d\d\d\d \d\d:\d\d:\d\d \S+)""",
    """\sshost=(((\d{1,3}\.){3}\d{1,3}|({src_host}[\w\-.]{1,2000}))|({additional_info}[^@]{1,2000}@[^\s]{1,2000}))\s{1,100}\w+=""",
    """\sdhost=((\d{1,3}\.){3}\d{1,3}|({dest_host}[\w\-.]{1,2000}))\s{1,100}\w+=""",
    """\Wapp=({app}[^=]{1,2000}?)(\s{1,100}\w+=|\s{0,100}$|\s{0,100}")""",
    """\Wdst=(::|({dest_ip}[a-fA-F\d.:]{1,2000}))\s""",
    """\Wdpt=({dest_port}\d{1,100})""",
    """\Wsrc=(::|({src_ip}[a-fA-F\d.:]{1,2000}))\s""",
    """\Wspt=({src_port}\d{1,100})""",
    """\Wact=(Unknown|({outcome}[^=]{1,2000}?))(?:\s{1,100}\w+=|\s{0,100}$|\s{0,100}")""",
    """\Wcn3=({threat_type}[^=]{1,2000}?)(\s{1,100}\w+=|\s{0,100}$|\s{0,100}")""",
    """\Wrequest="{0,20}(|({malware_url}[^"]{1,2000}?))(\s{1,100}\w+=|\s{0,100}$|\s{0,100}"|”\]{1,2000}\s{1,100}\w+=)""",
    """\WdeviceProcessName=({process}({directory}[^=]{0,2000}?)({process_name}[^\/\\=]{1,2000}?))(\s{1,100}\w+=|\s{0,100}$|\s{0,100}")""",
    """\sduser=((\d{1,3}\.){3}\d{1,3}|({user_email}[^@\s]{1,2000}@[^\.\s]{1,2000}\.[^\s]{1,2000}?)|((({domain}[^\s\\\/=]{1,2000})[\\\/]{1,2000})?({user}[^\s]{1,2000}?)))(\s{1,100}\w+=|\s{0,100}$)""",
    """\sfilePath=({malware_url}[^=]{1,2000}?)(\s{1,100}\w+=|\s{0,100}$)""",
    """\sfileHash=({md5}\w+)(\s{1,100}\w+=|\s{0,100}$)"""
  ]

```