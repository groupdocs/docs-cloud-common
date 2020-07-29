---
id: "image-representation-of-document-pages"
url: "annotation/image-representation-of-document-pages"
title: "Image Representation of Document Pages"
productName: "GroupDocs.Annotation Cloud"
weight: 3
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this page are working only with GroupDocs.Annotation Cloud V1
{{< /alert >}}






# Introduction #

GroupDocs.Annotation Cloud API supports to render the document pages to images and retrieves images link. Following APIs are provided for the purpose. 

# Generate Images of Document Pages #

This API generates images of the document pages and returns links to generated images.

## Resource ##

The following GroupDocs.Annotation Cloud REST API resource has been used to generate [images of document pages](https://apireference.groupdocs.cloud/annotation/#!/ImagePages/PostPages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/annotation/Annotated.pdf/image/pages" \
-X POST \
-H "Content-Type: application/json" -H "Accept: application/json" \
-d "{}" \
-H "authorization: Bearer 0v7TK3UGYjVBEcEIS9aaO0dsXAlt-KriIDnJGkDIPktFmuu6xIuou2-eVUD4-Td9TcToDvShk9w02pWIXvyEdstxDqjSa8L2K4Pk2zgNkAoEDgDeFlpWf0k7lZ8guqUm43eAKQf43MVNyr3L6P3w1e2l9j-RJx-btpPorcZ90xY8S_b1vySsKsUxOlnwYtWc01JEXlO7TNrmfD3Eek4ch-xzi-qe4V8nofmy7RbqwHNczeP7O_9bMi1eQ68b3Rprqd4UvDCj3gqTMyAaqd-I58lJzZsHRnbZoM7icIjVQyu02bRgx7meoXB8fIWmOkUfUkiGTT3IjI4NSmARxrPPwgp2LAv-N_9H0q3nxxfZDV1vHZQP--I6vgC2UHo-YPw-mB4WRVHsUKqq04L4pdR4pCIWuluus_ydjVH_ndJlqP843eL3glt1XJez3DgXQIbHiAnqBBDqZqSZZDVUYhLDq1jN9eM" 
 ```




 Response

```html 
{
  "totalCount": 2,
  "entries": [
    {
      "number": 0,
      "link": {
        "href": "http://api.groupdocs.cloud/storage/file/Annotated_pdf/i/0.png",
        "rel": "self",
        "type": null,
        "title": null
      }
    },
    {
      "number": 1,
      "link": {
        "href": "http://api.groupdocs.cloud/storage/file/Annotated_pdf/i/1.png",
        "rel": "self",
        "type": null,
        "title": null
      }
    }
  ]
} 
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-annotation-cloud).

### Generate Images of Document Pages ###





 C#




{{< gist groupdocscloud 024c8d6fda257f009f47dd55141c959f Annotation_CSharp_Post_Generate_Image_Pages.cs >}}







 PHP




{{< gist groupdocscloud 91cf9bb641d8b967c65ee1f2eb626f2e Annotation_PHP_Post_Generate_Image_Pages.php >}}







 Java




{{< gist groupdocscloud dd069ea3659b158b48e2239356aea189 Annotation_Java_Post_Generate_Image_Pages.java >}}







 Ruby




{{< gist groupdocscloud 6a14ecd45b4278c014689b688ec34d21 Annotation_Ruby_Generate_Pages.rb >}}









# Get Links to Images of Document Pages #

This API retrieves links to previously generated images of document pages.

## Resource ##

The following GroupDocs.Annotation Cloud REST API resource has been used to get [links to previously generated images of document pages](https://apireference.groupdocs.cloud/annotation/#!/ImagePages/GetPages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/annotation/Annotated.pdf/image/pages" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer 0v7TK3UGYjVBEcEIS9aaO0dsXAlt-KriIDnJGkDIPktFmuu6xIuou2-eVUD4-Td9TcToDvShk9w02pWIXvyEdstxDqjSa8L2K4Pk2zgNkAoEDgDeFlpWf0k7lZ8guqUm43eAKQf43MVNyr3L6P3w1e2l9j-RJx-btpPorcZ90xY8S_b1vySsKsUxOlnwYtWc01JEXlO7TNrmfD3Eek4ch-xzi-qe4V8nofmy7RbqwHNczeP7O_9bMi1eQ68b3Rprqd4UvDCj3gqTMyAaqd-I58lJzZsHRnbZoM7icIjVQyu02bRgx7meoXB8fIWmOkUfUkiGTT3IjI4NSmARxrPPwgp2LAv-N_9H0q3nxxfZDV1vHZQP--I6vgC2UHo-YPw-mB4WRVHsUKqq04L4pdR4pCIWuluus_ydjVH_ndJlqP843eL3glt1XJez3DgXQIbHiAnqBBDqZqSZZDVUYhLDq1jN9eM"
 ```




 Response

```html 
{
  "totalCount": 2,
  "entries": [
    {
      "number": 0,
      "link": {
        "href": "http://api.groupdocs.cloud/storage/file/Annotated_pdf/i/0.png",
        "rel": "self",
        "type": null,
        "title": null
      }
    },
    {
      "number": 1,
      "link": {
        "href": "http://api.groupdocs.cloud/storage/file/Annotated_pdf/i/1.png",
        "rel": "self",
        "type": null,
        "title": null
      }
    }
  ]
} 
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-annotation-cloud).

### Get Links to Images of Document Pages ###





 C#




{{< gist groupdocscloud 024c8d6fda257f009f47dd55141c959f Annotation_CSharp_Get_Image_Pages.cs >}}







 PHP




{{< gist groupdocscloud 91cf9bb641d8b967c65ee1f2eb626f2e Annotation_PHP_Get_Image_Pages.php >}}







 Java




{{< gist groupdocscloud dd069ea3659b158b48e2239356aea189 Annotation_Java_Get_Image_Pages.java >}}







 Ruby




{{< gist groupdocscloud 6a14ecd45b4278c014689b688ec34d21 Annotation_Ruby_Get_Image_Pages.rb >}}









# Get Link to Image of Specific Page #

This API retrieves the link to previously generated image by page number of the document pages

## Resource ##

The following GroupDocs.Annotation Cloud REST API resource has been used to get [link to image of specific page of the document](https://apireference.groupdocs.cloud/annotation/#!/ImagePages/GetPages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/annotation/Annotated.pdf/image/pages/1" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer 0v7TK3UGYjVBEcEIS9aaO0dsXAlt-KriIDnJGkDIPktFmuu6xIuou2-eVUD4-Td9TcToDvShk9w02pWIXvyEdstxDqjSa8L2K4Pk2zgNkAoEDgDeFlpWf0k7lZ8guqUm43eAKQf43MVNyr3L6P3w1e2l9j-RJx-btpPorcZ90xY8S_b1vySsKsUxOlnwYtWc01JEXlO7TNrmfD3Eek4ch-xzi-qe4V8nofmy7RbqwHNczeP7O_9bMi1eQ68b3Rprqd4UvDCj3gqTMyAaqd-I58lJzZsHRnbZoM7icIjVQyu02bRgx7meoXB8fIWmOkUfUkiGTT3IjI4NSmARxrPPwgp2LAv-N_9H0q3nxxfZDV1vHZQP--I6vgC2UHo-YPw-mB4WRVHsUKqq04L4pdR4pCIWuluus_ydjVH_ndJlqP843eL3glt1XJez3DgXQIbHiAnqBBDqZqSZZDVUYhLDq1jN9eM"
 ```




 Response

```html 
{
  "number": 1,
  "link": {
    "href": "http://api.groupdocs.cloud/storage/file/Annotated_pdf/i/1.png",
    "rel": "self",
    "type": null,
    "title": null
  }
} 
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-annotation-cloud).

### Get Link to Specific Page of the Document ###





 C#




{{< gist groupdocscloud 024c8d6fda257f009f47dd55141c959f Annotation_CSharp_Get_Image_Page.cs >}}







 PHP




{{< gist groupdocscloud 91cf9bb641d8b967c65ee1f2eb626f2e Annotation_PHP_Get_Image_Page.php >}}







 Java




{{< gist groupdocscloud dd069ea3659b158b48e2239356aea189 Annotation_Java_Get_Image_Page.java >}}







 Ruby




{{< gist groupdocscloud 6a14ecd45b4278c014689b688ec34d21 Annotation_Ruby_Get_Image_Page.rb >}}









# Clear Document Image Pages Cache #

This API clears the previously generated images of document pages. It returns 204 code when it successfully removes the cache images.

## Resource ##

The following GroupDocs.Annotation Cloud REST API resource has been used to clear [images cache of document pages](https://apireference.groupdocs.cloud/annotation/#!/ImagePages/DeletePages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/annotation/Annotated.pdf/image/pages?folder#Output" \
-X DELETE \
-H "Content-Type: application/json" \
-H "authorization: Bearer 0v7TK3UGYjVBEcEIS9aaO0dsXAlt-KriIDnJGkDIPktFmuu6xIuou2-eVUD4-Td9TcToDvShk9w02pWIXvyEdstxDqjSa8L2K4Pk2zgNkAoEDgDeFlpWf0k7lZ8guqUm43eAKQf43MVNyr3L6P3w1e2l9j-RJx-btpPorcZ90xY8S_b1vySsKsUxOlnwYtWc01JEXlO7TNrmfD3Eek4ch-xzi-qe4V8nofmy7RbqwHNczeP7O_9bMi1eQ68b3Rprqd4UvDCj3gqTMyAaqd-I58lJzZsHRnbZoM7icIjVQyu02bRgx7meoXB8fIWmOkUfUkiGTT3IjI4NSmARxrPPwgp2LAv-N_9H0q3nxxfZDV1vHZQP--I6vgC2UHo-YPw-mB4WRVHsUKqq04L4pdR4pCIWuluus_ydjVH_ndJlqP843eL3glt1XJez3DgXQIbHiAnqBBDqZqSZZDVUYhLDq1jN9eM"
 ```




 Response

```html 
204 No Content 
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-annotation-cloud).

###  Clear Images Cache of Document Pages ###





 C#




{{< gist groupdocscloud 024c8d6fda257f009f47dd55141c959f Annotation_CSharp_Delete_Image_Pages.cs >}}







 PHP




{{< gist groupdocscloud 91cf9bb641d8b967c65ee1f2eb626f2e Annotation_PHP_Delete_Image_Pages.php >}}







 Java




{{< gist groupdocscloud dd069ea3659b158b48e2239356aea189 Annotation_Java_Delete_Image_Pages.java >}}







 Ruby




{{< gist groupdocscloud 6a14ecd45b4278c014689b688ec34d21 Annotation_Ruby_Get_Delete_Annotation.rb >}}







