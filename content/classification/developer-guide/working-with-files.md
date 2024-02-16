---
id: "working-with-files"
url: "classification/working-with-files"
title: "Working With Files"
productName: "GroupDocs.Classification Cloud"
weight: 6
description: "GroupDocs.Classification Cloud Working With Files"
keywords: "GroupDocs.Classification Cloud, Working With Files"
toc: True
---

## Download File API

This API allows you to download a file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).

### Download File with API Explorer

[GroupDocs.Classification Cloud API Reference](https://apireference.groupdocs.cloud/classification/#/) lets you to try out [Download a File API](https://apireference.groupdocs.cloud/classification/#/File/DownloadFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.

### Download File Request Parameters

|Parameter|Description
|---|---
|**Path**|Path of the file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|versionId|File version id

### Download File with cURL

{{< tabs "example1">}} {{< tab "Request" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/classification/storage/file/one-page.docx?storageName#MyStorage" -H  "accept: multipart/form-data" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab "Response" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

### Download File with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-classification-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [File API](https://apireference.groupdocs.cloud/classification/#/) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "example2">}} {{< tab "C#" >}}

{{< gist i-mochalov 89f9ec7c8582943597feaa95a5e3d1d3 Classification_CSharp_Download_File.cs >}}

{{< /tab >}} {{< /tabs >}}

## Upload File API

This API allows you to upload files to the [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

### Upload File with API Explorer

[GroupDocs.Classification Cloud API Reference](https://apireference.groupdocs.cloud/classification/#/) lets you try out [Upload a File API](https://apireference.groupdocs.cloud/classification/#/File/UploadFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.

### Upload File Request Body Parameters

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|File|File content

### Upload File with cURL

{{< tabs "example3">}} {{< tab "Request" >}}

```bash
curl -X POST "https://api.groupdocs.cloud/v1.0/classification/storage/file/classificationdocs%2Fone-page2.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab "Response" >}}

```json
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2019-02-27T06:10:08.884Z"
      }
    }
  ]
}
```

{{< /tab >}} {{< /tabs >}}

### Upload File with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-classification-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [File API](https://apireference.groupdocs.cloud/classification/#/File) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "example4">}} {{< tab "C#" >}}

{{< gist i-mochalov 89f9ec7c8582943597feaa95a5e3d1d3 Classification_CSharp_Upload_File.cs >}}

{{< /tab >}} {{< /tabs >}}

## Delete File API

This API allows you to delete specific file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

### Delete File with API Explorer

[GroupDocs.Classification for Cloud API Reference](https://apireference.groupdocs.cloud/classification/#/) lets you to try out [Delete a File](https://apireference.groupdocs.cloud/classification/#/File/DeleteFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.

### Delete File Request Parameters

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|versionId|File version id

### Delete File with cURL

{{< tabs "example5">}} {{< tab "Request" >}}

```bash
curl -X DELETE "https://api.groupdocs.cloud/v1.0/classification/storage/file/classificationdocs1%2Fone-page1.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab "Response" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

### Delete File with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-classification-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [File API](https://apireference.groupdocs.cloud/classification/#/File) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "example6">}} {{< tab "C#" >}}

{{< gist i-mochalov 89f9ec7c8582943597feaa95a5e3d1d3 Classification_CSharp_Delete_File.cs >}}

{{< /tab >}} {{< /tabs >}}

## File Copy API

This API allows you to copy specific file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

### File Copy with API Explorer

[GroupDocs.Classification for Cloud API Reference](https://apireference.groupdocs.cloud/classification/#/) lets you to try out [Copy File](https://apireference.groupdocs.cloud/classification/#/File/CopyFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.

### File Copy Request Parameters

|Parameter|Description
|---|---
|**srcPath**|Path of the source file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as query string parameter or as part of the URL
|**destPath**|Path of the destination file. Required.
|srcStorageName|Name of the storage of source file. If not set, then default storage used
|destStorageName|Name of the storage of destination file. If not set, then default storage used
|versionId|Source file version id

### File Copy with cURL

{{< tabs "example7">}} {{< tab "Request" >}}

```bash
curl -X PUT "https://api.groupdocs.cloud/v1.0/classification/storage/file/copy/classificationdocs%2Fone-page1.docx?destPath#classificationdocs1%2Fone-page1.docx'&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab "Response" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

### File Copy with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-classification-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [File API](https://apireference.groupdocs.cloud/classification/#/File) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "example8">}} {{< tab "C#" >}}

{{< gist i-mochalov 89f9ec7c8582943597feaa95a5e3d1d3 Classification_CSharp_Copy_File.cs >}}

{{< /tab >}} {{< /tabs >}}

## File Move API

This API allows you to copy specific file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

### File Move with API Explorer

[GroupDocs.Classification for Cloud API Reference](https://apireference.groupdocs.cloud/classification/#/) lets you to try out [Move File](https://apireference.groupdocs.cloud/classification/#/File/MoveFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.

### File Move Request Parameters

|Parameter|Description
|---|---
|**srcPath**|Path of the source file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as query string parameter or as part of the URL
|**destPath**|Path of the destination file. Required.
|srcStorageName|Name of the storage of source file. If not set, then default storage used
|destStorageName|Name of the storage of destination file. If not set, then default storage used
|versionId|Source file version id

### File Move with cURL

{{< tabs "example9">}} {{< tab "Request" >}}

```bash
curl -X PUT "https://api.groupdocs.cloud/v1.0/classification/storage/file/move/classificationdocs%2Fone-page1.docx?destPath#classificationdocs1%2Fone-page1.docx'&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab "Response" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

### File Move with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-classification-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [File API](https://apireference.groupdocs.cloud/classification/#/File) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "example10">}} {{< tab "C#" >}}

{{< gist i-mochalov 89f9ec7c8582943597feaa95a5e3d1d3 Classification_CSharp_Move_File.cs >}}

{{< /tab >}} {{< /tabs >}}
