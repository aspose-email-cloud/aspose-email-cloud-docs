---
title: "AiNameParseRequest"
type: docs
url: /reference-model-ai-name-parse-request/
weight: 2
---

Request model for [EmailCloud.Ai.Name.Parse](/email/reference-ai-name-api/#parse) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**name** |**string**|A name to parse. |
**language** |**string**|An ISO-639 code of the language; either 639-1 or 639-3 (e.g. \"it\" or \"ita\" for Italian).              |[optional] 
**location** |**string**|A geographic code such as an ISO-3166 two letter country code, for example \"FR\" for France.              |[optional] 
**encoding** |**string**|A character encoding name. |[optional] 
**script** |**string**|A writing system code; starts with the ISO-15924 script name. |[optional] 
**style** |**string**|Name writing style. Enum, available values: Formal, Informal, Legal, Academic |[optional] [default to 0]

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="ai_name_parse_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameParseRequest
{ 
    Name = "John Cane",
    Language = "eng",
    Location = "USA"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameParseRequest request = Models.aiNameParseRequest()
    .name("John Cane")
    .language("eng")
    .location("USA")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.AiNameParseRequest(
    name='John Cane',
    language='eng',
    location='USA')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = AiNameParseRequest.new(
    name: 'John Cane',
    language: 'eng',
    location: 'USA')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.AiNameParseRequest()
    .name('John Cane')
    .language('eng')
    .location('USA')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::AiNameParseRequest()
    ->name('John Cane')
    ->language('eng')
    ->location('USA')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

