---
title: "AiNameMatchResult"
type: docs
url: /reference-model-ai-name-match-result/
weight: 1
---
Two names match result             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Similarity** | **double?** | Similarity score              | 
**Mismatches** | [**List&lt;AiNameMismatch&gt;**](/email/reference-model-ai-name-mismatch/) | Detailed description of mismatches              | [optional] 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="ai_name_match_result_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var aiNameMatchResult = new AiNameMatchResult
{
    Similarity = 0.6,
    Mismatches = new List<AiNameMismatch>
    {
        new AiNameMismatch
        {
            Category = "Gender",
            Explanation = "no_match"
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameMatchResult aiNameMatchResult = Models.aiNameMatchResult()
    .similarity(0.6)
    .mismatches(Arrays.<AiNameMismatch>asList(
        Models.aiNameMismatch()
            .category("Gender")
            .explanation("no_match")
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
ai_name_match_result = models.AiNameMatchResult(
    similarity=0.6,
    mismatches=[
        models.AiNameMismatch(
            category='Gender',
            explanation='no_match')])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
ai_name_match_result = AiNameMatchResult.new(
  similarity: 0.6,
  mismatches: [
    AiNameMismatch.new(
      category: 'Gender',
      explanation: 'no_match')])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let aiNameMatchResult = Models.aiNameMatchResult()
    .similarity(0.6)
    .mismatches([
        Models.aiNameMismatch()
            .category('Gender')
            .explanation('no_match')
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$aiNameMatchResult = Models::aiNameMatchResult()
    ->similarity(0.6)
    ->mismatches(array(
        Models::aiNameMismatch()
            ->category('Gender')
            ->explanation('no_match')
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

