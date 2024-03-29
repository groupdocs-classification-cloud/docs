---
id: "documents-classification"
url: "classification/documents-classification"
title: "Documents Classification"
productName: "GroupDocs.Classification Cloud"
weight: 4
description: ""
keywords: ""
toc: True
---

This API retrieves document classification result for [IAB-2 taxonomy]({{< ref "classification/developer-guide/common-resources/taxonomy.md" >}}) or [Documents taxonomy]({{< ref "classification/developer-guide/common-resources/taxonomy.md" >}}). It returns an object that contains information about the best class and its probability and about probability of other classes.

See [Classify request parameters]({{< ref "classification/developer-guide/common-resources/classify-request-parameters.md" >}}) for request's details.

## Resource

This resource represents a controller for single call document classification.

Classify document with taxonomy. Set taxonomy parameter to "default" for IAB-2, set to "documents" for Documents taxonomy, or set to "sentiment" or "sentiment3" for Sentiments taxonomies.

## cURL REST Example for IAB-2 (default) taxonomy

Request

```bash 
curl -v "http://api.groupdocs.cloud/v1.0/classification/classify"
-H "content-type: application/json"
-X POST -d '{ "document": {"folder": "words/docx","name": "four-pages.docx" } }'
 ```

Response

```json 
{
  "bestClassName": "Books_and_Literature",
  "bestClassProbability": 48.92,
  "bestResults":[{
    "className":"Books_and_Literature",
    "classProbability":48.92
  }],
  "code": 200,
  "status": "OK"
}
 ```

## cURL REST Example for "Documents" taxonomy

Request

```bash 
curl -v "http://api.groupdocs.cloud/v1.0/classification/classify?bestClassesCount=3&taxonomy=documents"
-H "content-type: application/json"
-X POST -d '{ "document": {"folder": "words/docx","name": "four-pages.docx" } }'
 ```

Response

```json 
{
  "bestClassName": "Other",
  "bestClassProbability": 36.8,
  "bestResults": [
    {
      "className": "Other",
      "classProbability": 36.8
    },
    {
      "className": "ADVE",
      "classProbability": 14.72
    },
    {
      "className": "News",
      "classProbability": 12.77
    }
  ],
  "code": 200,
  "status": "OK"
}
 ```

## cURL REST Example for Sentiment taxonomy

Request

```bash 
curl -v "http://api.groupdocs.cloud/v1.0/classification/classify?bestClassesCount=1&taxonomy=sentiment"
-H "content-type: application/json"
-X POST -d '{ "document": {"folder": "words/docx","name": "four-pages.docx" } }'
 ```

Response

```json 
{
  "bestClassName": "Positive",
  "bestClassProbability":90.02,
  "bestResults":[{
    "className":"Positive",
    "classProbability":90.02
  }],
  "Code":200,
  "status":"OK"
}
```

## cURL REST Example for Sentiment3 taxonomy


Request

```bash 
curl -v "http://api.groupdocs.cloud/v1.0/classification/classify?bestClassesCount=3&taxonomy=sentiment3"
-H "content-type: application/json"
-X POST -d '{ "document": {"folder": "words/docx","name": "four-pages.docx" } }'
 ```
Response

```json 
{
  "bestClassName": "Positive",
  "bestClassProbability":89.43,
  "bestResults":[{
    "className":"Positive",
    "classProbability":89.43
  },
  {
    "className":"Neutral",
    "classProbability":7.15
  },
  {
    "className":"Negative",
    "classProbability":3.42
  }],
  "Code":200,
  "status":"OK"
}
```

## SDK example

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-classification-cloud/)

### Classify Document from Storage

C#

{{< gist groupdocscloud adb54c76c82d414eeb066a86c8a9fc61 Classification_CSharp_Classify_Document_from_Storage.cs >}}

### Classify Document from Stream

C#

{{< gist i-mochalov ca4a706a028a4007f4ae14082f81ff90 ClassificationCSharpClassifyDocumentStream.cs >}}