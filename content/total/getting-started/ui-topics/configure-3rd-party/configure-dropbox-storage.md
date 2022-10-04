---
id: "configure-dropbox-storage"
url: "total/configure-dropbox-storage"
title: "Configure DropBox Storage"
productName: "GroupDocs.Total Cloud"
weight: 1
description: ""
keywords: ""
---

You have to complete following steps to configure Dropbox Storage:

* Log into [Dashboard](https://dashboard.groupdocs.cloud)
* Access the [Storages](https://dashboard.groupdocs.cloud/storages) Page
* Select [DropBox Storage](https://dashboard.groupdocs.cloud/storages/dropbox/create) from the 'Create New Storage' menu
* Enter **Storage Name** (For example: MyDropboxStorage) and click on **Generate Token** button
* Log into Dropbox and Authorize our app
* Dropbox will generate your Access Token and you will be redirected to our Dashboard
* Press **Save** button to create storage

Now you can use this storage with GroupDocs REST APIs. For example:

https://api.groupdocs.cloud/v2.0/conversion/info?FilePath=testfile.txt&StorageName=MyDropboxStorage
