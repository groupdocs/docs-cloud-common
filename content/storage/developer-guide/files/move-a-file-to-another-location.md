---
id: "move-a-file-to-another-location"
url: "storage/move-a-file-to-another-location"
title: "Move a File to Another Location"
productName: "GroupDocs.Storage Cloud"
weight: 3
description: ""
keywords: ""
---
This API allows you to move a file from one location to other location within same Cloud Storage or to other Cloud Storage.

## API Explorer ##

[GroupDocs.Storage Cloud API Reference](https://apireference.groupdocs.cloud/storage/) lets you to try out [Move a File API](https://apireference.groupdocs.cloud/storage/#!/File/PostMoveFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes. Please check [this article]({{< ref "total/getting-started/ui-topics/create-new-app-and-get-app-key-and-sid.md" >}}) to learn how to get your App Key and SID. 

## cURL Example ##

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1.0/storage/file?src#Input/Annotated.pdf&#x26;dest#Output/Annotated.pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "authorization: Bearer wy_ZmPEeTmXAYKin4qPDnqZj0jged66uI1GEj_6MeKqlZpaTXK6zYXEtMbQacDSeKjLvA9GI18rHc8bUomPnnbymhH_uLF7hCzQ1Z9iW_EsIaYowiExEngeDUOdFUWygfJOhXnwwsDNZcFXY3dA8tCmYHJJXdSPgJnC-KvohHxYsfJTDTm4Fa4ixZWTv_tIqLtw2skNy3pq7TGd10Tifs-l7kPRlxL7OkyJsCY-usqRKEDxRRPKh2FSfx_AfJ5chwZGFlh-zlWwRnsL_w1Khi5WjKxQ-1-37MBa7aXDhjPcdr24s4pke1-jEXvPGvW37DirJjY0kTHTLwxoa3aIMeLWC_IUmQVCnpd6YCoAYI7914GRdMiJXF_SDTk1_T1dXTd9CHQSckWViM4IbD9eJyLOpM0Z8eCV-MNy7XTktFPIBtxbHBSBrxuLGWsxdFPSJEL2-MIA9XCq3hdILQOzNn-LkwIM"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-storage-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-storage-cloud), it hides the [REST API](https://apireference.groupdocs.cloud/storage/#!/File/PostMoveFile) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

### SDK Examples ###

{{< tabs tabTotal="3" tabID="10" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud 646c8583b210bcc2770ea6a518a30be9 Storage_CSharp_Post_Move_File.cs >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud 8db205dcff0fe84f155e4aa371c0b4f4 Storage_Php_Post_Move_File.php >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud efe67e20dac7c956c2a22b2d80bfa941 Storage_Ruby_Post_Move_File.rb  >}}

{{< /tab >}} {{< /tabs >}}
