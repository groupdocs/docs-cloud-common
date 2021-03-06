---
id: "check-presence-of-a-file"
url: "storage/check-presence-of-a-file"
title: "Check Presence of a File"
productName: "GroupDocs.Storage Cloud"
weight: 5
description: ""
keywords: ""
---
This API allows you to check if a file exists in the specified Cloud Storage. If you do not pass storage name API will check file in default Cloud Storage.

## API Explorer ##

[GroupDocs.Storage Cloud API Reference](https://apireference.groupdocs.cloud/storage/) lets you to try out [File presence API](https://apireference.groupdocs.cloud/storage/#!/Storage/GetIsExist) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes. Please check [this article]({{< ref "total/getting-started/ui-topics/creating-and-managing-application.md" >}}) to learn how to get your App Key and SID. 

## cURL Example ##

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1.0/storage/exist?path#Output/Annotated.pdf" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "authorization: Bearer -Qz7_aqlSP2Mb3kvEKNwL69D6GmcSt3yPc8b4T4VP_DOkfjrNdesDYtM4Izzis8JJoRPSqQgOE1QYW41PeWjGomheHLZnsKHktAARwAzaPky0NfcT5LsMhKJMyfiFWMnF1JlDrK2Gn2ku51x-n-DwFaC3EJlwggrLfyyurCLlYd--PU55qj7okiOUxRYcd5C_F-Q2JnnYTdD4yIll33LP8GwaFlzfg5N9g9bc2XWG-9A8fi7yssSm6YqtSjMjrEypJIz4mC7zxwvP6uI39c9u5n-4vYJqoXyvQjCkDPdCZOejK7VnE7RZavDGV4OLjEgBSCh38LdCSUsKR0S2AK18PBIwb_Qf-RXsJtNnnjJdKbD1w-xE-8kfitHir6qdm4Ei-6adyNx0ZThXP3hulyUUErhetIPBVUaM25rWqy-9zflGRPfYrJWzDA27BcP262Thwd1zV3mh2MNptGAeIINChxebNE"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "fileExist": {
    "isExist": true,
    "isFolder": false
  },
  "code": 200,
  "status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-storage-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-storage-cloud), it hides the [REST API](https://apireference.groupdocs.cloud/storage/#!/Storage/GetIsExist) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

### SDK Examples ###

{{< tabs tabTotal="3" tabID="10" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud 646c8583b210bcc2770ea6a518a30be9 Storage_CSharp_Get_Is_Exist.cs >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud 8db205dcff0fe84f155e4aa371c0b4f4 Storage_Php_Get_Is_Exist.php >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud efe67e20dac7c956c2a22b2d80bfa941 Storage_Ruby_Get_Is_Exist.rb >}}

{{< /tab >}} {{< /tabs >}}
