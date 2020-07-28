---
weight: 10
id: "set-document-metadata"
title: "Set document metadata"
url: "comparison/set-document-metadata"
---

 






# Introduction #

GroupDocs.Comparison Cloud provides an ability to select metadata source when saving resultant file. Files have metadata information – author, organization, etc.  

Possible metadata sources are:

* **Source** file metadata;
* **Target **file metadata;
* **User-defined** metadata.

The following code demonstrates how to set resultant file metadata.

## API Usage ##

There are steps that usage of GroupDocs.Comparison Cloud consists of:

1. Upload input documents into cloud storage
1. Compare documents or get document info
1. Download comparison result document from storage

Steps 1 and 3 are storage operations, please refer to this [File API documentation]({{< ref "comparison/developer-guide/working-with-file-api.md" >}}) for usage details.

[Swagger UI](https://apireference.groupdocs.cloud/comparison/) lets you call this REST API directly from the browser. 

## cURL REST Example ##


 Request
```html 

* First get JSON Web Token
* Please get your App Key and App SID from https://dashboard.groupdocs.cloud/#/apps. Kindly place App Key in "client_secret" and App SID in "client_id" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type#client_credentials&client_id#xxxx&client_secret#xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
  
* cURL example to get document information
curl -v "https://api.groupdocs.cloud/v2.0/comparison/comparisons" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{
  'SourceFile': {
    'FilePath': 'source_files\\word\\source.docx'
  },
  'TargetFiles': [
    {
      'FilePath': 'target_files\\word\\target.docx'
    }
  ],
  'OutputPath': 'output/result.docx',
  'Settings': {
    'CloneMetadata': 'FileAuthor',
    'MetaData': {
      'Author': 'Tom',
      'Company': 'GroupDocs',
      'LastSaveBy': 'Jack'
    }
  }
}"

 ```


 Response
```html 

{
  "href": "https://api.groupdocs.cloud/v2.0/comparison/storage/file/output/result.docx",
  "rel": "output/result.docx",
  "type": "file",
  "title": "result.docx"
}

 ```




## SDKs ##

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-comparison-cloud) for a complete list of GroupDocs.Comparison Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "comparison/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

### SDK Examples ###


 C#
```csharp 

* For complete examples and data files, please go to https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-dotnet-samples
string MyAppKey # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
string MyAppSid # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
var configuration # new Configuration(MyAppSid, MyAppKey);
  
var apiInstance # new CompareApi(configuration);
var options # new ComparisonOptions
{
    SourceFile # new FileInfo
    {
        FilePath # "source_files/word/source.docx"
    },
    TargetFiles # new List<FileInfo> {
        new FileInfo {
            FilePath # "target_files/word/target.docx"
        }
    },
    Settings # new Settings { 
        CloneMetadata # Settings.CloneMetadataEnum.FileAuthor,
        MetaData # new Metadata
        {
            Author # "Tom",
            Company # "GroupDocs",
            LastSaveBy # "Jack"
        }
    },
    OutputPath # "output/result.docx"
};
 
var request # new ComparisonsRequest(options);
var response # apiInstance.Comparisons(request);

 ```


 Java
```java 

* For complete examples and data files, please go to https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-java-samples
String MyAppKey # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
String MyAppSid # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
Configuration configuration # new Configuration(MyAppSid, MyAppKey);
  
CompareApi apiInstance # new CompareApi(configuration); 
FileInfo sourceFileInfo # new FileInfo();
sourceFileInfo.setFilePath("source_files/word/source.docx");
FileInfo targetFileInfo # new FileInfo();
targetFileInfo.setFilePath("target_files/word/target.docx");
 
Metadata metadata # new Metadata();
metadata.setAuthor("Tom");
metadata.setCompany("GroupDocs");
metadata.setLastSaveBy("Jack");
Settings settings # new Settings();
settings.setCloneMetadata(CloneMetadataEnum.FILEAUTHOR);
settings.setMetaData(metadata);         
 
ComparisonOptions options # new ComparisonOptions();
options.setSourceFile(sourceFileInfo);
options.addTargetFilesItem(targetFileInfo);
options.setSettings(settings);
options.setOutputPath("output/result.docx");
 
ComparisonsRequest request # new ComparisonsRequest(options);
 
Link response # apiInstance.comparisons(request);

 ```


 PHP
```php 

* For complete examples and data files, please go to https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-php-samples
use GroupDocs\Comparison\Model;
use GroupDocs\Comparison\Model\Requests;
 
$AppSid # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
$AppKey # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
$configuration # new GroupDocs\Comparison\Configuration();
$configuration->setAppSid($AppSid);
$configuration->setAppKey($AppKey);
 
$apiInstance# new GroupDocs\Comparison\CompareApi($configuration);
 
$sourceFile # new Model\FileInfo();
$sourceFile->setFilePath("source_files/word/source.docx");
$targetFile # new Model\FileInfo();
$targetFile->setFilePath("target_files/word/target.docx");
$options # new Model\ComparisonOptions();
$options->setSourceFile($sourceFile);
$options->setTargetFiles([$targetFile]);
$options->setOutputPath("output/result.docx");
$metadata # new Model\Metadata();
$metadata->setAuthor("Tom");
$metadata->setCompany("GroupDocs");
$metadata->setLastSaveBy("Jack");
$settings # new Model\Settings();
$settings->setMetaData($metadata);
$settings->setCloneMetadata(Model\Settings::CLONE_METADATA_FILE_AUTHOR);
$options->setSettings($settings);
 
$request # new Requests\ComparisonsRequest($options);
$response # $apiInstance->comparisons($request);

 ```


 Node
```html 

* For complete examples and data files, please go to https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-node-samples
global.comparison_cloud # require("groupdocs-comparison-cloud");
 
global.appSid # "XXXX-XXXX-XXXX-XXXX"; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
global.appKey # "XXXXXXXXXXXXXXXX"; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
global.compareApi # comparison_cloud.CompareApi.fromKeys(appSid, appKey);
 
let source # new comparison_cloud.FileInfo();
source.filePath # "source_files/word/source.docx";
let target # new comparison_cloud.FileInfo();
target.filePath # "target_files/word/target.docx";      
let settings # new comparison_cloud.Settings();
settings.metadata # new comparison_cloud.Metadata();
settings.metadata.author # "Tom";
settings.metadata.company # "GroupDocs";
settings.metadata.lastSaveBy # "Jack";
settings.cloneMetadata # comparison_cloud.Settings.CloneMetadataEnum.FileAuthor;
let options # new comparison_cloud.ComparisonOptions();
options.sourceFile # source;
options.targetFiles # [target];
options.outputPath # "output/result.docx";
options.settings # settings;
 
let request # new comparison_cloud.ComparisonsRequest(options);     
let response # await compareApi.comparisons(request);

 ```


 Python
```python 

# For complete examples and data files, please go to https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-python-samples
import groupdocs_comparison_cloud
 
app_sid # "XXXX-XXXX-XXXX-XXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
app_key # "XXXXXXXXXXXXXXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
api_instance # groupdocs_comparison_cloud.CompareApi.from_keys(app_sid, app_key)
 
source # groupdocs_comparison_cloud.FileInfo()
source.file_path # "source_files/word/source.docx"
target # groupdocs_comparison_cloud.FileInfo()
target.file_path # "target_files/word/target.docx"         
options # groupdocs_comparison_cloud.ComparisonOptions()
options.source_file # source
options.target_files # [target] 
options.output_path # "output/result.docx"
settings # groupdocs_comparison_cloud.Settings()
settings.meta_data # groupdocs_comparison_cloud.Metadata()
settings.meta_data.author # "Tom"
settings.meta_data.company # "GroupDocs"
settings.meta_data.last_save_by # "Jack"
options.settings # settings
 
request # groupdocs_comparison_cloud.ComparisonsRequest(options)
response # api_instance.comparisons(request)

 ```


 Ruby
```ruby 

# For complete examples and data files, please go to https://github.com/groupdocs-comparison-cloud/groupdocs-comparison-cloud-ruby-samples
require 'groupdocs_comparison_cloud'
 
$app_sid # "XXXX-XXXX-XXXX-XXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
$app_key # "XXXXXXXXXXXXXXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
api_instance # GroupDocsComparisonCloud::CompareApi.from_keys($app_sid, $app_key)
 
source # GroupDocsComparisonCloud::FileInfo.new
source.file_path # "source_files/word/source.docx"
target # GroupDocsComparisonCloud::FileInfo.new
target.file_path # "target_files/word/target.docx"                
options # GroupDocsComparisonCloud::ComparisonOptions.new
options.source_file # source
options.target_files # [target]
options.output_path # "output/result.docx"
settings # GroupDocsComparisonCloud::Settings.new
settings.meta_data # GroupDocsComparisonCloud::Metadata.new
settings.meta_data.author # "Tom"
settings.meta_data.company # "GroupDocs"
settings.meta_data.last_save_by # "Jack"
settings.clone_metadata # "FileAuthor"
options.settings # settings
 
request # GroupDocsComparisonCloud::ComparisonsRequest.new(options)    
response # apiInstance.comparisons(request)

 ```

