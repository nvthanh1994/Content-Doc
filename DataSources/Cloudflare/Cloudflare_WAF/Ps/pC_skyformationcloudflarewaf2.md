#### Parser Content
```Java
{
Name = skyformation-cloudflare-waf-2
  Vendor = Cloudflare
  Product = Cloudflare WAF
  Lms = Direct
  DataType = "web-activity"
  IsHVF = true
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName=Cloudflare""", """"clientIP":"""", """"source":""", """"clientRequestHTTPMethodName":"""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s{1,100}[^\s]{1,2000}\s{1,100}Skyformation""",
    """exabeam_host=([^=]{1,2000}@\s{0,100})?({host}\S+)""",
    """"ClientDeviceType":"({device_type}[^"]{1,2000})""",
    """"clientCountryName":"({src_country}[^"]{1,2000})""",
    """"clientIP":"(?:["]{1,2000}|({src_ip}[A-Fa-f:\d.]{1,2000}))""",
    """"userAgent":"({user_agent}[^"]{1,2000})""",
    """"edgeResponseStatus":({result_code}({edge_response_status}\d\d\d))""",
    """"originResponseStatus":({result_code}({origin_response_status}\d\d\d))"""
    """"clientRequestHTTPMethodName":"({method}[^"]{1,2000})""",
    """"action":"({action}[^"]{1,2000})""",
    """"ClientRequestReferer":"({referrer}[^"]{1,2000}?)",""",
    """"clientRequestHTTPHost":"({web_domain}[^"<,]{1,2000})""",
    """"clientRequestHTTPHost"{1,20}:"{1,20}[^\s"?=]{0,2000}?({top_domain}(?!(?:\d{1,100}\.){3}\d{1,100})[^\.\s]{1,2000}(?=(?:\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za)(?::\d{1,100})?)+(?:\s\w+=|\/|))[^"\s:\/]{1,2000})""",
    """"clientRequestPath":"({uri_path}[^"]{1,2000})""",
    """"clientRequestHTTPProtocol":"({protocol}[^"//]{1,2000})""",
    """"userAgent":.+({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)(.+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident))?"""
    ]
}
```