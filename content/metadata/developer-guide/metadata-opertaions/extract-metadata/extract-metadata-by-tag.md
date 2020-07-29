---
id: "extract-metadata-by-tag"
url: "metadata/extract-metadata-by-tag"
title: "Extract Metadata By Tag"
productName: "GroupDocs.Metadata Cloud"
description: ""
keywords: ""
---






# Introduction #

This REST API allows to extract metadata properties from the document choosing the properties by exact tag and category name.

## cURL Example ##

The following example demonstrates how to extract metadata information from all properties with Created tag.


 Request

```html 

* First get JSON Web Token
* Please get your App Key and App SID from https://dashboard.groupdocs.cloud/#/apps. Kindly place App Key in "client_secret" and App SID in "client_id" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type#client_credentials&client_id#xxxx&client_secret#xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
  
* cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v1.0/metadata" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d "{
    "FileInfo": {
        "FilePath": "documents\\input.docx",
        "StorageName": ""
    },
    "SearchCriteria": {
        "TagOptions": {
            "ExactTag": {
                "Name": "Created",
                "Category": "Time"
            }
        }
    }
}"

 ```


 Response

```html 

{
    "properties": [
        {
            "name": "CreateTime",
            "value": "03/22/2016 17:08:00",
            "propertyType": "DateTime",
            "tags": [
                {
                    "name": "Created",
                    "category": "Time"
                },
                {
                    "name": "PropertyTypeBuiltIn",
                    "category": "Document"
                }
            ]
        }
    ]
}

 ```



# SDKs #

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-metadata-cloud) for a complete list of GroupDocs.Metadata Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "metadata/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

## Extract Metadata By Tag ##


 C#



{{< gist groupdocscloud 3c211b41ef72c2070064a8ad93f14fdc Metadata_CSharp_Extract_Metadata_By_Tag.cs >}}





 Java




{{< gist groupdocscloud b613728b13cd4a7c5e1d585361108181 Metadata_Java_Extract_Metadata_By_Tag.java >}}







 