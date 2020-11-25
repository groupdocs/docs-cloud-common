---
id: "configure-google-drive-storage"
url: "total/configure-google-drive-storage"
title: "Configure Google Drive Storage"
productName: "GroupDocs.Total Cloud"
weight: 1
description: ""
keywords: ""
---

You have to complete following steps to connect a Google Drive Storage:

# Google Drive Configurations

* Create Google account if you don't have one (Google Plus account can be used)
* (Optional) Install Google Drive application at your PC (see [https://drive.google.com](https://drive.google.com))
* Go to Google API console: [https://code.google.com/apis/console](https://code.google.com/apis/console)
* Create a new Project\
![](total/images/GoogleDriveCreateProject_1.PNG)

* In "APIs & Services" menu Enable Google Drive API\
![](total/images/GoogleDriveEnableAPIs_2.PNG)\
![](total/images/GoogleDriveEnableAPIs_3.PNG)

* Go to Credential options and add information in OAuth consent screen\
![](total/images/GoogleDriveCredential_4.PNG)

* Create "OAuth client ID" API credentials\
![](total/images/GoogleDriveCredential_5.PNG)

* Select Web Application and More options
* Add https://dashboard.groupdocs.cloud/storages/googledrive/callback to Authorized Redirect URIs\
![](total/images/GoogleDriveCredential_6.PNG)

* Push Create button

# GroupDocs Cloud Configuration

* Open [Dashboard](https://dashboard.groupdocs.cloud)
* Access the [Storages](https://dashboard.groupdocs.cloud/storages) page
* Click on the 'Create New Storage' and select [Google Drive Storage](https://dashboard.groupdocs.cloud/storages/googledrive/create)\
![](total/images/ThirdPartyStorageList.PNG)

* Enter Storage Name, Client Id and Client secret from the generated Client Id at Google console
* Push Generate Refresh Token button
* Allow access:\
![](total/images/GoogleDriveAccess_7.PNG)

* Save Storage

Now you can use it by its name in the service API with this account.
