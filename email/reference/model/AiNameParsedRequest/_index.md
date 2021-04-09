---
title: "AiNameParsedRequest"
type: docs
url: /reference-model-ai-name-parsed-request/
weight: 1
---
Parsed name request model             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**CulturalContext** | [**AiNameCulturalContext**](/email/reference-model-ai-name-cultural-context/) | AiName parser cultural context              | [optional] 
**Format** | **string** | Format of the name. Predefined format can be used by ID, or custom format can be specified. Predefined formats:      /format/default/ (&#x3D; &#39;%t%F%m%N%L%p&#39;)     /format/FN+LN/ (&#x3D; &#39;%F%L&#39;)     /format/title+FN+LN/ (&#x3D; &#39;%t%F%L&#39;)     /format/FN+MN+LN/ (&#x3D; &#39;%F%M%N%L&#39;)     /format/title+FN+MN+LN/ (&#x3D; &#39;%t%F%M%N%L&#39;)     /format/FN+MI+LN/ (&#x3D; &#39;%F%m%N%L&#39;)     /format/title+FN+MI+LN/ (&#x3D; &#39;%t%F%m%N%L&#39;)     /format/LN/ (&#x3D; &#39;%L&#39;)     /format/title+LN/ (&#x3D; &#39;%t%L&#39;)     /format/LN+FN+MN/ (&#x3D; &#39;%L,%F%M%N&#39;)     /format/LN+title+FN+MN/ (&#x3D; &#39;%L,%t%F%M%N&#39;)     /format/LN+FN+MI/ (&#x3D; &#39;%L,%F%m%N&#39;)     /format/LN+title+FN+MI/ (&#x3D; &#39;%L,%t%F%m%N&#39;)  Custom format string - custom combination of characters and the next term placeholders:      &#39;%t&#39; - Title (prefix)     &#39;%F&#39; - First name     &#39;%f&#39; - First initial     &#39;%M&#39; - Middle name(s)     &#39;%m&#39; - Middle initial(s)     &#39;%N&#39; - Nickname     &#39;%L&#39; - Last name     &#39;%l&#39; - Last initial     &#39;%p&#39; - Postfix  If no value for format option was provided, its default value is &#39;%t%F%m%N%L%p&#39;              | [optional] 
**ParsedName** | [**List&lt;AiNameComponent&gt;**](/email/reference-model-ai-name-component/) | Parsed name              | 


## Example

{{< tabs tabTotal="6" tabID="ai_name_parsed_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var aiNameParsedRequest = new AiNameParsedRequest
{
    ParsedName = new List<AiNameComponent>
    {
        new AiNameComponent
        {
            Value = "John",
            Category = "FirstName",
            Score = 0,95
        },
        new AiNameComponent
        {
            Value = "Cane",
            Category = "LastName",
            Score = 0,5,
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
            Score = 0,5
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameParsedRequest aiNameParsedRequest = Models.aiNameParsedRequest()
    .parsedName(Arrays.<AiNameComponent>asList(
        Models.aiNameComponent()
            .value("John")
            .category("FirstName")
            .score(0,95)
            .build(),
        Models.aiNameComponent()
            .value("Cane")
            .category("LastName")
            .score(0,5)
            .position(5)
            .build(),
        Models.aiNameComponent()
            .value("%F%L")
            .category("Format")
            .build(),
        Models.aiNameComponent()
            .value("0.5")
            .category("Score")
            .score(0,5)
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
ai_name_parsed_request = models.AiNameParsedRequest(
    parsed_name=[
        models.AiNameComponent(
            value='John',
            category='FirstName',
            score=0,95),
        models.AiNameComponent(
            value='Cane',
            category='LastName',
            score=0,5,
            position=5),
        models.AiNameComponent(
            value='%F%L',
            category='Format'),
        models.AiNameComponent(
            value='0.5',
            category='Score',
            score=0,5)])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
ai_name_parsed_request = AiNameParsedRequest.new(
  parsed_name: [
    AiNameComponent.new(
      value: 'John',
      category: 'FirstName',
      score: 0,95),
    AiNameComponent.new(
      value: 'Cane',
      category: 'LastName',
      score: 0,5,
      position: 5),
    AiNameComponent.new(
      value: '%F%L',
      category: 'Format'),
    AiNameComponent.new(
      value: '0.5',
      category: 'Score',
      score: 0,5)])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let aiNameParsedRequest = Models.aiNameParsedRequest()
    .parsedName([
        Models.aiNameComponent()
            .value('John')
            .category('FirstName')
            .score(0,95)
            .build(),
        Models.aiNameComponent()
            .value('Cane')
            .category('LastName')
            .score(0,5)
            .position(5)
            .build(),
        Models.aiNameComponent()
            .value('%F%L')
            .category('Format')
            .build(),
        Models.aiNameComponent()
            .value('0.5')
            .category('Score')
            .score(0,5)
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$aiNameParsedRequest = Models::aiNameParsedRequest()
    ->parsedName(array(
        Models::aiNameComponent()
            ->value('John')
            ->category('FirstName')
            ->score(0,95)
            ->build(),
        Models::aiNameComponent()
            ->value('Cane')
            ->category('LastName')
            ->score(0,5)
            ->position(5)
            ->build(),
        Models::aiNameComponent()
            ->value('%F%L')
            ->category('Format')
            ->build(),
        Models::aiNameComponent()
            ->value('0.5')
            ->category('Score')
            ->score(0,5)
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

