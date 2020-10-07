---
title: "AiNameMatchParsedRequest"
type: docs
url: /reference-model-ai-name-match-parsed-request/
weight: 1
---
Two parsed names to match request             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**OtherParsedName** | [**List&lt;AiNameComponent&gt;**](/email/reference-model-ai-name-component/) | Other parsed name to match              | 

Parent class: [AiNameParsedRequest](/email/reference-model-ai-name-parsed-request/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="ai_name_match_parsed_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var aiNameMatchParsedRequest = new AiNameMatchParsedRequest
{
    OtherParsedName = new List<AiNameComponent>
    {
        new AiNameComponent
        {
            Value = "J",
            Category = "FirstInitial",
            Score = 1
        },
        new AiNameComponent
        {
            Value = "Cane",
            Category = "LastName",
            Score = 0.5,
            Position = 3
        },
        new AiNameComponent
        {
            Value = "%f%L",
            Category = "Format"
        },
        new AiNameComponent
        {
            Value = "0.5",
            Category = "Score",
            Score = 0.5
        }
    },
    ParsedName = new List<AiNameComponent>
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
AiNameMatchParsedRequest aiNameMatchParsedRequest = Models.aiNameMatchParsedRequest()
    .otherParsedName(Arrays.<AiNameComponent>asList(
        Models.aiNameComponent()
            .value("J")
            .category("FirstInitial")
            .score(1)
            .build(),
        Models.aiNameComponent()
            .value("Cane")
            .category("LastName")
            .score(0.5)
            .position(3)
            .build(),
        Models.aiNameComponent()
            .value("%f%L")
            .category("Format")
            .build(),
        Models.aiNameComponent()
            .value("0.5")
            .category("Score")
            .score(0.5)
            .build()))
    .parsedName(Arrays.<AiNameComponent>asList(
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
ai_name_match_parsed_request = models.AiNameMatchParsedRequest(
    other_parsed_name=[
        models.AiNameComponent(
            value='J',
            category='FirstInitial',
            score=1),
        models.AiNameComponent(
            value='Cane',
            category='LastName',
            score=0.5,
            position=3),
        models.AiNameComponent(
            value='%f%L',
            category='Format'),
        models.AiNameComponent(
            value='0.5',
            category='Score',
            score=0.5)],
    parsed_name=[
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
ai_name_match_parsed_request = AiNameMatchParsedRequest.new(
  other_parsed_name: [
    AiNameComponent.new(
      value: 'J',
      category: 'FirstInitial',
      score: 1),
    AiNameComponent.new(
      value: 'Cane',
      category: 'LastName',
      score: 0.5,
      position: 3),
    AiNameComponent.new(
      value: '%f%L',
      category: 'Format'),
    AiNameComponent.new(
      value: '0.5',
      category: 'Score',
      score: 0.5)],
  parsed_name: [
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
let aiNameMatchParsedRequest = Models.aiNameMatchParsedRequest()
    .otherParsedName([
        Models.aiNameComponent()
            .value('J')
            .category('FirstInitial')
            .score(1)
            .build(),
        Models.aiNameComponent()
            .value('Cane')
            .category('LastName')
            .score(0.5)
            .position(3)
            .build(),
        Models.aiNameComponent()
            .value('%f%L')
            .category('Format')
            .build(),
        Models.aiNameComponent()
            .value('0.5')
            .category('Score')
            .score(0.5)
            .build()])
    .parsedName([
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
$aiNameMatchParsedRequest = Models::aiNameMatchParsedRequest()
    ->otherParsedName(array(
        Models::aiNameComponent()
            ->value('J')
            ->category('FirstInitial')
            ->score(1)
            ->build(),
        Models::aiNameComponent()
            ->value('Cane')
            ->category('LastName')
            ->score(0.5)
            ->position(3)
            ->build(),
        Models::aiNameComponent()
            ->value('%f%L')
            ->category('Format')
            ->build(),
        Models::aiNameComponent()
            ->value('0.5')
            ->category('Score')
            ->score(0.5)
            ->build()))
    ->parsedName(array(
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

