---
title: "AiNameFormatted"
type: docs
url: /reference-model-ai-name-formatted/
weight: 1
---
Formatted name             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Name** | **string** | Formatted name value              | [optional] 
**Comments** | **string** | Usually empty; can contain extra message describing some issue occurred during the formatting              | [optional] 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="ai_name_formatted_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var aiNameFormatted = new AiNameFormatted
{
    Name = "Mr. Cane J. M.",
    Comments = "format: %t%L%f%m; source: parsed format"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameFormatted aiNameFormatted = Models.aiNameFormatted()
    .name("Mr. Cane J. M.")
    .comments("format: %t%L%f%m; source: parsed format")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
ai_name_formatted = models.AiNameFormatted(
    name='Mr. Cane J. M.',
    comments='format: %t%L%f%m; source: parsed format')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
ai_name_formatted = AiNameFormatted.new(
  name: 'Mr. Cane J. M.',
  comments: 'format: %t%L%f%m; source: parsed format')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let aiNameFormatted = Models.aiNameFormatted()
    .name('Mr. Cane J. M.')
    .comments('format: %t%L%f%m; source: parsed format')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$aiNameFormatted = Models::aiNameFormatted()
    ->name('Mr. Cane J. M.')
    ->comments('format: %t%L%f%m; source: parsed format')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

