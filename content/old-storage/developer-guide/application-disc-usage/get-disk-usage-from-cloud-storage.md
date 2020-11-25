---
id: "get-disk-usage-from-cloud-storage"
url: "storage/get-disk-usage-from-cloud-storage"
title: "Get Disk Usage from Cloud Storage"
productName: "GroupDocs.Storage Cloud"
weight: 1
description: ""
keywords: ""
---
This API allows you to get disk usage details from specified Cloud Storage. If you do not pass storage name API will find folder in GroupDocs Cloud Storage.

**Note:** If you want to use a Cloud Storage other than GroupDocs Cloud Storage, you need to configure Third Party Storage with Groupdocs for Cloud. Please follow the instructions at [this page]({{< ref "total/getting-started/ui-topics/configure-3rd-party/_index.md" >}}) to configure your required storage.

## API Explorer ##

[GroupDocs.Storage Cloud API Reference](https://apireference.groupdocs.cloud/storage/) lets you to try out [Get Disk Usage API](https://apireference.groupdocs.cloud/storage/#!/Storage/GetDiscUsage) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs exposes. Please check [this article]({{< ref "total/getting-started/ui-topics/creating-and-managing-application.md" >}}) to learn how to get your App Key and SID. 

## cURL Example ##

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1.0/storage/disc" -X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "authorization: Bearer c-luONyAsQ1vSrygeoqxPBC9jX-KE8zc_Fy13GkyfAV1n-yZq-NHYVmGYwj-z1FuHjm-8ogxz6XrRMQoyBqz5viML85WhN1GhNnPqrgoZ80IgAM5jTx5czuDEV4AqnJWrTx2HHm9Rb9LhWNdizZqltGae7oCJ-LR-ELR1T0GAimij_4Zbt5T5GIj67Xpz5MQpxkuC1lhU3sCVCOgsNT4Zq_MAOyTZV8ZBDJja4brN5EyggxgR3fYKsfaPSEd6De7Zr__-_LTH5QX9g9QsgfliaZsUgGUEWNTouIQhxBnCnusF98T3oUrYF8Wh2OoPl0Os_cN0loBHPfFrMsV6eSJafxzgVQRsF9U48HQZe_euKyh-N4UKASnOfTgQ-hvSV83ufjxwvTKHqzagYAEjvHvJU8YL6T8aoTBG2G8-GOt23GrxR0cPzTyVxZ2xobLPYhH8ZDGvkSWDdZJDkTwD-VaSp9GaGA"    
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "discUsage": {
    "usedSize": 3178138,
    "totalSize": 3221225472
  },
  "code": 200,
  "status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-storage-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-storage-cloud), it hides the [REST API](https://apireference.groupdocs.cloud/storage/#!/Storage/GetDiscUsage) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

### SDK Examples ###

{{< tabs tabTotal="3" tabID="10" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud 646c8583b210bcc2770ea6a518a30be9 Storage_CSharp_Get_Disk_Usage.cs >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud 8db205dcff0fe84f155e4aa371c0b4f4 Storage_Php_Get_Disk_Usage.php >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud efe67e20dac7c956c2a22b2d80bfa941 Storage_Ruby_Get_Disk_Usage.rb >}}

{{< /tab >}} {{< /tabs >}}
