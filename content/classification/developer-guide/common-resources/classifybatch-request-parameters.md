---
id: "classifybatch-request-parameters"
url: "classification/classifybatch-request-parameters"
title: "classify/batch Request Parameters"
productName: "GroupDocs.Classification Cloud"
weight: 3
description: ""
keywords: ""
toc: True
---

|Parameter|In|Type|Comment
|---|---|---|---
| |body|BatchRequest|Batch of texts (up to 10).
|BestClassesCount|url (Optional)|string ("1", "2", "3",..)|Count of the best classes to return.
|Taxonomy|url (Optional)|string ("", "default", "iab2", "documents", "sentiment", "sentiment3")|Taxonomy to use for classification return.
|PrecisionRecallBalance|url (Optional)|string ("precision", "recall", "") |Balance between precision and recall.


## BaseRequest

### Model:

```javascript 

BatchRequest {
  batch (string[]),
}

 ```

### Examples:


JSON

```json 
{
  "batch": ["Text1", "Text2"]
}
```

XML

```xml 

<?xml version#"1.0"?>
<BatchRequest>
  <batch>Text1</batch>
  <batch>Text1</batch>
</BatchRequest>

 ```
