---
title: "AiNameComponentList"
type: docs
url: /reference-model-ai-name-component-list/
weight: 1
---
List of name components             

Properties:

Class has no properties

Parent class: [ListResponseOfAiNameComponent](/email/reference-model-list-response-of-ai-name-component/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="ai_name_component_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var aiNameComponentList = new AiNameComponentList
{
    Value = new List<AiNameComponent>
    {
        new AiNameComponent
        {
            Value = "John",
            Category = "FirstName",
            Score = 0.95
        },
        new AiNameComponent
        {
            Value = "Cane",
            Category = "LastName",
            Score = 0.5,
            Position = 5
        },
        new AiNameComponent
        {
            Value = "%F%L",
            Category = "Format"
        },
        new AiNameComponent
        {
            Value = "0.5",
            Category = "Score",
            Score = 0.5
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameComponentList aiNameComponentList = Models.aiNameComponentList()
    .value(Arrays.<AiNameComponent>asList(
        Models.aiNameComponent()
            .value("John")
            .category("FirstName")
            .score(0.95)
            .build(),
        Models.aiNameComponent()
            .value("Cane")
            .category("LastName")
            .score(0.5)
            .position(5)
            .build(),
        Models.aiNameComponent()
            .value("%F%L")
            .category("Format")
            .build(),
        Models.aiNameComponent()
            .value("0.5")
            .category("Score")
            .score(0.5)
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
ai_name_component_list = models.AiNameComponentList(
    value=[
        models.AiNameComponent(
            value='John',
            category='FirstName',
            score=0.95),
        models.AiNameComponent(
            value='Cane',
            category='LastName',
            score=0.5,
            position=5),
        models.AiNameComponent(
            value='%F%L',
            category='Format'),
        models.AiNameComponent(
            value='0.5',
            category='Score',
            score=0.5)])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
ai_name_component_list = AiNameComponentList.new(
  value: [
    AiNameComponent.new(
      value: 'John',
      category: 'FirstName',
      score: 0.95),
    AiNameComponent.new(
      value: 'Cane',
      category: 'LastName',
      score: 0.5,
      position: 5),
    AiNameComponent.new(
      value: '%F%L',
      category: 'Format'),
    AiNameComponent.new(
      value: '0.5',
      category: 'Score',
      score: 0.5)])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let aiNameComponentList = Models.aiNameComponentList()
    .value([
        Models.aiNameComponent()
            .value('John')
            .category('FirstName')
            .score(0.95)
            .build(),
        Models.aiNameComponent()
            .value('Cane')
            .category('LastName')
            .score(0.5)
            .position(5)
            .build(),
        Models.aiNameComponent()
            .value('%F%L')
            .category('Format')
            .build(),
        Models.aiNameComponent()
            .value('0.5')
            .category('Score')
            .score(0.5)
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$aiNameComponentList = Models::aiNameComponentList()
    ->value(array(
        Models::aiNameComponent()
            ->value('John')
            ->category('FirstName')
            ->score(0.95)
            ->build(),
        Models::aiNameComponent()
            ->value('Cane')
            ->category('LastName')
            ->score(0.5)
            ->position(5)
            ->build(),
        Models::aiNameComponent()
            ->value('%F%L')
            ->category('Format')
            ->build(),
        Models::aiNameComponent()
            ->value('0.5')
            ->category('Score')
            ->score(0.5)
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

