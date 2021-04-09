---
title: "AiNameExtracted"
type: docs
url: /reference-model-ai-name-extracted/
weight: 1
---
Extracted name             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Name** | [**List&lt;AiNameExtractedComponent&gt;**](/email/reference-model-ai-name-extracted-component/) | Extracted name components              | [optional] 
**Score** | **double?** | Extracted name score              | 


## Example

{{< tabs tabTotal="6" tabID="ai_name_extracted_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var aiNameExtracted = new AiNameExtracted
{
    Name = new List<AiNameExtractedComponent>
    {
        new AiNameExtractedComponent
        {
            Category = "Surname",
            Value = "Cane"
        },
        new AiNameExtractedComponent
        {
            Category = "SomeName",
            Value = "John"
        }
    },
    Score = 0,5
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameExtracted aiNameExtracted = Models.aiNameExtracted()
    .name(Arrays.<AiNameExtractedComponent>asList(
        Models.aiNameExtractedComponent()
            .category("Surname")
            .value("Cane")
            .build(),
        Models.aiNameExtractedComponent()
            .category("SomeName")
            .value("John")
            .build()))
    .score(0,5)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
ai_name_extracted = models.AiNameExtracted(
    name=[
        models.AiNameExtractedComponent(
            category='Surname',
            value='Cane'),
        models.AiNameExtractedComponent(
            category='SomeName',
            value='John')],
    score=0,5)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
ai_name_extracted = AiNameExtracted.new(
  name: [
    AiNameExtractedComponent.new(
      category: 'Surname',
      value: 'Cane'),
    AiNameExtractedComponent.new(
      category: 'SomeName',
      value: 'John')],
  score: 0,5)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let aiNameExtracted = Models.aiNameExtracted()
    .name([
        Models.aiNameExtractedComponent()
            .category('Surname')
            .value('Cane')
            .build(),
        Models.aiNameExtractedComponent()
            .category('SomeName')
            .value('John')
            .build()])
    .score(0,5)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$aiNameExtracted = Models::aiNameExtracted()
    ->name(array(
        Models::aiNameExtractedComponent()
            ->category('Surname')
            ->value('Cane')
            ->build(),
        Models::aiNameExtractedComponent()
            ->category('SomeName')
            ->value('John')
            ->build()))
    ->score(0,5)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

