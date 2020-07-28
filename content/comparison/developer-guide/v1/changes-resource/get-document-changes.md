---
weight: 1
id: "get-document-changes"
title: "Get Document - Changes"
url: "comparison/get-document-changes"
---






# Get Document (Changes) #

You can compare documents and update the changes (Accept/Reject)  by providing the [JsonRequest Object]({{< ref "comparison\developer-guide\v1\common-resources\jsonrequest-fields-description.md" >}}) data in request body.

## Resource ##

The following GroupDocs.Comparison Cloud REST API resource has been used to [get document (changes)](https://apireference.groupdocs.cloud/comparison/#!/Changes/PutChangesDocument).

## cURL REST Example ##





 Request

```html 
curl -v  "https://api.groupdocs.cloud/v1.0/comparison/compareDocuments/changes/update?outPath#comparisons%2Foutput.docx&#x26;appsid#XXXX&#x26;signature#XXX-XX"  
-H "Content-Type: application/json" 
-X PUT -d  "{'sourceFile':{'folder':'comparisons','name':'source.docx','password':''},'targetFiles' [{'folder':'comparisons','name':'target.docx','password':''}],'settings
  ':{'generateSummaryPage':true,'showDeletedContent':true,'styleChangeDetection':true,'insertedItemsStyle':{'color':'Blue','beginSeparatorString':'','endSeparatorString':'','bold':false,'italic':false,'strikeThrough':false},'deletedItemsStyle':{'color':'Red','beginSeparatorString':'','endSeparatorString':'','bold':false,'italic':false,'strikeThrough':false},'styleChangedItemsStyle':{'color':'Green','beginSeparatorString':'','endSeparatorString':'','bold':false,'italic':false,'strikeThrough':false},'wordsSeparatorChars':[],'detailLevel':'Low','useFramesForDelInsElements':false,'calculateComponentCoordinates':false,'markDeletedInsertedContentDeep':false},'changes':[{'id':0,'action':'Accept'},{'id':1,'action':'Reject'}]}"
 ```




 Response

```html 
{
  "href": "https://api.groupdocs.cloud/storage/file/comparisons/output.docx",
  "rel": "self",
  "type": null,
  "title": null
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-comparison-cloud).

### Get Document (Changes) ###





 C#



 
{{< gist groupdocscloud 33ad9afbf76ac035c8552d2efe0ec895 Comparison_CSharp_Update_Changes_And_Get_Document.cs  >}}







 PHP



  
{{< gist groupdocscloud fb9d531a4ea5f0755dfd0e079b7801b5 Comparison_Php_Update_Changes_And_Get_Document.php >}}







 Java




{{< gist groupdocscloud dde5dbd092bef3a3ac74848342ee4f64 Comparison_Java_Get_Changes_Document.java >}}







 Ruby




{{< gist groupdocscloud 4e15a0a5e68b0d2755592a552488d1ec Comparison_Ruby_get_changes_document.rb >}}






