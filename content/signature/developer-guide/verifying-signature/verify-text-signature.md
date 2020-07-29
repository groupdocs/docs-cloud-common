---
id: "verify-text-signature"
url: "signature/verify-text-signature"
title: "Verify Text Signature"
productName: "GroupDocs.Signature Cloud"
weight: 1
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed on this page are supported only in GroupDocs.Signature Cloud V1
{{< /alert >}}










# Introduction #

GroupDocs.Signature Cloud REST API supports to verify a signed document. It provides methods to verify Text Signature in Documents Pages with different options for page number, text and search criteria by using [doc:signaturecloud.Verification Options Objects) data in request body.

# Verify Text Signature in a Document #

You can verify Text Signature in a Document using this API. It expects [doc:signaturecloud.Verification Options Objects) data in request body. It returns object which contains result of verification process. The field Result keeps flag if verification processed successfully.

## Resource ##

The following GroupDocs.Signature Cloud REST API resource has been used [to verify Text signature in a document](https://apireference.groupdocs.cloud/signature/#!/Verification/PostVerificationText) example.

## cURL Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/signature/Signed_Text.pdf/text/verification?Folder#signed" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"DocumentPageNumber":1,"Text":"1234567890","VerifyAllPages":true,"OptionsType":"PdfVerifyTextOptionsData"}" \
-H "authorization: Bearer rf1Wyp3-Cz_xukjKqvzF-OMwYvhJcl0rJ6CQ0IgQbZwdSGTKYJziBpGNeDdzGSwwXgsRLCCfPLhHJBKPv8dzqX3tGA8n8SA4tXhLdnGh-hws2gQgmCWEjF0RpzEdJA6jh6tGZyOSAa2GlTrLhuflBwjMB5-dc8JwRmI-ssOiXkO3fSRxnwWuWih24Co8-n8elsun4HxZVMqCzXepAiXBV9UBeUktV_PLclri_lTJEnDzoJRzfRyDigjb2-luODo9aX8DFseboggoCIMKDoyLPSVHnFXgs5EWV2aQ_DgRm_D6UPn2T1Gn7OAIe-T8aA7ypDCoR-wuTJdB8o7T0f2I8K-8FrXCy2Sgb8B5QPpAOcLdiBBqFxRdk8f2c67J-rSbm2WUPWK65pbLa8NGHHdIRKuiI87NmphWuKc39a_zcgEg4MnHSlDeephmStnLS8OayQObNdLQBYAmoeQeVpZRy9t9bcU"
 ```




 Response

```html 
{
  "result": true,
  "fileName": "Signed_Text.pdf",
  "folder": "signed",
  "code": 200,
  "status": "OK"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-signature-cloud).

### Verify Text Signature in a Document ###





 C#




{{< gist groupdocscloud e1e1480f327b6a0982bc1ecc3768718f Signature_CSharp_Verify_Signature_Text.cs >}}







 PHP




{{< gist groupdocscloud a43adea6e4f64b33ea37ead904a401cb Signature_Php_Signature_Text_Verify.php >}}







 Java




{{< gist groupdocscloud d95398adbee451da9981705cf5c6ad7f Signature_Java_Verify_Signature_Text.java >}}







 Python




{{< gist groupdocscloud e967ad642d9e6e11f123064b9292e12e Signature_Python_Verify_Signature_Text.py >}}







 Ruby




{{< gist groupdocscloud 1a0d1223161ccb6a2157dcef82c39c37 Signature_Ruby_Signature_Signature_Text.rb >}}









# Verify Text Signature in a Document at Provided URL #

GroupDocs.Signature Cloud REST API supports to verify Text Signature for document at provided URL with [doc:signaturecloud.Verification Options Objects). The API retrieves file from specified URL and tries to detect file type when fileName parameter is not specified. It expects [doc:signaturecloud.Verification Options Objects)  data in request body. Based on passed Verification Options settings proceeds with Document verification and returns object which contains result of verification process. The field Result keeps flag if verification processed successfully.

## Resource ##

The following GroupDocs.Signature Cloud REST API resource has been used in the example [to verify Text signature in a document at provided URL](https://apireference.groupdocs.cloud/signature/#!/Verification/PostVerificationTextFromUrl).

## cURL Example ##





 Request

```html 
curl -v "https://api-qa.groupdocs.cloud/v1/signature/text/verification?url#https%3A%2F%2Fwww.dropbox.com%2Fs%2Fbzx1xm68zd0c910%2FPieChart.docx" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"DocumentPageNumber":1,"Text":"coca cola","VerifyAllPages":true,"OptionsType":"WordsVerifyTextOptionsData"}" \
-H "authorization: Bearer ku1wBVYory9t4m9MOW0VuEKbyT4GYUZy8hTXpirhs6ECV_3dQhlbwLHn8ffsX650Syt0hDq2vXZNia70T1NY0jG32h_LUxQoRrVQMvV88P5Y0EbmBinPsmEAuqFHCR2ahhWJqZhidpXU7tP_PHh5IXuZ-cmmW1VUARtj73oE-B4gyD8WEJ1i0CgEM8-Do2843TpCgueqczRgCikeKy8ftSjhgNr2HfYGIc8Fjn152yE3o-wi2VvYwRmEquF28di-zDCxVcZa742ENp9d5GLs1obG8Y-pf-FwQDFcvj-XreWt9U1_dNbTaRiREsrliisAxFAM7qUG1zRZpNISX_kEYC6NqaLlebMIAd5-WHL_PeK2reld-DMURVsniqsgHSxNRnQpmxoJ-YVeQQeN7ZoMBrI4G3zWMeRrUwWR2UmS4jfBlckpfCjkvGZ7ydbzWp3qkLmE3Ns95uf1ccJuvESN9yWkUmg"
 ```




 Response

```html 
{
  "result": false,
  "fileName": "https://www.dropbox.com/s/bzx1xm68zd0c910/PieChart.docx",
  "folder": "",
  "code": 200,
  "status": "OK"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-signature-cloud).

### Verify Text Signature in a Document at Provided URL ###





 C#




{{< gist groupdocscloud e1e1480f327b6a0982bc1ecc3768718f Signature_CSharp_Verify_Signature_Text_URL.cs >}}







 PHP




{{< gist groupdocscloud a43adea6e4f64b33ea37ead904a401cb Signature_Php_Signature_Text_Verify_URL.php >}}







 Java




{{< gist groupdocscloud d95398adbee451da9981705cf5c6ad7f Signature_Java_Verify_Signature_Text_URL.java >}}







 Python




{{< gist groupdocscloud e967ad642d9e6e11f123064b9292e12e Signature_Python_Verify_Signature_Text_URL.py >}}







 Ruby




{{< gist groupdocscloud 1a0d1223161ccb6a2157dcef82c39c37 Signature_Ruby_Signature_Signature_Text_URL.rb >}}







