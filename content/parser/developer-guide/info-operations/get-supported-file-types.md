---
id: "get-supported-file-types"
url: "parser/get-supported-file-types"
title: "Get Supported File Types"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
---






# Introduction #

This REST API allows getting a list of all [file formats supported ]({{< ref "parser/getting-started/supported-document-formats.md" >}}))by GroupDocs.Parser Cloud product.
|---|---

## Resources ##

The following GroupDocs.Parser Cloud REST API resource has been used in the [get supported file types](https://apireference.groupdocs.cloud/parser/#/Info/GetSupportedFileFormats) example.
|---|---







 

|
|---




HTTP POST ~~/formats




 




## cURL Example ##

The following example demonstrates how to get supported file types.



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
curl -v "https://api.groupdocs.cloud/v1.0/parser/formats" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer 
<jwt token>"


 ```


 Response

```html 
{
  "formats": [    
    {
      "extension": ".doc",
      "fileFormat": "Microsoft Word Document"
    },
    {
      "extension": ".docm",
      "fileFormat": "Word Open XML Macro-Enabled Document"
    },
    {
      "extension": ".docx",
      "fileFormat": "Microsoft Word Open XML Document"
    },
   ...
    {
      "extension": ".xlsx",
      "fileFormat": "Microsoft Excel Open XML Spreadsheet"
    }
  ]
}


 ```




## SDKs ##

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-parser-cloud for a complete list of GroupDocs.Parser Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "parser/getting-started/available-sdks.md" >}})) article to learn how to add an SDK to your project.
|---|---|---|---

### Get Supported File Types Examples ###



 C#




{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Get_Document_File_Types.cs >}}





 Java




{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Get_Document_File_Types.java >}}




