---
weight: 1
id: "working-with-storage"
title: "Working With Storage"
url: "editor/working-with-storage"
---





# Storage existence API #

This API intended for checking the existence of cloud storage with a given name from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).
|---|---

## API Explorer ##

[GroupDocs.Editor Cloud API Reference](https://apireference.groupdocs.cloud/editor/#/) lets you try out [Storage existence API](https://apireference.groupdocs.cloud/editor/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.
|---|---|---|---

### Request parameters ###

|#
|---
Parameter
|#
Description

|
**storageName**
|
Storage name


## cURL Example ##



 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v1.0/editor/storage/MyStorage/exist" -H  "accept: application/json" -H  "authorization: Bearer  [Access Token]"
    
 ```


 Response

```html 
{
  "exists": true
}
 ```




## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-editor-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-editor-cloud), it hides the [Storage existence](https://apireference.groupdocs.cloud/editor/#/Storage/StorageExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###



 C#




{{< gist groupdocscloud 34f0df87ff6e7aaffef5876bdcb04a38 Editor_CSharp_Storage_Exist.cs >}}





 Java




{{< gist groupdocscloud cb5b0d1ae842f50f90382640823a2004 Editor_Java_Storage_Exist.java >}}





 PHP




{{< gist groupdocscloud 288fe44b5603cd7966fa72f293e91b88 Editor_Php_Storage_Exist.php >}}





 Ruby




{{< gist groupdocscloud ba011159eee59cd5a1f696ae6fadb2e4 Editor_Ruby_Working_With_Spreadsheets.rb >}}





 Node.js




{{< gist groupdocscloud d42190d60101442ccba939ac4db41454 Editor_Node_Storage_Exist.js >}}





 Python




{{< gist groupdocscloud 49c298f42348259cd85175f315d57272 Editor_Python_Storage_Exist.py >}}







# Storage object existence API #

This API intended for checking the existence of a file or folder in [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).
|---|---

## API Explorer ##

[GroupDocs.Editor Cloud API Reference](https://apireference.groupdocs.cloud/editor/#/) lets you try out [Storage existence API](https://apireference.groupdocs.cloud/editor/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.
|---|---|---|---

### Request parameters ###

|#
|---
Parameter
|#
Description

|

**path**
|

Path of the file or folder

Required. Can be passed as a query string parameter or as part of the URL

|
storageName
|
Name of the storage. If not set, then default storage used

|

versionId
|

File version id


## cURL Example ##



 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v1.0/editor/storage/exist/editordocs?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
 ```


 Response

```html 
{
  "exists": true,
  "isFolder": true
}
 ```




## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-editor-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-editor-cloud), it hides the [Storage Object existence](https://apireference.groupdocs.cloud/editor/#/Storage/ObjectExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###



 C#




{{< gist groupdocscloud 34f0df87ff6e7aaffef5876bdcb04a38 Editor_CSharp_Object_Exists.cs >}}





 Java




{{< gist groupdocscloud cb5b0d1ae842f50f90382640823a2004 Editor_Java_Object_Exists.java >}}





 PHP




{{< gist groupdocscloud 288fe44b5603cd7966fa72f293e91b88 Editor_Php_Object_Exists.php >}}





 Ruby




{{< gist groupdocscloud ba011159eee59cd5a1f696ae6fadb2e4 Editor_Ruby_Object_Exists.rb >}}





 Node.js




{{< gist groupdocscloud d42190d60101442ccba939ac4db41454 Editor_Node_Object_Exists.js >}}





 Python




{{< gist groupdocscloud 49c298f42348259cd85175f315d57272 Editor_Python_Object_Exists.py >}}







# Storage Space Usage API #

This API intended for getting total and used space of the[ GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)
|---|---

## API Explorer ##

[GroupDocs.Editor Cloud API Reference](https://apireference.groupdocs.cloud/editor/#/) lets you try out [storage space usage API](https://apireference.groupdocs.cloud/editor/#/Storage/GetDiscUsage) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.
|---|---|---|---

### Request parameters ###

|#
|---
Parameter
|#
Description

|
storageName
|
Name of the storage. If not set, then default storage used


## cURL Example ##



 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v1.0/editor/storage/disc?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
 ```


 Response

```html 
{
  "usedSize": 31032368,
  "totalSize": 3221225472
}
 ```




## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-editor-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-editor-cloud), it hides the [storage space usage API](https://apireference.groupdocs.cloud/editor/#/Storage/GetDiscUsage) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###



 C#




{{< gist groupdocscloud 34f0df87ff6e7aaffef5876bdcb04a38 Editor_CSharp_Get_Disc_Usage.cs >}}





 Java




{{< gist groupdocscloud cb5b0d1ae842f50f90382640823a2004 Editor_Java_Get_Disc_Usage.java >}}






 PHP




{{< gist groupdocscloud 288fe44b5603cd7966fa72f293e91b88 Editor_Php_Get_Disc_Usage.php >}}





 Ruby




{{< gist groupdocscloud ba011159eee59cd5a1f696ae6fadb2e4 Editor_Ruby_Get_Disc_Usage.rb >}}





 Node.js




{{< gist groupdocscloud d42190d60101442ccba939ac4db41454 Editor_Node_Get_Disc_Usage.js >}}





 Python




{{< gist groupdocscloud 49c298f42348259cd85175f315d57272 Editor_Python_Get_Disc_Usage.py >}}







# Storage File Versions API #

This API intended for getting the list of file versions, stored in the [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)
|---|---

## API Explorer ##

[GroupDocs.Editor Cloud API Reference](https://apireference.groupdocs.cloud/editor/#/) lets you try out [Storage File Versions API](https://apireference.groupdocs.cloud/editor/#/Storage/GetFileVersions) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.
|---|---|---|---

### Request parameters ###

|#
|---
Parameter
|#
Description

|

**path**
|

Path of the file including file name and extension e.g. /Folder1/file.ext

Required. Can be passed as a query string parameter or as part of the URL

|
storageName
|
Name of the storage. If not set, then default storage used


## cURL Example ##



 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v1.0/editor/storage/version/one-page.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
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

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-editor-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-editor-cloud), it hides the [Storage File Versions API](https://apireference.groupdocs.cloud/editor/#/Storage/GetFileVersions) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###



 C#




{{< gist groupdocscloud 34f0df87ff6e7aaffef5876bdcb04a38 Editor_CSharp_Get_File_Versions.cs >}}





 Java




{{< gist groupdocscloud cb5b0d1ae842f50f90382640823a2004 Editor_Java_Get_File_Versions.java >}}





 PHP




{{< gist groupdocscloud 288fe44b5603cd7966fa72f293e91b88 Editor_Php_Get_File_Versions.php >}}





 Ruby




{{< gist groupdocscloud ba011159eee59cd5a1f696ae6fadb2e4 Editor_Ruby_Get_File_Versions.rb >}}





 Node.js




{{< gist groupdocscloud d42190d60101442ccba939ac4db41454 Editor_Node_Get_File_Versions.js >}}





 Python




{{< gist groupdocscloud 49c298f42348259cd85175f315d57272 Editor_Python_Get_File_Versions.py >}}






 
