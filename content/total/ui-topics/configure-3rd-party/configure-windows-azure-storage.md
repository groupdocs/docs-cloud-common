---
id: "configure-windows-azure-storage"
url: "total/configure-windows-azure-storage"
title: "Configure Windows Azure Storage"
productName: "GroupDocs.Total Cloud"
weight: 1
description: ""
keywords: ""
---

You have to complete following steps to configure the Storage:

* Create Azure account if you don't have one
* Log into [Dashboard](https://dashboard.groupdocs.cloud)
* Access the [Storages](https://dashboard.groupdocs.cloud/storages) page
* Click on the 'Create New Storage' and select [Azure Storage](https://dashboard.groupdocs.cloud/storages/googledrive/create)
* Enter Storage Name (For example: MyAzureStorage), Container, Account name, Account key, and Connection from your Azure account
* Save Storage

Now you can use it by its name in the service API with this account. For example:

https://api.groupdocs.cloud/v2.0/conversion/info?FilePath=testfile.txt&StorageName=MyAzureStorage
