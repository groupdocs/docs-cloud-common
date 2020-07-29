---
id: "quickstart"
url: "watermark/quickstart"
title: "Quickstart"
productName: "GroupDocs.Watermark Cloud"
weight: 3
description: ""
keywords: ""
---





# Create an account #

Creating an account is very simple. Go to [https://dashboard.groupdocs.cloud](https://dashboard.groupdocs.cloud/) to create a free account. 

# Create an API client app #

Before you can make any requests to GroupDocs Cloud API you need to get APP SID and APP key (secret key). This will be used to invoke the GroupDocs Cloud API. 

You can get it from the default Application or create a new Application from [My Apps tab of GroupDocs Cloud Dashboard]({{< ref "total/getting-started/ui-topics/create-new-app-and-get-app-key-and-sid.md" >}})).

# Install the SDK of your choice #

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Please check  article to learn how to add an SDK to your project.

# Make an API request from the SDK of your choice #

Use the **App SID** and **App key (secret key)** from the API app client you created in step one and replace in the corresponding code. Below is an example demonstrating how to get a list of all supported file formats in GroupDocs.Watermark Cloud.

{{< alert style="info" >}}
The GitHub repository for [GroupDocs.Watermark Cloud](https://github.com/groupdocs-watermark-cloud) has a complete set of examples, demonstrating our API capabilities.
{{< /alert >}}




 


* For complete examples and data files, please go to https://github.com/groupdocs-watermark-cloud/groupdocs-watermark-cloud-dotnet-samples
string MyAppKey # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
string MyAppSid # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
 
var configuration # new Configuration(MyAppSid, MyAppKey);
var apiInstance # new InfoApi(configuration);
\\var response # apiInstance.GetSupportedFileFormats();*

