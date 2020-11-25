---
id: "groupdocs-classification-cloud-20-11"
url: "classification/groupdocs-classification-cloud-20-11"
title: "GroupDocs.Classification Cloud 20.11"
productName: "GroupDocs.Classification Cloud"
description: ""
keywords: ""
---

## Major Features ##

* Sentiment Classification probability model for English and Chinese was enhanced.


## Full List of Issues Covering all Changes in this Release ##

|Key|Summary|Category
|---|---|---
|GDCLASS-62|Add a support for batch text classification|Feature
|GDCLASS-64|Add a support for sentiment3 taxonomy|Feature

## Public API and Backward Incompatible Changes ##

### Classify batch of texts with the Sentiment taxonomy ###

**Sentiment Analysis (Classification)**

```html 

curl -X POST "https://api.groupdocs.cloud/v1.0/classification/classify/batch?BestClassesCount#1&Taxonomy#sentiment" \
-H "accept: application/json" -H "Content-Type: application/json" \
-d "{ \"batch\": [\"熟能生巧\", \"熟能生巧\"]}" -H "Authorization: Bearer [Access_token]"

 ```

```json 
{
	"results":
	[
		{"bestClassName":"Positive","bestClassProbability":79.44,"bestResults":
			[
			{"className":"Positive","classProbability":79.44},{"className":"Neutral","classProbability":11.34},{"className":"Negative","classProbability":9.22}
			]},
		{"bestClassName":"Positive","bestClassProbability":79.44,"bestResults":
			[
			{"className":"Positive","classProbability":79.44},{"className":"Neutral","classProbability":11.34},{"className":"Negative","classProbability":9.22}
			]}
	],
	"Code":200,
	"status":"OK"
}
 ```