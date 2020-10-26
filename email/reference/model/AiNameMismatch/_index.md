---
title: "AiNameMismatch"
type: docs
url: /reference-model-ai-name-mismatch/
weight: 1
---
Names mismatch detailed description             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Category** | **string** | Mismatch type. Enum, available values: Unknown, FirstName, MiddleName, MiddleLastName, MiddleNickname, Gender, Context | 
**Similarity** | **double?** | Similarity score              | 
**Explanation** | **string** | Explanation or mismatch subtype              | [optional] 


## Example

{{< tabs tabTotal="6" tabID="ai_name_mismatch_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var aiNameMismatch = new AiNameMismatch
{
    Category = "Gender",
    Explanation = "no_match"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameMismatch aiNameMismatch = Models.aiNameMismatch()
    .category("Gender")
    .explanation("no_match")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
ai_name_mismatch = models.AiNameMismatch(
    category='Gender',
    explanation='no_match')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
ai_name_mismatch = AiNameMismatch.new(
  category: 'Gender',
  explanation: 'no_match')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let aiNameMismatch = Models.aiNameMismatch()
    .category('Gender')
    .explanation('no_match')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$aiNameMismatch = Models::aiNameMismatch()
    ->category('Gender')
    ->explanation('no_match')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

