---
weight: 9
id: "searchresult"
title: "SearchResult"
url: "signature/searchresult"
---

# SearchResult #

SearchResult data structure returned by  as output result

##### SearchResult example #####

```html 

{
  "FileInfo": {
    "FilePath": "/words/docx/one-page.docx",
    "Password" : "1234567890"
  },
  "Size" : 12345,
  "Signatures": "true"
}

 

 ```

##### SignResult fields #####

|Name|Description
|---|---
|FilePath|Name of the verified document
|Size|Size of the verified document
|IsSuccess|Result of verification process
|Signatures|Array of found Signatures that match for passed Search Options.

Based of found signature type of one the following data structures will be created





