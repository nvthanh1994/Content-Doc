#### Parser Content
```Java
{
Name = cef-snare-576
  Vendor = Microsoft
  Product = Windows
  Lms = ArcSight
  DataType = "windows-privileged-access"
  TimeFormat = "epoch"
  Conditions = [ """|Snare|""","""|Security:576|""" ]
  Fields = [
    """({event_name}Special privileges assigned to new logon)""",
    """({event_code}576)""",
    """\srt=({time}\d{1,100})""",
    """\ssuser=({user}.+?)\s{1,100}\w+=""",
    """\sduid=\([^,]{1,2000}
```