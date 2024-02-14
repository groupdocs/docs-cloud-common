---
id: "configure-amazon-s3-storage"
url: "total/configure-amazon-s3-storage"
title: "Configure Amazon S3 Storage"
productName: "GroupDocs.Total Cloud"
weight: 1
description: ""
keywords: ""
---

To use Amazon S3 storage, you have to create your own account and create a new bucket at [AWS Amazon](http://aws.amazon.com).\
Please follow [http://docs.amazonwebservices.com/AmazonS3/latest/gsg/SigningUpforS3.html](http://docs.amazonwebservices.com/AmazonS3/latest/gsg/SigningUpforS3.html) for more details.

Next, you will have to configure Amazon S3 Storage using your Aspose account at the [Dashboard](https://dashboard.groupdocs.cloud).

Please follow these steps to configure it:

* Log into [Dashboard](https://dashboard.groupdocs.cloud)
* Access the [Storages](https://dashboard.groupdocs.cloud/storages) Page
* Select [Amazon S3 Storage](https://dashboard.groupdocs.cloud/storages/amazons3/create) from the 'Create New Storage' menu
* Enter 'Storage Name' (For example: MyAmazonS3Storage)
* Enter 'Bucket' Name
* Enter 'AWS Access Key'
* Enter 'AWS Secret Key'
* Press 'Save' button to configure new storage

The new storage would appear under Storages view. Now you can use this storage with GroupDocs REST APIs. For example:

https://api.groupdocs.cloud/v2.0/conversion/info?FilePath=testfile.txt&StorageName=MyAmazonS3Storage

Please note when you configure external Amazon S3 storage, The GroupDocs Cloud APIs need the following APIs access on the bucket:

Required APIs access:

* GetObjectMetadada API
* ListObjects API

Optional APIs:

* CopyObject API
* PutObject API
* GetPreSignedURL API
* PutBucket API
* PutBucketVersioning API
* DeleteObject API
* ListVersions API
* GetObject API
* DeleteBucket API
