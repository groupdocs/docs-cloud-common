---
id: "working-with-files"
url: "translation/working-with-files"
title: "Working With Files"
productName: "GroupDocs.Translation Cloud"
weight: 6
description: ""
keywords: ""
---

 





# Download File API #

This API allows you to download a file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).

## API Explorer ##

[GroupDocs.Translation Cloud API Reference](https://apireference.groupdocs.cloud/translation) lets you try out [Download a File API](https://apireference.groupdocs.cloud/translation/#/File/DownloadFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Request parameters ###

|#
|---
Parameter
|#
Description

|
**Path**
|
Path of the file including file name and extension e.g. /Folder1/file.ext

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
curl -X GET "https://api.groupdocs.cloud/v1.0/translation/storage/file/one-page.docx?storageName#MyStorage" -H  "accept: multipart/form-data" -H  "authorization: Bearer [Access Token]"
    
 ```


 Response

```html 
{
  "Code": 200,
  "Status": "OK"
}
 ```



## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-translation-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-translation-cloud), it hides the [File API](https://apireference.groupdocs.cloud/translation/#/File) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###


 C#




{{< gist groupdocscloud ffdd7c22bdf290769f6aa83bb870a80d Translation_CSharp_Download_File.cs >}}






# Upload File API #

This API allows you to upload files to the [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

## API Explorer ##

[GroupDocs.Translation Cloud API Reference](https://apireference.groupdocs.cloud/translation/#/) lets you try out [Upload a File API](https://apireference.groupdocs.cloud/translation/#/File/UploadFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.


### Request Body parameters ###

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

|
File
|
File content


## cURL Example ##


 Request

```html 
curl -X POST "https://api.groupdocs.cloud/v1.0/translation/storage/file/editordocs%2Fone-page2.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"

 ```


 Response

```html 
Http status code: 200 (Returns OK and list of errors, which is empty if success.)
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2019-02-27T06:10:08.884Z"
      }
    }
  ]
}


 ```



## SDKs ##

Our API is completely independent of your operating system, database system, or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone, and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-translation-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-translation-cloud), it hides the [File API](https://apireference.groupdocs.cloud/translation/#/File) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###


 C#




{{< gist groupdocscloud ffdd7c22bdf290769f6aa83bb870a80d Translation_CSharp_Upload_File.cs >}}






# Delete File API #

This API allows you to delete a specific file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

## API Explorer ##

[GroupDocs.Translation Cloud API Reference](https://apireference.groupdocs.cloud/translation/#/) lets you try out [Delete a File](https://apireference.groupdocs.cloud/translation/#/File/DeleteFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.


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

|
versionId
|
File version id


## cURL Example ##


 Request

```html 
curl -X DELETE "https://api.groupdocs.cloud/v1.0/translation/storage/file/editordocs1%2Fone-page1.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"

 ```


 Response

```html 
{
  "Code": 200,
  "Status": "OK"
}
 ```



## SDKs ##

Our API is completely independent of your operating system, database system, or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone, and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-translation-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-translation-cloud), it hides the [File API](https://apireference.groupdocs.cloud/translation/#/File) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###


 C#




{{< gist groupdocscloud ffdd7c22bdf290769f6aa83bb870a80d Translation_CSharp_Delete_File.cs >}}






# File Copy API #

This API allows you to copy a specific file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

## API Explorer ##

[GroupDocs.Translation for Cloud API Reference](https://apireference.groupdocs.cloud/translation/#/) lets you try out [Copy File](https://apireference.groupdocs.cloud/translation/#/File/CopyFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose. 

### Request parameters ###

|#
|---
Parameter
|#
Description

|
**srcPath**
|
Path of the source file including file name and extension e.g. /Folder1/file.ext

Required. Can be passed as a query string parameter or as part of the URL

|
**destPath**
|
Path of the destination file. Required.

|
srcStorageName
|
Name of the storage of source file. If not set, then default storage used

|
destStorageName
|
Name of the storage of destination file. If not set, then default storage used

|
versionId
|
Source file version id


## cURL Example ##


 Request

```html 
curl -X PUT "https://api.groupdocs.cloud/v1.0/translation/storage/file/copy/editordocs%2Fone-page1.docx?destPath#editordocs1%2Fone-page1.docx'&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
    
 ```


 Response

```html 
{
  "Code": 200,
  "Status": "OK"
}
 ```


## SDKs ##

Our API is completely independent of your operating system, database system, or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone, and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-translation-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-translation-cloud), it hides the [File API](https://apireference.groupdocs.cloud/translation/#/File) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###


 C#




{{< gist groupdocscloud ffdd7c22bdf290769f6aa83bb870a80d Translation_CSharp_Copy_File.cs >}}







# File Move API #

This API allows you to copy a specific file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

## API Explorer ##

[GroupDocs.Translation for Cloud API Reference](https://apireference.groupdocs.cloud/translation/#/) lets you try out [Move File](https://apireference.groupdocs.cloud/translation/#/File/MoveFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose. 

### Request parameters ###

|#
|---
Parameter
|#
Description

|
**srcPath**
|
Path of the source file including file name and extension e.g. /Folder1/file.ext

Required. Can be passed as a query string parameter or as part of the URL

|
**destPath**
|
Path of the destination file. Required.

|
srcStorageName
|
Name of the storage of source file. If not set, then default storage used

|
destStorageName
|
Name of the storage of destination file. If not set, then default storage used

|
versionId
|
Source file version id


## cURL Example ##


 Request

```html 
curl -X PUT "https://api.groupdocs.cloud/v1.0/translation/storage/file/move/editordocs%2Fone-page1.docx?destPath#editordocs1%2Fone-page1.docx'&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
    
 ```


 Response

```html 
{
  "Code": 200,
  "Status": "OK"
}
 ```



## SDKs ##

Our API is completely independent of your operating system, database system, or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone, and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-translation-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-translation-cloud), it hides the [File API](https://apireference.groupdocs.cloud/translation/#/File) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###


 C#




{{< gist groupdocscloud ffdd7c22bdf290769f6aa83bb870a80d Translation_CSharp_Move_File.cs >}}




