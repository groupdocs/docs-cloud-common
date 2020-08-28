---
id: "quick-start"
url: "storage/quick-start"
title: "Quick Start"
productName: "GroupDocs.Storage Cloud"
weight: 2
description: ""
keywords: ""
---


# Create an account #

Creating an account is very simple. Go to [Dashboard](https://dashboard.groupdocs.cloud) to create a free account.

# Create an API client app #

Before you can make any requests to GroupDocs for Cloud API you need to get APP SID and APP key (secret key). This will will be used to invoke GroupDocs for Cloud API.

You can get it from default Application or create new Application from [My Apps tab of GroupDocs for Cloud Dashboard]({{< ref "total/getting-started/ui-topics/create-new-app-and-get-app-key-and-sid.md" >}}).

# Install the SDK of your choice #

GroupDocs for Cloud SDK is written in different languages, all you need to get started is adding our [SDK]({{< ref "storage/getting-started/available-sdks.md" >}}) to your existing project.

# Make an API request from the SDK of your choice #

Use the **App SID** and **App key (secret key)** from the API app client you created in step one and replace in the corresponding code. Below is an example demonstrating using Formats API to get all supported file formats in GroupDocs.Viewer for Cloud.

{{< alert style="info" >}}The GitHub repository for [GroupDocs.Storage Cloud](https://github.com/groupdocs-storage-cloud) has a complete set of examples, demonstrating our API capabilities.{{< /alert >}}

{{< tabs tabTotal="3" tabID="1" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud 646c8583b210bcc2770ea6a518a30be9 Storage_CSharp_Get_Is_Exist.cs >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud 8db205dcff0fe84f155e4aa371c0b4f4 Storage_Php_Get_Is_Exist.php >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud efe67e20dac7c956c2a22b2d80bfa941 Storage_Ruby_Get_Is_Exist.rb >}}

{{< /tab >}} {{< /tabs >}}
