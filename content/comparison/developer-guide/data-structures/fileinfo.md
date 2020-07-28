---
weight: 7
id: "fileinfo"
title: "FileInfo"
url: "comparison/fileinfo"
---

## FileInfo ##

FileInfo data structure used for input files description in various comparison cloud API methods.

FileInfo example:


```javascript 

{
    "FilePath": "string",
    "VersionId": "string",
    "StorageName": "string",
    "Password": "string"
}

 ```



 

|Name|Description
|---|---
|FilePath|Path of the file in the cloud storage
|VersionId|File Version, can be null or omitted.
|StorageName|Name of the cloud storage. Can be omitted, then default storage used.
|Password|The password for password-protected documents (docx, pdf, etc)

 


