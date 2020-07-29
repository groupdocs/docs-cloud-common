---
id: "overview-rest-api"
url: "total/overview-rest-api"
title: "Overview of GroupDocs for Cloud REST API"
productName: "GroupDocs.Total Cloud"
weight: 1
description: ""
keywords: ""
---






## Introduction ##

This document outlines the design of a REST-based API for GroupDocs for Cloud, it covers both the structure of REST URLs as well as specific behavior linked to the API such as Authentication, Request Queuing, and Storage. The GroupDocs for Cloud API will give developers access to all the key functions of the [downloadable GroupDocs componenets](https://www.groupdocs.com/) through a Software as a Service hosted model.

There will be 3 sub-components within the API design (although these are largely transparent to the end-user);

* Platform - this covers elements of the GroupDocs for Cloud platform, not directly linked to file format manipulation, such as Storage, Authentication, Queuing, etc;
* Common - this covers common elements of the API which are shared by all products;
* Product - this covers product specific areas for each product;
** GroupDocs.Viewer Cloud
** GroupDocs.Annotation Cloud
** GroupDocs.Conversion Cloud
** GroupDocs.Comparison Cloud
** GroupDocs.Signature Cloud
** GroupDocs.Storage Cloud

## API Basics ##

The GroupDocs for Cloud API is a REST-based API for wide usability on the web across platforms. By default, the REST API returns XML formatted responses, but it is possible to get the response in JSON format by setting Content-Type to **application/json**. Accompanying the REST API will be Client SDKs for all major development platforms which will provide client libraries to make it very easy for developers to code against the GroupDocs for Cloud APIs.

#### Base URL ####

GroupDocs for Cloud API requests are made by sending a correctly constructed HTTP requests to the following address, with arguments being generally submitted as **HTTP** **get** or **post** arguments and data files being sent as **HTTP** **post** method where necessary.

```html 

https://api.groupdocs.cloud/*

 ```

#### Versions ####

Each version beginning with 1.0 will have its number as a part of the URL. So the next URLs are used for the first version:

```html 

https://api.groupdocs.cloud/v1/*

 ```

#### Routes ####

Each product uses its own URL route (key word) to separate its interface:

1. 
File storage uses **storage** and sub routes **file** and **folder** for files and folders manipulation correspondingly;

```html 

https://api.groupdocs.cloud/v1/storage

 ```

1. 
GroupDocs.Viewer for Cloud uses **viewer** route;

```html 

https://api.groupdocs.cloud/v1/viewer

 ```

1. 
GroupDocs.Annotation for Cloud uses **annotation** route;

```html 

https://api.groupdocs.cloud/v1/annotation

 ```

1. 
GroupDocs.Conversion for Cloud uses **conversion** route;

```html 

https://api.groupdocs.cloud/v1/conversion

 ```

1. 
GroupDocs.Comparison uses **comparison** route;

```html 

https://api.groupdocs.cloud/v1/comparison

 ```

1. 
GroupDocs.Signature uses **signature** route;

```html 

https://api.groupdocs.cloud/v1/signature

 ```


Folders

Each user's application has its own root folder at the server, but any number of subfolders at different levels can be created as well. File storage considers folders as resources and gets the folder or file path as a part of URL:

```html 

https://api.groupdocs.cloud/v1/folder/subfolder/subsubfolder/file.txt

 ```


where the file relative to application root folder path is folder/subfolder/subsubfolder/file.txt. See e.g. [doc:asposezarchivedjava.Folder) for additional details.

While product services get the folder path as a query string folder parameter.

#### URI Structure ####

Within the API we will have Resources (each identified by a URI) and Operations (as much as possible covered by the 4 HTTP Methods: GET, POST, PUT and DELETE) which can be applied to those resources.

Default 'empty' request [http:~~/~~/api.groupdocs.cloud/v1](http://api.groupdocs.cloud/) redirects to service start page with a link to some helpful examples. Please check following articles for information regarding Request and Response Format and how to authenticate GroupDocs for Cloud API request.



