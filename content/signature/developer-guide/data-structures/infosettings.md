---
weight: 2
id: "infosettings"
title: "InfoSettings"
url: "signature/infosettings"
---

# InfoSettings #

InfoSettings data structure used as input parameters for  to retrieve information

{{< alert style="info" >}}
Not all options are supported by all document formats. Each option may correspond to one or more formats.
{{< /alert >}}

 

##### InfoSettings example #####

```html 

{
  "FileInfo": {
    "FilePath": "string",
    "StorageName": "string",
    "VersionId": "string",
    "Password": "string"
  }
}

 ```

##### InfoSettings fields #####

|Name|Description|API Version
|---|---|---
|FileInfo.FilePath|The path of the document, located in the storage. **Required.**| 
|FileInfo.StorageName|Storage name| 
|FileInfo.VersionId|File version Id| 
|FileInfo.Password|Password for rendering password-protected documents| 

