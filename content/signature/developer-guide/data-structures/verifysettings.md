---
weight: 6
id: "verifysettings"
title: "VerifySettings"
url: "signature/verifysettings"
---

# VerifySettings #

VerifySettings data structure used as input parameters of method **~~/verify** for .

 

##### VerifySettings example #####

```html 

{
  "FileInfo": {
    "FilePath": "string",
    "StorageName": "string",
    "VersionId": "string",
    "Password": "string"
  },   
  "VerifyOptions": [
   		{
           "DocumentType": "Pdf",
           "SignatureType": "Text",  
           "Page": 1,
           "Text": "John",
           "MatchType": "Contains"
        }
	]
 }

 ```

##### VerifySettings fields #####

|Name|Description|API Version
|---|---|---
|FileInfo.FilePath|The path of the document, located in the storage. **Required.**| 
|FileInfo.StorageName|Storage name| 
|FileInfo.VersionId|File version Id| 
|FileInfo.Password|Password for password-protected document to be signed.| 
|VerifyOptions|Array with at least one VerifyOptions that specifies Verification options to provide Document signature verification



| 
|---


 

 
