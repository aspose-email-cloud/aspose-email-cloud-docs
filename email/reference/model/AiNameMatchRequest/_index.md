---
title: "AiNameMatchRequest"
type: docs
url: /reference-model-ai-name-match-request/
weight: 2
---

Request model for [EmailCloud.Ai.Name.Match](/email/reference-ai-name-api/#match) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**name** |**string**|A name to match. |
**otherName** |**string**|Another name to match. |
**language** |**string**|An ISO-639 code of the language; either 639-1 or 639-3 (e.g. \"it\" or \"ita\" for Italian).              |[optional] 
**location** |**string**|A geographic code such as an ISO-3166 two letter country code, for example \"FR\" for France.              |[optional] 
**encoding** |**string**|A character encoding name. |[optional] 
**script** |**string**|A writing system code; starts with the ISO-15924 script name. |[optional] 
**style** |**string**|Name writing style. Enum, available values: Formal, Informal, Legal, Academic |[optional] [default to 0]

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="ai_name_match_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameMatchRequest
{ 
    Name = "John Michael Cane",
    OtherName = "Cane J."
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameMatchRequest request = Models.aiNameMatchRequest()
    .name("John Michael Cane")
    .otherName("Cane J.")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.AiNameMatchRequest(
    name='John Michael Cane',
    other_name='Cane J.')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = AiNameMatchRequest.new(
    name: 'John Michael Cane',
    other_name: 'Cane J.')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.AiNameMatchRequest()
    .name('John Michael Cane')
    .otherName('Cane J.')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::AiNameMatchRequest()
    ->name('John Michael Cane')
    ->other_name('Cane J.')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

