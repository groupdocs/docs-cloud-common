---
id: "get-document-information"
url: "editor/get-document-information"
title: "Get Document Information"
productName: "GroupDocs.Editor Cloud"
weight: 3
description: ""
keywords: ""
---





# Introduction #

This REST API allows us to obtain basic information about the document and it's pages properties. The endpoint accepts the document storage path as input payload.
Here is the list of properties that can be obtained for a document:

* Document file extension;
* Document size in bytes;
* 
Document file format.

* Pages count
* Password protection

## Resources ##

```html 

HTTP POST ~/info

 ```

[Swagger UI](https://apireference.groupdocs.cloud/editor/#/Info/GetInfo) lets you call this REST API directly from the browser.  

## cURL Example ##



 


 Request

```html 
* First get JSON Web Token
* Please get your App Key and App SID from https://dashboard.groupdocs.cloud/#/apps. Kindly place App Key in "client_secret" and App SID in "client_id" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type#client_credentials&#x26;client_id#xxxx&#x26;client_secret#xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
 
* cURL example to get document information
curl -v "https://api.groupdocs.cloud/v1.0/editor/info" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer 
<jwt token>"
-d "{ FilePath: 'words/four-pages.docx' }"
 ```


 Response

```html 
{
  "pageCount": 4,
  "size": 8651,
  "isEncrypted": false,
  "formatName": "Office Open XML WordProcessingML Macro-Free Document (DOCX)",
  "formatExtension": "docx"
}
 ```





## SDKs ##


Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-editor-cloud) for a complete list of GroupDocs.Editor Cloud SDKs along with working examples, to get you started in no time. Please check the article to learn how to add an SDK to your project.


### Get Document Information Examples ###


 C#




{{< gist groupdocscloud 34f0df87ff6e7aaffef5876bdcb04a38 Editor_CSharp_Get_Document_Information.cs >}}





 Java




{{< gist groupdocscloud cb5b0d1ae842f50f90382640823a2004 Editor_Java_Get_Document_Information.java >}}





 PHP




{{< gist groupdocscloud 288fe44b5603cd7966fa72f293e91b88 Editor_Php_Get_Document_Information.php >}}





 Ruby




{{< gist groupdocscloud ba011159eee59cd5a1f696ae6fadb2e4 Editor_Ruby_Get_Document_Information.rb >}}





 Node.js




{{< gist groupdocscloud d42190d60101442ccba939ac4db41454 Editor_Node_Get_Document_Information.js >}}





 Python




{{< gist groupdocscloud 49c298f42348259cd85175f315d57272 Editor_Python_Get_Document_Information.py >}}




