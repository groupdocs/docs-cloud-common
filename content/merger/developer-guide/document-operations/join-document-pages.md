---
weight: 1
id: "join-document-pages"
title: "Join Document Pages"
url: "merger/join-document-pages"
---






# Introduction #

This REST API allows merging the source document with specific document pages from joined documents into one resultant document by specifying desired page numbers or page ranges. Joined documents should be of the same format. 
There are several ways to specify page numbers needed from each document:

* Provide exact page numbers via Pages collection;
* Specify pages range start/end page numbers. There is also an ability to get only even/odd pages from the specified page range by setting RangeMode property. 

For protected documents, it is also required to provide a password.
The table below contains the full list of properties that can be specified for each joined document.


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
Could be omitted for default storage

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

Pages
|

Collection of page numbers to use in a Join operation
|

The first page should have number 1

|

StartPageNumber
|

Start page number
|

Ignored if Pages collection is not empty

|

EndPageNumber
|

End page number
|

Ignored if Pages collection is not empty

|

RangeMode
|

Page range mode: Even, Odd, All. The default value is All
|

Ignored if Pages collection is not empty

|


OutputPath
|

Path to resultant document
|

Required




 

## Resource URI ##

```html 

HTTP POST ~/join

 ```

[Swagger UI](https://apireference.groupdocs.cloud/merger/#/Document/Join) lets you call this REST API directly from the browser.  
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
 
* cURL example to join pages from several documents into one document
curl -v "https://api.groupdocs.cloud/v1.0/merger/join" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer 
<jwt token>"
-d "{ 
    'JoinItems': 
    [ 
        { 
            'FileInfo': 
            { 
                'FilePath': 'WordProcessing/sample-10-pages.docx'
            },
            'Pages':  [ 3, 6, 8 ], 
        },
        {   
            'FileInfo': 
            { 
                'FilePath': 'WordProcessing/four-pages.docx'
            },
            'StartPageNumber': 1,
            'EndPageNumber': 4,
            'RangeMode' : 1
        } 
    ], 
    'OutputPath': 'output/joined-pages.docx'
}"

 ```


 Response
```html 

* Response will contain storage path to resultant document
{
  "path": "output/joined-pages.docx"
}
 ```





# SDKs #

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-merger-cloud) for a complete list of GroupDocs.Merger Cloud SDKs along with working examples, to get you started in no time. Please check the article to learn how to add an SDK to your project.
|---|---

## Join Document Pages ##



 C#

{{< gist groupdocscloud b7a9ad2a32b358e32583134d20c4a384 Merger_CSharp_JoinPagesFromVariousDocuments.cs >}}




 Java

{{< gist groupdocscloud a22ef5f91f7f8565fee2bac658674b49 Merger_Java_JoinPagesFromVariousDocuments.java >}}




 PHP

{{< gist groupdocscloud 48648ca8f7d3bfedb079a7d7e3af9e0e Merger_Php_JoinPagesFromVariousDocuments.php >}}




 Ruby

{{< gist groupdocscloud 61d2eea73f56f457c060b2894d545d23 Merger_Ruby_JoinPagesFromVariousDocuments.rb >}}




 Node.js

{{< gist groupdocscloud 45a085bb4520da51407ee295a67b4021 Merger_Node_JoinPagesFromVariousDocuments.js >}}




 Python

{{< gist groupdocscloud ca731968d52778c9e2b0fc5d82d044d0 Merger_Python_JoinPagesFromVariousDocuments.py >}}




