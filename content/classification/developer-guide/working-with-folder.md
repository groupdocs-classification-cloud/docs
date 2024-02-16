---
id: "working-with-folder"
url: "classification/working-with-folder"
title: "Working With Folder"
productName: "GroupDocs.Classification Cloud"
weight: 7
description: "GroupDocs.Classification Cloud Working With Folder"
keywords: "GroupDocs.Classification Cloud, Working With Folder"
toc: True
---

## List Files

This API allows you to get a list of all files of a specific folder from the specified Cloud Storage. If you do not pass storage name API will find folder in GroupDocs Cloud Storage.

### List Files with API Explorer

[GroupDocs.Classification Cloud API Reference](https://apireference.groupdocs.cloud/classification/) lets you to try out [List Files in a Folder API](https://apireference.groupdocs.cloud/classification/#/Folder/GetFilesList) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs exposes.

### List Files Request Parameters

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used

### List Files with cURL

{{< tabs "example1">}} {{< tab "Request" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/classification/storage/folder/classificationdocs?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab "Response" >}}

```json
{
  "value": [
    {
      "name": "four-pages.docx",
      "isFolder": false,
      "modifiedDate": "2019-03-20T12:35:38+00:00",
      "size": 8651,
      "path": "/classificationdocs/four-pages.docx"
    },
    ...
  ]
}
```

{{< /tab >}} {{< /tabs >}}

### List Files with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-storage-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [Folder API](https://apireference.groupdocs.cloud/classification/#/Folder) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "example2">}} {{< tab "C#" >}}

{{< gist i-mochalov 89f9ec7c8582943597feaa95a5e3d1d3 Classification_CSharp_Get_Files_List.cs >}}

{{< /tab >}} {{< /tabs >}}

## Create New Folder

This API allows you to create a new Folder in the specified Cloud Storage. If you do not pass storage name API will create new Folder in default Cloud Storage.

### Create New Folder with API Explorer

[GroupDocs.Classification Cloud API Reference](https://apireference.groupdocs.cloud/classification/) lets you to try out [Create Folder API](https://apireference.groupdocs.cloud/classification/#/Folder/CreateFolder) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs exposes.

### Create New Folder Request Parameters

|Parameter|Description
|---|---
|**path**|Target folder’s path e.g. Folder1/Folder2/. The folders will be created recursively Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used

### Create New Folder with cURL

{{< tabs "example3">}} {{< tab "Request" >}}

```bash
curl -X POST "https://api.groupdocs.cloud/v1.0/classification/storage/folder/classificationdocs3?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab "Response" >}}

```json
{
  "code": 200,
  "status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

### Create New Folder with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-storage-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [Folder API](https://apireference.groupdocs.cloud/classification/#/Folder/) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "example3">}} {{< tab "C#" >}}

{{< gist i-mochalov 89f9ec7c8582943597feaa95a5e3d1d3 Classification_CSharp_Create_Folder.cs >}}

{{< /tab >}} {{< /tabs >}}

## Delete Folder

This API allows you to delete a particular Folder in the specified Cloud Storage. If you do not pass storage name API will create new Folder in default Cloud Storage. To remove recursively inner folder/files you need to pass true value to recursive parameter in Request. If it is set to false and folder contains data then API throws the exception.

### Delete Folder with API Explorer

[GroupDocs.Classification Cloud API Reference](https://apireference.groupdocs.cloud/classification/#/) lets you to try out [Delete a Particular Folder API](https://apireference.groupdocs.cloud/classification/#/Folder/DeleteFolder) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs exposes.

### Delete Folder Request Parameters

|Parameter|Description
|---|---
|**path**|Folder path e.g. /Folder1 Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used

### Delete Folder with cURL

{{< tabs "example4">}} {{< tab "Request" >}}

```bash
curl -X DELETE "https://api.groupdocs.cloud/v1.0/classification/storage/folder/classificationdocs3?storageName#MyStorage&#x26;recursive#true" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab "Response" >}}

```json
{
  "code": 200,
  "status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

### Delete Folder with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-classification-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [Delete Folder API](https://apireference.groupdocs.cloud/classification/#/Folder/DeleteFolder) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "example5">}} {{< tab "C#" >}}

{{< gist i-mochalov 89f9ec7c8582943597feaa95a5e3d1d3 Classification_CSharp_Delete_Folder.cs >}}

{{< /tab >}} {{< /tabs >}}

## Copy Folder

This API allows you to copy a Folder to another location in the GroupDocs Cloud Storage. If you do not pass source and destination storage names API will copy Folder within default Cloud Storage.

### Copy Folder with API Explorer

[GroupDocs.Classification Cloud API Reference](https://apireference.groupdocs.cloud/classification/#/) lets you to try out [Copy Folder API](https://apireference.groupdocs.cloud/classification/#/Folder/CopyFolder) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs exposes.

### Request parameters

|Parameter|Description
|---|---
|**srcPath**|Source folder path e.g. /Folder1 Required. Can be passed as query string parameter or as part of the URL
|**destPath**|Destination folder path. Required
|srcStorageName|Name of the storage of source folder. If not set, then default storage used
|destStorageName|Name of the storage of destination folder. If not set, then default storage used

### Copy Folder with cURL

{{< tabs "example6">}} {{< tab "Request" >}}

```bash
curl -X PUT "https://api.groupdocs.cloud/v1.0/classification/storage/folder/copy/classificationdocs?destPath#classificationdocs1&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab "Response" >}}

```json
{
  "code": 200,
  "status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

### Copy Folder with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-classification-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [Copy Folder API](https://apireference.groupdocs.cloud/classification/#/Folder/CopyFolder) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "example7">}} {{< tab "C#" >}}

{{< gist i-mochalov 89f9ec7c8582943597feaa95a5e3d1d3 Classification_CSharp_Copy_Folder.cs >}}

{{< /tab >}} {{< /tabs >}}

## Move Folder

This API allows you to move a Folder to another location in the GroupDocs Cloud Storage. If you do not pass source and destination storage names API will move Folder within default Cloud Storage.

### Move Folder with API Explorer

[GroupDocs.Classification Cloud API Reference](https://apireference.groupdocs.cloud/classification/#/) lets you to try out [Move a Folder API](https://apireference.groupdocs.cloud/classification/#/Folder/MoveFolder) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs exposes.

### Move Folder Request Parameters

|Parameter|Description
|---|---
|**srcPath**|Source folder path e.g. /Folder1 Required. Can be passed as query string parameter or as part of the URL
|**destPath**|Destination folder path. Required
|srcStorageName|Name of the storage of source folder. If not set, then default storage used
|destStorageName|Name of the storage of destination folder. If not set, then default storage used

### Move Folder with cURL

{{< tabs "example9">}} {{< tab "Request" >}}

```bash
curl -X PUT "https://api.groupdocs.cloud/v1.0/classification/storage/folder/move/classificationdocs?destPath#classificationdocs1&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab "Response" >}}

```json
{
  "code": 200,
  "status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

### Move Folder with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-classification-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [Move Folder API](https://apireference.groupdocs.cloud/classification/#/Folder/MoveFolder) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "example9">}} {{< tab "C#" >}}

{{< gist i-mochalov 89f9ec7c8582943597feaa95a5e3d1d3 Classification_CSharp_Move_Folder.cs >}}

{{< /tab >}} {{< /tabs >}}
