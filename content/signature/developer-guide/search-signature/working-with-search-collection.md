---
weight: 4
id: "working-with-search-collection"
title: "Working with Search Collection"
url: "signature/working-with-search-collection"
---

{{< alert style="info" >}}
Note:  The features listed on this page are supported only in GroupDocs.Signature Cloud V1
{{< /alert >}}










# Introduction #

GroupDocs.Signature Cloud REST API supports to search multiple signatures in a document. For example, you can search whether a document contains Text and Barcode Signatures at same time. To search list of signatures on document (Cells, Images, PDF, Slides or Words) Signature API provides an object **[SearchOptionsCollectionData]({{< ref "signature/developer-guide/common-resources/search-options-objects.md" >}})** that can contain one or more search options. Please, use search options which appropriate for current document format.

# Search Multiple Signatures on Document #

You can search multiple Signatures on Document at same time provided by fileName and document folder (if required) using following API. It expects [SearchOptionsCollectionData]({{< ref "signature/developer-guide/common-resources/search-options-objects.md" >}}) object data in request body. You can add required search options to this object as per your document format.

It returns an object which contains document name, folder location and search result.

## Resource ##

The following GroupDocs.Signature Cloud REST API resource has been used in the example [to search multiple signatures in a document](https://apireference.groupdocs.cloud/signature/#!/Search/PostSearchCollection).

## cURL Example ##





 Request

```html 
curl --request POST \
--url http://api.groupdocs.cloud/v1/signature/SignedForVerificationAll.pdf/collection/search?folder#signed \
--header 'authorization: [Access Token]' \
--header 'content-type: application/json' \
--data '{ "items": [ { "barcodeTypeName": "Code39Standard", "text": "123456789012", "matchType": "Contains", "documentPageNumber": 1, "pagesSetup": { "firstPage": true, "lastPage": false, "oddPages": false, "evenPages": false, "pageNumbers": [  1 ] }, "searchAllPages": true, "OptionsType": "PdfSearchBarcodeOptionsData" }, { "documentPageNumber": 1, "pagesSetup": { "firstPage": true, "lastPage": false, "oddPages": false, "evenPages": false, "pageNumbers": [  1 ] }, "searchAllPages": true, "OptionsType": "PdfSearchDigitalOptionsData" } ] }'

 ```




 Response

```html 
{
  "signatures": [
    {
      "barcodeTypeName": "Code39Standard",
      "text": "123456789012",
      "signatureType": "PdfBarcodeSignatureData"
    },
    {
      "comments": "",
      "isValid": false,
      "digitalSignatureType": 0,
      "signTime": "2018-03-13T21:37:04",
      "signatureType": "PdfDigitalSignatureData"
    }
  ],
  "fileName": "SignedForVerificationAll.pdf",
  "folder": "pdf",
  "code": 200,
  "status": "OK"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-signature-cloud).

### Search Multiple Signatures ###





 C#




{{< gist groupdocscloud e1e1480f327b6a0982bc1ecc3768718f Signature_CSharp_Search_Collection.cs >}}







 PHP




{{< gist groupdocscloud a43adea6e4f64b33ea37ead904a401cb Signature_Php_Search_Collection.php >}}







 Java




{{< gist groupdocscloud d95398adbee451da9981705cf5c6ad7f Signature_Java_Search_Collection.java >}}







 Python




{{< gist groupdocscloud e967ad642d9e6e11f123064b9292e12e Signature_Python_Search_Collection.py >}}







 Ruby




{{< gist groupdocscloud 1a0d1223161ccb6a2157dcef82c39c37 Signature_Ruby_Search_Collection.rb >}}









# Search Multiple Signatures on Document at Provided URL #

You can search multiple Signatures on Document at same time from specified  file URL and document folder (if required) using following API. It expects [SearchOptionsCollectionData]({{< ref "signature/developer-guide/common-resources/search-options-objects.md" >}}) object data in request body. You can add required search options to this object as per your document format.

It returns an object which contains document name, folder location and search result.

## Resource ##

The following GroupDocs.Signature Cloud REST API resource has been used in the example [to search multiple signatures in a document at provided url](https://apireference.groupdocs.cloud/signature/#!/Search/PostSearchCollectionFromUrl).

## cURL Example ##





 Request

```html 
curl --request POST \
--url http://api.groupdocs.cloud/v1/signature/collection/verification?url#https%3a%2f%2fwww.dropbox.com%2fs%2fumokluz338w4ng7%2fone-page.docx%3fdl%3d1 \
--header 'authorization: [Access Token]' \
--header 'content-type: application/json' \
--data '{ "items": [ { "barcodeTypeName": "Code39Standard", "text": "123456789012", "matchType": "Contains", "documentPageNumber": 1, "pagesSetup": { "firstPage": true, "lastPage": false, "oddPages": false, "evenPages": false, "pageNumbers": [  1 ] }, "searchAllPages": true, "OptionsType": "PdfSearchBarcodeOptionsData" }, { "documentPageNumber": 1, "pagesSetup": { "firstPage": true, "lastPage": false, "oddPages": false, "evenPages": false, "pageNumbers": [  1 ] }, "searchAllPages": true, "OptionsType": "PdfSearchDigitalOptionsData" } ] }'

 ```




 Response

```html 
{
  "signatures": [
    {
      "barcodeTypeName": "Code39Standard",
      "text": "123456789012",
      "signatureType": "PdfBarcodeSignatureData"
    },
    {
      "comments": "",
      "isValid": false,
      "digitalSignatureType": 0,
      "signTime": "2018-03-13T21:37:04",
      "signatureType": "PdfDigitalSignatureData"
    }
  ],
  "fileName": "SignedForVerificationAll.pdf",
  "folder": "pdf",
  "code": 200,
  "status": "OK"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-signature-cloud).

### Search Multiple Signatures on Document at Provided URL ###

 





 C#




{{< gist groupdocscloud e1e1480f327b6a0982bc1ecc3768718f Signature_CSharp_Search_Collection_FromUrl.cs >}}







 PHP




{{< gist groupdocscloud a43adea6e4f64b33ea37ead904a401cb Signature_Php_Search_Collection_URL.php >}}







 Java




{{< gist groupdocscloud d95398adbee451da9981705cf5c6ad7f Signature_Java_Search_Collection_FromUrl.java >}}







 Python




{{< gist groupdocscloud e967ad642d9e6e11f123064b9292e12e Signature_Python_Search_Collection_FromUrl.py >}}







 Ruby




{{< gist groupdocscloud 1a0d1223161ccb6a2157dcef82c39c37 Signature_Ruby_Search_Collection_FromUrl.rb >}}







