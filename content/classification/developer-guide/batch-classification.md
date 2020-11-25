---
id: "batch-classification"
url: "classification/batch-classification"
title: "Batch of texts classification"
productName: "GroupDocs.Classification Cloud"
weight: 5
description: ""
keywords: ""
---






# Classify batch of texts #

Batch classification allows to classify a group of texts (up to 10) in one request. 
This API retrieves batch classification result for [IAB-2]({{< ref "classification/developer-guide/common-resources/taxonomy.md" >}}), [Documents]({{< ref "classification/developer-guide/common-resources/taxonomy.md" >}}), [Sentiment, or Sentiment3]({{< ref "classification/developer-guide/common-resources/taxonomy.md" >}}) taxonomies. It returns an object that contains information about the best classes for all the texts in the request and their probabilities.

See [Classify request parameters]({{< ref "classification/developer-guide/common-resources/classify-request-parameters.md" >}}) for request's details.

## Limitations ##

Only the first 10 texts will be processed.

## Resource ##

This resource represents a controller for single call document classification.

Classify document with taxonomy. Set taxonomy parameter to "default" for IAB-2, set to "documents" for Documents taxonomy, or set to "sentiment" or "sentiment3" for Sentiments taxonomies.

## cURL REST Example for Sentiment3 taxonomy ##


 Request

```html 
curl -v "http://api.groupdocs.cloud/v1.0/classification/classify/batch?taxonomy#sentiment3"
-H "content-type: application/json"
-X POST -d '{ "Batch": ["Text1", "Text2"] }'
 ```


 Response

```html 
{ results:
  [{
      "bestClassName": "Neutral",
      "bestClassProbability": 90.02,
      "bestResults": [],
      "code": 200,
      "status": "OK"
    },
    {
      "bestClassName": "Neutral",
      "bestClassProbability": 90.02,
      "bestResults": [],
      "code": 200,
      "status": "OK"
  }]
}
 ```



## cURL REST Example for "Documents" taxonomy ##


 Request

```html 
curl -v "http://api.groupdocs.cloud/v1.0/classification/classify?bestClassesCount#3&taxonomy#documents"
-H "content-type: application/json"
-X POST -d '{ "Document": {"Folder": "words/docx","Name": "four-pages.docx" } }'
 ```


 Response

```html 
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



## cURL REST Example for Sentiment taxonomy ##


 Request

```html 
curl -v "http://api.groupdocs.cloud/v1.0/classification/classify?bestClassesCount#1&taxonomy#sentiment"
-H "content-type: application/json"
-X POST -d '{ "Document": {"Folder": "words/docx","Name": "four-pages.docx" } }'
 ```


 Response

```html 
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


## cURL REST Example for Sentiment3 taxonomy ##


 Request

```html 
curl -v "http://api.groupdocs.cloud/v1.0/classification/classify?bestClassesCount#3&taxonomy#sentiment3"
-H "content-type: application/json"
-X POST -d '{ "Document": {"Folder": "words/docx","Name": "four-pages.docx" } }'
 ```


 Response

```html 
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
    "className":"Negative
    "classProbability":3.42
  }],
  "Code":200,
  "status":"OK"
}
 ```


## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-classification-cloud/)

### Classify Document from Storage ###


 C#




{{< gist groupdocscloud adb54c76c82d414eeb066a86c8a9fc61 Classification_CSharp_Classify_Document_from_Storage.cs >}}






###   ###

### Classify Document from Stream ###


 C#




{{< gist i-mochalov ca4a706a028a4007f4ae14082f81ff90 ClassificationCSharpClassifyDocumentStream.cs >}}











 

