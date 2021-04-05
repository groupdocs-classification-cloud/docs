---
id: "working-with-storage"
url: "classification/working-with-storage"
title: "Working With Storage"
productName: "GroupDocs.Classification Cloud"
weight: 6
description: "GroupDocs.Classification Cloud Working With Storage"
keywords: "GroupDocs.Classification Cloud, Working With Storage"
---

## Check Storage Exist API

This API intended for checking the existence of cloud storage with a given name from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).

### Check Storage Exist with API Explorer

[GroupDocs.Classification Cloud API Reference](https://apireference.groupdocs.cloud/classification/#/) lets you try out [Storage existence API](https://apireference.groupdocs.cloud/classification/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.

### Check Storage Exist Request Parameters

|Parameter|Description
|---|---
|**storageName**|Storage name

### Check Storage Exist with cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/classification/storage/MyStorage/exist" -H  "accept: application/json" -H  "authorization: Bearer  [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```json
{
  "exists": true
}
```

{{< /tab >}} {{< /tabs >}}

### Check Storage Exist with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-classification-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [Storage existence](https://apireference.groupdocs.cloud/classification/#/Storage/StorageExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs tabTotal="1" tabID="10" tabName1="C#" >}} {{< tab tabNum="1" >}}

{{< gist i-mochalov caf8bcd223759d65afaa07436f251820 Classification_CSharp_Storage_Exist.cs >}}

{{< /tab >}} {{< /tabs >}}

## Check Storage Object Exist API

This API intended for checking existence of file or folder in [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).

### Check Storage Object Exist with API Explorer

[GroupDocs.Classification Cloud API Reference](https://apireference.groupdocs.cloud/classification/#/) lets you try out [Storage existence API](https://apireference.groupdocs.cloud/classification/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Check Storage Object Exist Request Parameters

|Parameter|Description
|---|---
|**path**|Path of the file or folder Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|versionId|File version id

### Check Storage Object Exist with cURL

{{< tabs tabTotal="2" tabID="2" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/classification/storage/exist/classificationdocs?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```json
{
  "exists": true,
  "isFolder": true
}
```

{{< /tab >}} {{< /tabs >}}

### Check Storage Object Exist with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-classification-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [Storage Object existence](https://apireference.groupdocs.cloud/classification/#/Storage/ObjectExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs tabTotal="1" tabID="11" tabName1="C#" >}} {{< tab tabNum="1" >}}

{{< gist i-mochalov caf8bcd223759d65afaa07436f251820 Classification_CSharp_Object_Exists.cs >}}

{{< /tab >}} {{< /tabs >}}

## Storage Space Usage API

This API intended for getting total and used space of the[ GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)

### Storage Space Usage with API Explorer

[GroupDocs.Classification Cloud API Reference](https://apireference.groupdocs.cloud/classification/#/) lets you try out [storage space usage API](https://apireference.groupdocs.cloud/classification/#/Storage/GetDiscUsage) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Storage Space Usage Request parameters

|Parameter|Description
|---|---
|storageName|Name of the storage. If not set, then default storage used

### Storage Space Usage with cURL

{{< tabs tabTotal="2" tabID="3" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/classification/storage/disc?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```json
{
  "usedSize": 31032368,
  "totalSize": 3221225472
}
```

{{< /tab >}} {{< /tabs >}}

### Storage Space Usage with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-classification-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [storage space usage API](https://apireference.groupdocs.cloud/classification/#/Storage/GetDiscUsage) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs tabTotal="1" tabID="12" tabName1="C#" >}} {{< tab tabNum="1" >}}

{{< gist i-mochalov caf8bcd223759d65afaa07436f251820 Classification_CSharp_Get_Disc_Usage.cs >}}

{{< /tab >}} {{< /tabs >}}

## Storage File Versions API

This API intended for getting the list of file versions, stored in the [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)

### Storage File Versions with API Explorer

[GroupDocs.Classification Cloud API Reference](https://apireference.groupdocs.cloud/classification/#/) lets you try out [Storage File Versions API](https://apireference.groupdocs.cloud/classification/#/Storage/GetFileVersions) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Storage File Versions Request parameters

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used

### Storage File Versions with cURL

{{< tabs tabTotal="2" tabID="4" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/classification/storage/version/one-page.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```json
{
  "value": [
    {
      "versionId": "null",
      "isLatest": true,
      "name": "one-page.docx",
      "isFolder": false,
      "modifiedDate": "2018-08-16T19:45:05+00:00",
      "size": 347612,
      "path": "/one-page.docx"
    }
  ]
}
```

{{< /tab >}} {{< /tabs >}}

### Storage File Versions with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-classification-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-classification-cloud), it hides the [Storage File Versions API](https://apireference.groupdocs.cloud/classification/#/Storage/GetFileVersions) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs tabTotal="1" tabID="13" tabName1="C#" >}} {{< tab tabNum="1" >}}

{{< gist i-mochalov caf8bcd223759d65afaa07436f251820 Classification_CSharp_Get_File_Versions.cs >}}

{{< /tab >}} {{< /tabs >}}
