---
id: "get-a-list-of-files-of-a-specific-folder"
url: "storage/get-a-list-of-files-of-a-specific-folder"
title: "Get a list of Files of a Specific Folder"
productName: "GroupDocs.Storage Cloud"
weight: 4
description: ""
keywords: ""
---
This API allows you to get a list of all files of a specific folder from the specified Cloud Storage. If you do not pass storage name API will find folder in GroupDocs Cloud Storage.

**Note:** If you want to use a Cloud Storage other than GroupDocs Cloud Storage, you need to configure Third Party Storage with Groupdocs for Cloud. Please follow the instructions at [this page]({{< ref "total/getting-started/ui-topics/configure-3rd-party/_index.md" >}}) to configure your required storage.

## API Explorer ##

[GroupDocs.Storage Cloud API Reference](https://apireference.groupdocs.cloud/storage/) lets you to try out [List Files in a Folder API](https://apireference.groupdocs.cloud/storage/#!/Folder/GetListFiles) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs exposes. Please check [this article]({{< ref "total/getting-started/ui-topics/create-new-app-and-get-app-key-and-sid.md" >}}) to learn how to get your App Key and SID. 

## cURL Example ##

Request

```html
curl -v "https://api.groupdocs.cloud/v1.0/storage/folder?path#/Output" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "authorization: Bearer -Qz7_aqlSP2Mb3kvEKNwL69D6GmcSt3yPc8b4T4VP_DOkfjrNdesDYtM4Izzis8JJoRPSqQgOE1QYW41PeWjGomheHLZnsKHktAARwAzaPky0NfcT5LsMhKJMyfiFWMnF1JlDrK2Gn2ku51x-n-DwFaC3EJlwggrLfyyurCLlYd--PU55qj7okiOUxRYcd5C_F-Q2JnnYTdD4yIll33LP8GwaFlzfg5N9g9bc2XWG-9A8fi7yssSm6YqtSjMjrEypJIz4mC7zxwvP6uI39c9u5n-4vYJqoXyvQjCkDPdCZOejK7VnE7RZavDGV4OLjEgBSCh38LdCSUsKR0S2AK18PBIwb_Qf-RXsJtNnnjJdKbD1w-xE-8kfitHir6qdm4Ei-6adyNx0ZThXP3hulyUUErhetIPBVUaM25rWqy-9zflGRPfYrJWzDA27BcP262Thwd1zV3mh2MNptGAeIINChxebNE"
```

Response

```html
{
  "files": [
    {
      "name": "Annotated_pdf",
      "isFolder": true,
      "modifiedDate": "0001-01-01T00:00:00",
      "size": 0,
      "path": "/Output/Annotated_pdf/",
      "isDirectory": true
    },
    {
      "name": "Annotated.pdf",
      "isFolder": false,
      "modifiedDate": "2018-02-08T17:45:32+00:00",
      "size": 532683,
      "path": "/Output/Annotated.pdf",
      "isDirectory": false
    }
  ],
  "code": 200,
  "status": "OK"
}
```

## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-storage-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-storage-cloud), it hides the [REST API](https://apireference.groupdocs.cloud/storage/#!/Folder/GetListFiles) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

### SDK Examples ###

C#
{{< gist groupdocscloud 646c8583b210bcc2770ea6a518a30be9 Storage_CSharp_Get_List_Files.cs >}}

PHP
{{< gist groupdocscloud 8db205dcff0fe84f155e4aa371c0b4f4 Storage_Php_Get_List_Files.php >}}

Ruby
{{< gist groupdocscloud efe67e20dac7c956c2a22b2d80bfa941 Storage_Ruby_Get_list_file_of_Specific_Folder.rb >}}
