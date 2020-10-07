---
title: "AiNameWeightedVariants"
type: docs
url: /reference-model-ai-name-weighted-variants/
weight: 1
---
Name variants             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Names** | [**List&lt;AiNameWeighted&gt;**](/email/reference-model-ai-name-weighted/) | List of name variations              | [optional] 
**Comments** | **string** | Usually empty; can contain extra message describing some issue occurred during processing              | [optional] 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="ai_name_weighted_variants_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var aiNameWeightedVariants = new AiNameWeightedVariants
{
    Names = new List<AiNameWeighted>
    {
        new AiNameWeighted
        {
            Name = "J. Cane",
            Score = 1
        },
        new AiNameWeighted
        {
            Name = "Mr. Cane",
            Score = 0.75
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameWeightedVariants aiNameWeightedVariants = Models.aiNameWeightedVariants()
    .names(Arrays.<AiNameWeighted>asList(
        Models.aiNameWeighted()
            .name("J. Cane")
            .score(1)
            .build(),
        Models.aiNameWeighted()
            .name("Mr. Cane")
            .score(0.75)
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
ai_name_weighted_variants = models.AiNameWeightedVariants(
    names=[
        models.AiNameWeighted(
            name='J. Cane',
            score=1),
        models.AiNameWeighted(
            name='Mr. Cane',
            score=0.75)])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
ai_name_weighted_variants = AiNameWeightedVariants.new(
  names: [
    AiNameWeighted.new(
      name: 'J. Cane',
      score: 1),
    AiNameWeighted.new(
      name: 'Mr. Cane',
      score: 0.75)])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let aiNameWeightedVariants = Models.aiNameWeightedVariants()
    .names([
        Models.aiNameWeighted()
            .name('J. Cane')
            .score(1)
            .build(),
        Models.aiNameWeighted()
            .name('Mr. Cane')
            .score(0.75)
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$aiNameWeightedVariants = Models::aiNameWeightedVariants()
    ->names(array(
        Models::aiNameWeighted()
            ->name('J. Cane')
            ->score(1)
            ->build(),
        Models::aiNameWeighted()
            ->name('Mr. Cane')
            ->score(0.75)
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

