---
weight: 5
id: "signresult"
title: "SignResult"
url: "signature/signresult"
---

# SignResult #

SignResult data structure returned by  as output result

##### SignResult example #####

```html 

{
  "FileInfo": {
    "FilePath": "signed/one-page.pdf",
    "Password" : "1234567890"
  },
  "Size" : 12345,
  "DownloadUrl": "signed/one-page.pdf"
}

 

 ```

##### SignResult fields #####

|Name|Description
|---|---
|FilePath|Name of the signed document
|Size|Size of the signed document
|DownloadUrl|Page file path in the cloud storage. Use this value to download page using 

