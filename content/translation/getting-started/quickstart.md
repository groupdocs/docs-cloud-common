---
weight: 4
id: "quickstart"
title: "Quickstart"
url: "translation/quickstart"
---

####   ####

#### Create an account ####

Creating an account is very simple. Go to [https://dashboard.groupdocs.cloud](https://dashboard.groupdocs.cloud) to create a free account.


#### Get App Key and SID ####

Before you can make any requests to GroupDocs Cloud API you need to get APP SID and APP key (secret key). This will be used to invoke the GroupDocs Cloud API.

You can get it from the default Application or create a new Application. For further details see [Create New App and Get App Key and SID]({{< ref "translation\getting-started\create-new-app-and-get-app-key-and-sid.md" >}})


#### Get your JWT token ####

After you have created a new application you can obtain a JWT token. See [JSON Web Token Authentication]({{< ref "translation\getting-started\json-web-token-authentication.md" >}}) for further details.


#### Call Rest API ####

When you’ve got your access_token your can make Rest API call by adding to Headers of your request:

* Authorization: Bearer access_token

##### To translate plain text #####

###### cURL ######


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



###### SDKs ######


 C#




{{< gist groupdocscloud ffdd7c22bdf290769f6aa83bb870a80d Translation_CSharp_Translate_Text.cs >}}






##### To translate document #####

###### cURL ######


 Request

```html 
curl -X POST "https://api.groupdocs.cloud/v1.0/translation/document" \
-H "Authorization: Bearer TOKEN" \
-H "Content-Type: application/json" \
-d '[{"format": "docx", "pair": "en-fr", "name": "test.docx", "folder": "", "savepath": "", "savefile": "translated.docx", "storage": "First Storage"}]'

 ```


 Response

```html 
{
    "status": "ok",
    "message": "word file saved successfully"
}

 ```



###### SDKs ######


 C#




{{< gist groupdocscloud ffdd7c22bdf290769f6aa83bb870a80d Translation_CSharp_Translate_Document.cs >}}




