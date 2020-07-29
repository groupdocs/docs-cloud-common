---
id: "get-document-information"
url: "merger/get-document-information"
title: "Get Document Information"
productName: "GroupDocs.Merger Cloud"
weight: 2
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


Here is the list of properties that can be obtained for document pages:

* 
Page width in pixels (when converted to the image);

* 
Page height in pixels (when converted to image);

* Page number;
* 
Visible property that indicates whether the page is visible or not.


## Resource URI ##

```html 

HTTP POST ~/info

 ```

[Swagger UI](https://apireference.groupdocs.cloud/merger/#/Info/GetInfo) lets you call this REST API directly from the browser.  

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
curl -v "https://api.groupdocs.cloud/v1.0/merger/info" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer 
<jwt token>"
-d "{ FilePath: '/wordprocessing/four-pages.docx' }"


 ```


 Response

```html 
 {
  "extension": ".docx",
  "pages": [
   {
    "width": 612,
   "height": 792,
   "pageNumber": 1,
   "visible": true
   },
   {
   "width": 612,
   "height": 792,
    "pageNumber": 2,
    "visible": true
   },
   {
    "width": 612,
   "height": 792,
   "pageNumber": 3,
   "visible": true
   },
   {
   "width": 612,
    "height": 792,
   "pageNumber": 4,
   "visible": true
   }],
 "size": 8651,
 "fileFormat": "Microsoft Word Open XML Document"
}
 ```





# SDKs #

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-merger-cloud) for a complete list of GroupDocs.Merger Cloud SDKs along with working examples, to get you started in no time. Please check the [Get Document Information](https://apireference.groupdocs.cloud/merger/#/Info/GetInfo) article to learn how to add an SDK to your project.


## Get Document Information ##


 C#

{{< gist groupdocscloud b7a9ad2a32b358e32583134d20c4a384 Merger_CSharp_GetDocumentInformation.cs >}}




 Java

{{< gist groupdocscloud a22ef5f91f7f8565fee2bac658674b49 Merger_Java_GetDocumentInformation.java >}}




 PHP

{{< gist groupdocscloud 48648ca8f7d3bfedb079a7d7e3af9e0e Merger_Php_GetDocumentInformation.php >}}




 Ruby

{{< gist groupdocscloud 61d2eea73f56f457c060b2894d545d23 Merger_Ruby_GetDocumentInformation.rb >}}




 Node.js

{{< gist groupdocscloud 45a085bb4520da51407ee295a67b4021 Merger_Node_GetDocumentInformation.js >}}




 Python

{{< gist groupdocscloud ca731968d52778c9e2b0fc5d82d044d0 Merger_Python_GetDocumentInformation.py >}}





