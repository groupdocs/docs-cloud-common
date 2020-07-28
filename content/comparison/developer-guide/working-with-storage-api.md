---
keywords: ""
description: ""
weight: 4
id: "working-with-storage-api"
title: "Working with Storage API"
url: "comparison/working-with-storage-api"
---






# Storage existence API #

This API intended for checking existence of cloud storage with given name from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).
|---|---

## API Explorer ##

[GroupDocs.Comparison Cloud API Reference](https://apireference.groupdocs.cloud/comparison/#/) lets you to try out [Storage existence API](https://apireference.groupdocs.cloud/comparison/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.
|---|---|---|---

### Request parameters ###

|Parameter|Description
|---|---
|**storageName**|Storage name


## cURL Example ##





 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v2.0/comparison/storage/MyStorage/exist" -H  "accept: application/json" -H  "authorization: Bearer  [Access Token]"
    
 ```




 Response

```html 
{
  "exists": true
}
 ```






## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-comparison-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-comparison-cloud), it hides the [Storage existence](https://apireference.groupdocs.cloud/comparison/#/Storage/StorageExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###





 C#




{{< gist groupdocscloud 622c78dd86e4c5ade7e870295b6db376 Comparison_CSharp_Storage_Exist.cs >}}







 Java




{{< gist groupdocscloud fcf2013d068abf714662f99cba3c0d47 Comparison_Java_Storage_Exist.java >}}







 PHP




{{< gist groupdocscloud 24ad96946345493cb230d7124f22c176 Comparison_Php_Storage_Exist.php >}}







 Ruby




{{< gist groupdocscloud f830f503cb44c7aa38a757cb86b34f5d Comparison_Ruby_Storage_Exist.rb >}}







 Node.js




{{< gist groupdocscloud 7999207c55ecfba6c2a125f5b77ca0d8 Comparison_Node_Storage_Exist.js >}}







 Python




{{< gist groupdocscloud 5b471172e33a251d70b08127085d200e Comparison_Python_Storage_Exist.py >}}









# Storage object existence API #

This API intended for checking existence of file or folder in [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).
|---|---

## API Explorer ##

[GroupDocs.Comparison Cloud API Reference](https://apireference.groupdocs.cloud/comparison/#/) lets you to try out [Storage existence API](https://apireference.groupdocs.cloud/comparison/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.
|---|---|---|---

### Request parameters ###

|Parameter|Description
|---|---
|**path**|Path of the file or folder

Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|versionId|File version id


## cURL Example ##





 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v2.0/comparison/storage/exist/comparisondocs?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
 ```




 Response

```html 
{
  "exists": true,
  "isFolder": true
}
 ```






## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-comparison-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-comparison-cloud), it hides the [Storage Object existence](https://apireference.groupdocs.cloud/comparison/#/Storage/ObjectExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###







 C#




{{< gist groupdocscloud 622c78dd86e4c5ade7e870295b6db376 Comparison_CSharp_Object_Exists.cs >}}







 Java




{{< gist groupdocscloud fcf2013d068abf714662f99cba3c0d47 Comparison_Java_Object_Exists.java >}}









 PHP




{{< gist groupdocscloud 24ad96946345493cb230d7124f22c176 Comparison_Php_Object_Exists.php >}}







 Ruby




{{< gist groupdocscloud f830f503cb44c7aa38a757cb86b34f5d Comparison_Ruby_Object_Exists.rb >}}







 Node.js




{{< gist groupdocscloud 7999207c55ecfba6c2a125f5b77ca0d8 Comparison_Node_Object_Exists.js >}}







 Python




{{< gist groupdocscloud 5b471172e33a251d70b08127085d200e Comparison_Python_Object_Exists.py >}}









# Storage Space Usage API #

This API intended for getting total and used space of the[ GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)
|---|---

## API Explorer ##

[GroupDocs.Comparison Cloud API Reference](https://apireference.groupdocs.cloud/conversion/#/) lets you to try out [storage space usage API](https://apireference.groupdocs.cloud/comparison/#/Storage/GetDiscUsage) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.
|---|---|---|---

### Request parameters ###

|Parameter|Description
|---|---
|storageName|Name of the storage. If not set, then default storage used


## cURL Example ##





 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v2.0/comparison/storage/disc?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
 ```




 Response

```html 
{
  "usedSize": 31032368,
  "totalSize": 3221225472
}
 ```






## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-comparison-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-comparison-cloud), it hides the [storage space usage API](https://apireference.groupdocs.cloud/comparison/#/Storage/GetDiscUsage) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###





 C#




{{< gist groupdocscloud 622c78dd86e4c5ade7e870295b6db376 Comparison_CSharp_Get_Disc_Usage.cs >}}







 Java




{{< gist groupdocscloud fcf2013d068abf714662f99cba3c0d47 Comparison_Java_Get_Disc_Usage.java >}}







 PHP




{{< gist groupdocscloud 24ad96946345493cb230d7124f22c176 Comparison_Php_Get_Disc_Usage.php >}}







 Ruby




{{< gist groupdocscloud f830f503cb44c7aa38a757cb86b34f5d Comparison_Ruby_Get_Disc_Usage.rb >}}







 Node.js




{{< gist groupdocscloud 7999207c55ecfba6c2a125f5b77ca0d8 Comparison_Node_Get_Disc_Usage.js >}}







 Python




{{< gist groupdocscloud 5b471172e33a251d70b08127085d200e Comparison_Python_Get_Disc_Usage.py >}}









# Storage File Versions API #

This API intended for getting the list of file versions, stored in the [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)
|---|---

## API Explorer ##

[GroupDocs.Comparison Cloud API Reference](https://apireference.groupdocs.cloud/conversion/#/) lets you to try out [Storage File Versions API](https://apireference.groupdocs.cloud/comparison/#/Storage/GetFileVersions) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.
|---|---|---|---

### Request parameters ###

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext

Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used


## cURL Example ##





 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v2.0/comparison/storage/version/one-page.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
 ```




 Response

```html 
{
  "value": [
    {
      "versionId": "null",
      "isLatest": true,
      "name": "one-page.docx",
      "isFolder": false,
      "modifiedDate": "2018-08-16T19:45:05+00:00",
      "size": 347612,
      "path": "/one-page.docx"
    }
  ]
}
 ```






## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-comparison-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-comparison-cloud), it hides the [Storage File Versions API](https://apireference.groupdocs.cloud/comparison/#/Storage/GetFileVersions) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###

 





 C#




{{< gist groupdocscloud 622c78dd86e4c5ade7e870295b6db376 Comparison_CSharp_Get_File_Versions.cs >}}







 Java




{{< gist groupdocscloud fcf2013d068abf714662f99cba3c0d47 Comparison_Java_Get_File_Versions.java >}}







 PHP




{{< gist groupdocscloud 24ad96946345493cb230d7124f22c176 Comparison_Php_Get_File_Versions.php >}}







 Ruby




{{< gist groupdocscloud f830f503cb44c7aa38a757cb86b34f5d Comparison_Ruby_Get_File_Versions.rb >}}







 Node.js




{{< gist groupdocscloud 7999207c55ecfba6c2a125f5b77ca0d8 Comparison_Node_Get_File_Versions.js >}}







 Python




{{< gist groupdocscloud 5b471172e33a251d70b08127085d200e Comparison_Python_Get_File_Versions.py >}}







