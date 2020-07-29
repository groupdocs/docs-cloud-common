---
id: "quick-start"
url: "assembly/quick-start"
title: "Quick Start"
productName: "GroupDocs.Assembly Cloud"
weight: 3
description: ""
keywords: ""
---






## Create an account ##

Creating an account is very simple. Go to [https://dashboard.groupdocs.cloud](https://dashboard.groupdocs.cloud) to create a free account.

## Create an API client app ##

Before you can make any requests to GroupDocs for Cloud API you need to get APP SID and APP key (secret key). This will will be used to invoke GroupDocs for Cloud API.

You can get it from default Application or create new Application from [My Apps tab of GroupDocs for Cloud Dashboard]({{< ref "total/getting-started/ui-topics/create-new-app-and-get-app-key-and-sid.md" >}})).

## Install the SDK of your choice ##

GroupDocs for Cloud SDK is written in different languages, all you need to get started is adding our [SDK ]({{< ref "classification/getting-started/available-sdks.md" >}})to your existing project. 

## Make an API request from the SDK of your choice ##

Use the App SID and App key (secret key) from the API app client you created in step one and replace in the corresponding code. Below is an example demonstrating using Formats API to get all supported file formats in GroupDocs.Assembly Cloud.

{{< alert style="info" >}}The GitHub repository for GroupDocs.Assembly Cloud has a complete set of examples, demonstrating our API capabilities.{{< /alert >}}



 C#

```html 
using GroupDocs.Assembly.Cloud.Sdk.Api;
using GroupDocs.Assembly.Cloud.Sdk.Model;
using GroupDocs.Assembly.Cloud.Sdk.Model.Requests;
using System;
using System.IO;

namespace GroupDocs.Assembly.Cloud.Examples
{
    class Assembly_CSharp_Build_Charts_With_DataFile
    {
        public static void Run()
        {
            *TODO: Get your AppSID and AppKey at https://dashboard.groupdocs.cloud/ (free registration is required).
            var configuration # new Configuration
            {
                AppSid # "XXXXXX",
                AppKey # "XXXX-XXX",
                Version # Configuration.AvailiableApiVersions.V1
            };

            var apiInstance # new AssemblyApi(configuration);

            try
            {
                var request # new PostAssembleDocumentRequest();

                request.Name # "TestAllChartTypes.docx";
                request.Folder # "";
                request.Data # new MemoryStream(File.ReadAllBytes("../../../TestData/Teams.json"));
                request.DestFileName # "TestAllChartTypes_Out.pdf";
                request.SaveOptions # new LoadSaveOptionsData("pdf");

                * Get assembly results
                var response # apiInstance.PostAssembleDocument(request);
                Console.WriteLine(response.Length.ToString());

                using (var fileStream # new FileStream(request.DestFileName, FileMode.Create, FileAccess.Write))
                {
                    response.CopyTo(fileStream);
                }
            }
            catch (Exception e)
            {
                Console.WriteLine("Exception when calling AssemblyAPI: " + e.Message);
            }
        }
    }
}
 ```




