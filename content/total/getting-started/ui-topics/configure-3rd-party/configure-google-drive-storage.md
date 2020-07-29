---
id: "configure-google-drive-storage"
url: "total/configure-google-drive-storage"
title: "Configure Google Drive Storage"
productName: "GroupDocs.Total Cloud"
weight: 1
description: ""
keywords: ""
---

{{< alert style="info" >}}
The page contains Google Drive Storage configuration.
{{< /alert >}}

You have to complete following steps to configure the Storage:

* Create Google account if you don't have one (Google Plus account can be used)
* Install Google Drive application at your PC (see [https://drive.google.com](https://drive.google.com))
* Go to Google API console: [https://code.google.com/apis/console](https://code.google.com/apis/console)
* Create a new Project
![](total/images/GoogleDriveCreateProject_1.PNG)
* In "APIs & Services" menu Enable Google Drive API
![](total/images/GoogleDriveEnableAPIs_2.PNG)

          ![](total/images/GoogleDriveEnableAPIs_3.PNG)

* Go to Credential options and add information in OAuth consent screen

         ![](total/images/GoogleDriveCredential_4.PNG)

* Create "OAuth client IDAPI" credentials

         ![](total/images/GoogleDriveCredential_5.PNG)

* Select Web Application and More options
* Add '[https://dashboard.groupdocs.cloud/breeze/UserData/GetGoogleDriveCallback](https://dashboard.groupdocs.cloud:9090/breeze/UserData/GetGoogleDriveCallback)' to Authorized Redirect URIs
![](total/images/GoogleDriveCredential_6.PNG)
* Push Create button
* Open [https://dashboard.groupdocs.cloud](https://dashboard.groupdocs.cloud), open My Storage
* Select Create New Storage and Google Drive Storage
![](total/images/StorageList.PNG)
* Enter Storage Name, Client ID and Client secret from generated Client ID at Google console
* Push Generate Token button
* Allow access:
![](total/images/GoogleDriveAccess_7.PNG)
* Save Storage

Now you can use it by its name in the service API with this account.