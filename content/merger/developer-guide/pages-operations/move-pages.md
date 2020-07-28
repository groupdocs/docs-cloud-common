---
weight: 1
id: "move-pages"
title: "Move Pages"
url: "merger/move-pages"
---






# Introduction #

This REST API provides a move page feature that allows you to manipulate page ordering by moving any page(s) to a new position within a document. 
For moving page to a new position, it's needed to specify current and new page numbers along with the path to document in storage. For protected documents, it is also required to provide a password.
The table below contains the full list of properties that can be specified while moving document pages.

|#
|---
Name
|#
Description
|#
Comment

|

FilePath
|
The file path in the storage
|
Required property

|

StorageName
|
Storage name
|
It could be omitted for default storage.

|

VersionId
|
File version Id
|
Useful for storages that support file versioning

|


Password
|

The password to open file
|

Should be specified only for password-protected documents

|


PageNumber
|

Page number to move
|

Required

|


NewPageNumber
|

New page number
|

Required

|


OutputPath
|

Path to resultant document
|

Required



## Resource URI ##

```html 

HTTP GET ~/Pages/Move

 ```

[Swagger UI](https://apireference.groupdocs.cloud/merger/#/Pages/Move) lets you call this REST API directly from the browser.  
|---|---

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
 
* cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v1.0/merger/pages/move" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer 
<jwt token>" \ 
-d "{
  'FileInfo': { 'FilePath': 'words/four-pages.docx'},
     'PageNumber':  1, 
     'NewPageNumber':  2, 
     'OutputPath': 'output/move-page.docx' 
 }"
 ```


 Response
```html 

* Response will contain storage path to resultant document
{
  "path": "output/move-page.docx"
}
 ```




## SDKs ##

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-merger-cloud) for a complete list of GroupDocs.Merger Cloud SDKs along with working examples, to get you started in no time. Please check to [Get Supported File Formats]({{< ref "merger\getting-started\supported-document-formats.md" >}})) article to learn how to add an SDK to your project.
|---|---|---|---

### Move Pages ###

 C#

{{< gist groupdocscloud b7a9ad2a32b358e32583134d20c4a384 Merger_CSharp_MovePage.cs >}}




 Java

{{< gist groupdocscloud a22ef5f91f7f8565fee2bac658674b49 Merger_Java_MovePage.java >}}





 PHP

{{< gist groupdocscloud 48648ca8f7d3bfedb079a7d7e3af9e0e Merger_Php_MovePage.php >}}




 Ruby

{{< gist groupdocscloud 61d2eea73f56f457c060b2894d545d23 Merger_Ruby_MovePage.rb >}}




 Node.js

{{< gist groupdocscloud 45a085bb4520da51407ee295a67b4021 Merger_Node_MovePage.js >}}




 Python

{{< gist groupdocscloud ca731968d52778c9e2b0fc5d82d044d0 Merger_Python_MovePage.py >}}




