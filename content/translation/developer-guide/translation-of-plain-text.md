---
id: "translation-of-plain-text"
url: "translation/translation-of-plain-text"
title: "Translation Of Plain Text"
productName: "GroupDocs.Translation Cloud"
description: ""
keywords: ""
---

# Translate Plain Text API #

This API allows you to translate plain text from your request.

## API Explorer ##

[GroupDocs.Translation Cloud API Reference](https://apireference.groupdocs.cloud/translation) lets you try out [Translate Document API](https://apireference.groupdocs.cloud/translation/#/Transport/PostRunTranslationText) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Request parameters ###

|#
|---
Parameter
|#
Description

|
**userRequest**
|
String that represents list of JSONs precised in [JSON Request Details]({{< ref "translation/developer-guide/json-request-details.md" >}})). 

Required.


## cURL Example ##


 Request

```html 
curl -X POST "https://api.groupdocs.cloud/v1.0/translation/text" \
-H "Authorization: Bearer TOKEN" \
-H "Content-Type: application/json" \
-d '[{"pair": "en-fr", "text": "Welcome to Paris"}]'

 ```


 Response

```html 
{
    "status": "ok",
    "message": "Text translated successfully",
    "translation": "Bienvenue à Paris"
}

 ```



## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-translation-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-translation-cloud), it hides the [File API](https://apireference.groupdocs.cloud/translation/#/File) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###


 C#




{{< gist groupdocscloud ffdd7c22bdf290769f6aa83bb870a80d Translation_CSharp_Translate_Text.cs >}}




