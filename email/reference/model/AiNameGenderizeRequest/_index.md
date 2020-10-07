---
title: "AiNameGenderizeRequest"
type: docs
url: /reference-model-ai-name-genderize-request/
weight: 2
---

Request model for [EmailCloud.Ai.Name.Genderize](/email/reference-ai-name-api/#genderize) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**name** |**string**|A name to genderize. |
**language** |**string**|An ISO-639 code of the language; either 639-1 or 639-3 (e.g. \"it\" or \"ita\" for Italian).              |[optional] 
**location** |**string**|A geographic code such as an ISO-3166 two letter country code, for example \"FR\" for France.              |[optional] 
**encoding** |**string**|A character encoding name. |[optional] 
**script** |**string**|A writing system code; starts with the ISO-15924 script name. |[optional] 
**style** |**string**|Name writing style. Enum, available values: Formal, Informal, Legal, Academic |[optional] [default to 0]

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="ai_name_genderize_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameGenderizeRequest
{ 
    Name = "John Cane"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameGenderizeRequest request = Models.aiNameGenderizeRequest()
    .name("John Cane")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.AiNameGenderizeRequest(
    name='John Cane')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = AiNameGenderizeRequest.new(
    name: 'John Cane')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.AiNameGenderizeRequest()
    .name('John Cane')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::AiNameGenderizeRequest()
    ->name('John Cane')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

