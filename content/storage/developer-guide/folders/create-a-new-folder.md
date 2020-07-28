---
weight: 1
id: "create-a-new-folder"
title: "Create a New Folder"
url: "storage/create-a-new-folder"
---






# Create a New Folder #

This API allows you to create a new Folder in the specified Cloud Storage. If you do not pass storage name API will create new Folder in default Cloud Storage.

**Note:** If you want to use a Cloud Storage other than GroupDocs Cloud Storage, you need to configure Third Party Storage with Groupdocs for Cloud. Please follow the instructions at [this page]({{< ref "total\getting-started\ui-topics\configure-3rd-party\_index.md" >}}) to configure your required storage.

## API Explorer ##

[GroupDocs.Storage Cloud API Reference](https://apireference.groupdocs.cloud/storage/) lets you to try out [Create Folder API](https://apireference.groupdocs.cloud/storage/#!/Folder/PutCreateFolder) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs exposes. Please check [this article]({{< ref "total\getting-started\ui-topics\create-new-app-and-get-app-key-and-sid.md" >}}) to learn how to get your App Key and SID. 

## cURL Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1.0/storage/folder?path#Output/NewFolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "authorization: Bearer -Qz7_aqlSP2Mb3kvEKNwL69D6GmcSt3yPc8b4T4VP_DOkfjrNdesDYtM4Izzis8JJoRPSqQgOE1QYW41PeWjGomheHLZnsKHktAARwAzaPky0NfcT5LsMhKJMyfiFWMnF1JlDrK2Gn2ku51x-n-DwFaC3EJlwggrLfyyurCLlYd--PU55qj7okiOUxRYcd5C_F-Q2JnnYTdD4yIll33LP8GwaFlzfg5N9g9bc2XWG-9A8fi7yssSm6YqtSjMjrEypJIz4mC7zxwvP6uI39c9u5n-4vYJqoXyvQjCkDPdCZOejK7VnE7RZavDGV4OLjEgBSCh38LdCSUsKR0S2AK18PBIwb_Qf-RXsJtNnnjJdKbD1w-xE-8kfitHir6qdm4Ei-6adyNx0ZThXP3hulyUUErhetIPBVUaM25rWqy-9zflGRPfYrJWzDA27BcP262Thwd1zV3mh2MNptGAeIINChxebNE"
    
 ```




 Response

```html 
{  
  "code": 200,
  "status": "OK"
}
 ```






## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-storage-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-storage-cloud), it hides the [REST API](https://apireference.groupdocs.cloud/storage/#!/Folder/PutCreateFolder) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

### SDK Examples ###





 C#




{{< gist groupdocscloud 646c8583b210bcc2770ea6a518a30be9 Storage_CSharp_Put_Create_Folder.cs >}}







 PHP




{{< gist groupdocscloud 8db205dcff0fe84f155e4aa371c0b4f4 Storage_Php_Put_Create_Folder.php >}}







 Ruby




{{< gist groupdocscloud efe67e20dac7c956c2a22b2d80bfa941 Storage_Ruby_Put_Create_Folder.rb >}}







