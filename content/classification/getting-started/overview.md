---
id: "overview"
url: "classification/overview"
title: "Overview"
productName: "GroupDocs.Classification Cloud"
weight: 1
description: ""
keywords: ""
toc: True
---

GroupDocs.Classification Cloud is a REST API for classification documents.

{{< alert style="info" >}}
Our GroupDocs.Classification Cloud REST API comes with many features crucial to organizations, such as:

* Classification of the raw texts.
* Classification of batches of raw texts.
* Classification of documents for next supported file formats:
Portable Document Format: PDF;
Microsoft Word: DOC, DOCX, DOCM, DOT, DOTX, DOTM;
OpenDocument Formats: ODT, OTT;
Rich Text Format: RTF;
Plain Text File: TXT.
* Multilingual Sentiment Analysis with Sentiment and Sentiment3 taxonomies. English, Chinese, German and Spanish languages are supported.
{{< /alert >}}

## Security and authentication

The GroupDocs.Classification Cloud API is secured and requires authentication. Developers can [generate]({{< ref "total/ui-topics/creating-and-managing-application.md" >}}) a new application with an unique Client Id and Client Secret combination after [registering]({{< ref "total/ui-topics/creating-and-managing-account.md" >}}) to our [dashboard](https://dashboard.groupdocs.cloud). Authenticated requests require a Bearer authorization header with a JWT Token obtained by using the previously specified Cliend Id + Client Secret credentials. You can check complete details about authenticating your calls to our API [here]({{< ref "total/overview-rest-api/authenticating-api-requests.md" >}}).

## SDK example

GroupDocs.Classification Cloud comes with SDKs for different platforms to use this REST API in your specific project effortlessly. Checkout our GitHub [repository](https://github.com/groupdocs-classification-cloud)for a complete list of GroupDocs.Classification SDKs along with working examples, to get you started in no time.

## API explorer

The easiest way to try out our API right away in your browser! With the [GroupDocs Cloud Web API explorer](https://apireference.groupdocs.cloud/classification/). This is a collection of Swagger documentation for the GroupDocs Cloud APIs. You can get information about all the resources in the API. It also provides testing and interactivity to our API endpoint documentation.