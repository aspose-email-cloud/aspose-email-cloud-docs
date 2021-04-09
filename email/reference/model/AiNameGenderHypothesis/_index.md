---
title: "AiNameGenderHypothesis"
type: docs
url: /reference-model-ai-name-gender-hypothesis/
weight: 1
---
Name gender hypothesis             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Gender** | **string** | Recognized name gender. Enum, available values: Male, Female, Unknown | 
**Score** | **double?** | Hypothesis score              | 


## Example

{{< tabs tabTotal="6" tabID="ai_name_gender_hypothesis_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var aiNameGenderHypothesis = new AiNameGenderHypothesis
{
    Score = 0,8
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameGenderHypothesis aiNameGenderHypothesis = Models.aiNameGenderHypothesis()
    .score(0,8)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
ai_name_gender_hypothesis = models.AiNameGenderHypothesis(
    score=0,8)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
ai_name_gender_hypothesis = AiNameGenderHypothesis.new(
  score: 0,8)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let aiNameGenderHypothesis = Models.aiNameGenderHypothesis()
    .score(0,8)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$aiNameGenderHypothesis = Models::aiNameGenderHypothesis()
    ->score(0,8)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

