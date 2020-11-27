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

See [classify/batch request parameters]({{< ref "classification/developer-guide/common-resources/classifybatch-request-parameters.md" >}}) for request's details.

## Limitations ##

Only the first 10 texts will be processed.

## Resource ##

This resource represents a controller for single call batch of texts classification.

Classify up to 10 texts with one request. Set taxonomy parameter to "default" for IAB-2, set to "documents" for Documents taxonomy, or set to "sentiment" or "sentiment3" for Sentiments taxonomies.

## cURL REST Example for Sentiment3 taxonomy ##


 Request

```html 
curl -v "http://api.groupdocs.cloud/v1.0/classification/classify/batch?taxonomy=sentiment3"
-H "content-type: application/json"
-X POST -d '{ "batch": ["Text1", "Text2"] }'
 ```


 Response

```html 
{ results:
  [{
      "bestClassName": "Neutral",
      "bestClassProbability": 90.02,
      "bestResults": [{"className":"Neutral","classProbability":90.02}],
      "code": 200,
      "status": "OK"
    },
    {
      "bestClassName": "Neutral",
      "bestClassProbability": 90.02,
      "bestResults": [{"className":"Neutral","classProbability":90.02}],
      "code": 200,
      "status": "OK"
  }]
}
 ```



## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-classification-cloud/)

### Classify Batch of Texts ###


 C#




{{< gist i-mochalov ca4a706a028a4007f4ae14082f81ff90 ClassificationCSharpCloudBatch.cs >}}















 


