---
weight: 5
id: "conversion-api"
title: "Working with Conversion API"
url: "conversion/conversion-api"
---





 

## Document Conversion API ##

This API intended for convert the document to specified target format. 

#### URI ####

```html 

~/

 ```

#### HTTP POST ####

#### Example 2 (Convert document) ####

Takes  as input and returns .

###### Example URL ######

```html 

https://api.groupdocs.cloud/v2.0/conversion

 ```

###### Example Request  ######

```html 

{
  "FilePath": "/words/docx/one-page.docx",
  "Format": "pdf",
  "OutputPath": "converted"
}

 ```

###### Example Response ######

```html 

[
  {
    "name": "one-page.pdf",
    "size": 17958,
    "url": "converted/one-page.pdf"
  }
]

 ```