---
title: "AiNameCompleteRequest"
type: docs
url: /reference-model-ai-name-complete-request/
weight: 2
---

Request model for [EmailCloud.Ai.Name.Complete](/email/reference-ai-name-api/#complete) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**name** |**string**|A name to complete. |
**language** |**string**|An ISO-639 code of the language; either 639-1 or 639-3 (e.g. \"it\" or \"ita\" for Italian).              |[optional] 
**location** |**string**|A geographic code such as an ISO-3166 two letter country code, for example \"FR\" for France.              |[optional] 
**encoding** |**string**|A character encoding name. |[optional] 
**script** |**string**|A writing system code; starts with the ISO-15924 script name. |[optional] 
**style** |**string**|Name writing style. Enum, available values: Formal, Informal, Legal, Academic |[optional] [default to 0]

## Example

{{< tabs tabTotal="6" tabID="ai_name_complete_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameCompleteRequest
{ 
    Name = "Dav"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameCompleteRequest request = Models.aiNameCompleteRequest()
    .name("Dav")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.AiNameCompleteRequest(
    name='Dav')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = AiNameCompleteRequest.new(
    name: 'Dav')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.AiNameCompleteRequest()
    .name('Dav')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::AiNameCompleteRequest()
    ->name('Dav')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

