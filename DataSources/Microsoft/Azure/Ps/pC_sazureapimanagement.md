#### Parser Content
```Java
{
Name = s-azure-api-management
 Vendor = Microsoft
 Product = Azure
 Lms = Splunk
 DataType = "cloud-admin-activity"
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
 Conditions = ["""operationName":"MICROSOFT.APIMANAGEMENT"""]
 Fields = [
         """time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
         """exabeam_host=([^=]{1,2000}@\s{0,100})?({host}[^\s]{1,2000})""",
         """({service}MICROSOFT.APIMANAGEMENT)""",
         """"MICROSOFT.APIMANAGEMENT\/({activity}[^"]{1,2000})""",
         """ipaddr":"({src_ip}[^"]{1,2000})""",
         """callerIpAddress":"({src_ip}[^"]{1,2000})""",
         """surname":"({user_lastname}[^"]{1,2000})""",
         """givenname":"({user_firstname}[^"]{1,2000})""",
         """claims\/name":"({user_email}[^@]{1,2000}@[^"]{1,2000})""",
         """identity/claims/nameidentifier":"({user}[^"]{1,2000})""",
         """roleDefinitionId":"({role}[^"]{1,2000})""",
         """resourceId":".*\/RESOURCEGROUPS\/({account_id}[^\/]{1,2000})"""
         """resultType":"({outcome}[^"]{1,2000})""",
         """\[Namespace:\s{0,100}({event_hub_namespace}\S+) ; EventHub name:\s{0,100}({event_hub_name}[\w-]{1,2000})"""
 ]
DupFields= ["event_hub_namespace->host"]
}
```