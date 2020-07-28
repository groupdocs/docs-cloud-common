---
weight: 1
id: "overview"
title: "Overview"
url: "comparison/overview"
---






# GroupDocs.Comparison Cloud #

GroupDocs.Comparison Cloud is a REST API that provides an ability to detect differences between source and target files for changes at paragraphs, words and characters levels. Can identify styling and formatting changes - like bold, italic, underlines, strike-troughs, font types, etc.

Every particular difference between compared document can be applied or rejected and the exported to a final document.

GroupDocs.Comparison Cloud allows to obtain basic information about source document - file type, size, pages count etc.

Once comparison process is complete, you can save a differences summary report which lists all changes found between compared documents.

## API Endpoint Groups Overview ##

|#Endpoint Group|#Description
|Info|Contains endpoints for obtaining list of formats supported by GroupDocs.Comparison Cloud, and getting basic information about document and its pages
|Compare|Contains main product endpoint for document comparison
|File|Contains endpoints for upload, download, copy, move, delete files in the storage
|Folder|Contains endpoints for create, copy, move, delete folders in the storage
|Storage|Contains endpoints for obtaining storage information and file information

## Security and Authentication ##

The GroupDocs.Comparison Cloud API is secured and requires authentication. Developers can [create]({{< ref "total\getting-started\ui-topics\create-new-app-and-get-app-key-and-sid.md" >}})) an app access key ID (appSID) and app secret access key when they [register]({{< ref "total\getting-started\ui-topics\creating-and-managing-account.md" >}})). Authenticated requests require a signature and AppSID query parameters or OAuth 2.0 authorization header. You can see complete detail [here]({{< ref "total\getting-started\overview-rest-api\authenticating-api-requests.md" >}})).

## SDKs ##

Checkout our GitHub [repository](https://github.com/groupdocs-comparison-cloud) for a complete list of GroupDocs.Comparison Cloud SDKs along with working examples, to get you started in no time. 

At the moment following SDKs are provided: 

* .NET ([Sources](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-dotnet), [NuGet Package](https://www.nuget.org/packages/GroupDocs.Comparison-Cloud), [samples](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-dotnet-samples))
* Java ([Sources](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-java), [Jar](https://repository.groupdocs.cloud/webapp/#/artifacts/browse/tree/General/repo/com/groupdocs/groupdocs-comparison-cloud), [samples](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-java-samples))
* PHP ([Sources](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-php), [samples](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-php-samples))
* Node.js ([Sources](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-node), [samples](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-node-samples))
* Python ([Sources](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-python), [samples](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-python-samples))
* Ruby ([Sources](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-ruby), [samples](https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-ruby-samples))

## API Explorer ##

The easiest way to try out our API right away in your browser! With the [GroupDocs Cloud Web API explorer](https://apireference.groupdocs.cloud/comparison/). This is a collection of Swagger documentation for the GroupDocs for Cloud APIs. You can get information about all the resources in the API. It also provides testing and interactivity to our API endpoint documentation.