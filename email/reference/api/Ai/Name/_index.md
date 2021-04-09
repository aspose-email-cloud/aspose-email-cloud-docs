---
title: "Name"
type: docs
url: /reference-ai-name-api/
weight: 1
---

AI Name operations.


AI-powered Name API.

This API should be used to:
 - Determine a person's gender from the name.
 - Complete name using given starting characters.
 - Compare names to determine similarity.
 - Format name.
 - Parse a name from the email address.

## Complete

The call proposes k most probable names for given starting characters. 
Returns [**AiNameWeightedVariants**](/email/reference-model-ai-name-weighted-variants/) model. Requires:

{{< expand-list title="request" >}}

Complete method request. Type: [**AiNameCompleteRequest**](/email/reference-model-ai-name-complete-request/).

{{< tabs tabTotal="6" tabID="ai_name_complete_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameCompleteRequest
{ 
    Name = "Dav"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameCompleteRequest request = Models.aiNameCompleteRequest()
    .name("Dav")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.AiNameCompleteRequest(
    name='Dav')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = AiNameCompleteRequest.new(
    name: 'Dav')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.AiNameCompleteRequest()
    .name('Dav')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::AiNameCompleteRequest()
    ->name('Dav')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="ai_name_complete_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Ai.Name.CompleteAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameWeightedVariants result = api.ai().name().complete(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.name.complete(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.ai.name.complete(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.ai.name.complete(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->ai()->name()->complete($request);
```

{{< /tab >}}

{{< /tabs >}}
## Expand

Expands a person's name into a list of possible alternatives using options for expanding instructions. 
Returns [**AiNameWeightedVariants**](/email/reference-model-ai-name-weighted-variants/) model. Requires:

{{< expand-list title="request" >}}

Expand method request. Type: [**AiNameExpandRequest**](/email/reference-model-ai-name-expand-request/).

{{< tabs tabTotal="6" tabID="ai_name_expand_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameExpandRequest
{ 
    Name = "John Cane"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameExpandRequest request = Models.aiNameExpandRequest()
    .name("John Cane")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.AiNameExpandRequest(
    name='John Cane')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = AiNameExpandRequest.new(
    name: 'John Cane')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.AiNameExpandRequest()
    .name('John Cane')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::AiNameExpandRequest()
    ->name('John Cane')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="ai_name_expand_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Ai.Name.ExpandAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameWeightedVariants result = api.ai().name().expand(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.name.expand(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.ai.name.expand(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.ai.name.expand(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->ai()->name()->expand($request);
```

{{< /tab >}}

{{< /tabs >}}
## ExpandParsed

Expands a person's parsed name into a list of possible alternatives using options for expanding instructions. 
Returns [**AiNameWeightedVariants**](/email/reference-model-ai-name-weighted-variants/) model. Requires:

{{< expand-list title="request" >}}

Parsed name with options. Type: [**AiNameParsedRequest**](/email/reference-model-ai-name-parsed-request/).

{{< tabs tabTotal="6" tabID="ai_name_expand_parsed_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameParsedRequest
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
AiNameParsedRequest request = Models.aiNameParsedRequest()
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
request = models.AiNameParsedRequest(
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
request = AiNameParsedRequest.new(
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
let request = Models.aiNameParsedRequest()
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
$request = Models::aiNameParsedRequest()
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

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="ai_name_expand_parsed_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Ai.Name.ExpandParsedAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameWeightedVariants result = api.ai().name().expandParsed(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.name.expand_parsed(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.ai.name.expand_parsed(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.ai.name.expandParsed(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->ai()->name()->expandParsed($request);
```

{{< /tab >}}

{{< /tabs >}}
## Format

Formats a person's name in correct case and name order using options for formatting instructions. 
Returns [**AiNameFormatted**](/email/reference-model-ai-name-formatted/) model. Requires:

{{< expand-list title="request" >}}

Format method request. Type: [**AiNameFormatRequest**](/email/reference-model-ai-name-format-request/).

{{< tabs tabTotal="6" tabID="ai_name_format_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameFormatRequest
{ 
    Name = "Mr. John Michael Cane",
    Format = "%t%L%f%m"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameFormatRequest request = Models.aiNameFormatRequest()
    .name("Mr. John Michael Cane")
    .format("%t%L%f%m")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.AiNameFormatRequest(
    name='Mr. John Michael Cane',
    format='%t%L%f%m')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = AiNameFormatRequest.new(
    name: 'Mr. John Michael Cane',
    format: '%t%L%f%m')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.AiNameFormatRequest()
    .name('Mr. John Michael Cane')
    .format('%t%L%f%m')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::AiNameFormatRequest()
    ->name('Mr. John Michael Cane')
    ->format('%t%L%f%m')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="ai_name_format_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Ai.Name.FormatAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameFormatted result = api.ai().name().format(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.name.format(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.ai.name.format(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.ai.name.format(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->ai()->name()->format($request);
```

{{< /tab >}}

{{< /tabs >}}
## FormatParsed

Formats a person's parsed name in correct case and name order using options for formatting instructions. 
Returns [**AiNameFormatted**](/email/reference-model-ai-name-formatted/) model. Requires:

{{< expand-list title="request" >}}

Parsed name with options. Type: [**AiNameParsedRequest**](/email/reference-model-ai-name-parsed-request/).

{{< tabs tabTotal="6" tabID="ai_name_format_parsed_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameParsedRequest
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
AiNameParsedRequest request = Models.aiNameParsedRequest()
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
request = models.AiNameParsedRequest(
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
request = AiNameParsedRequest.new(
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
let request = Models.aiNameParsedRequest()
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
$request = Models::aiNameParsedRequest()
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

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="ai_name_format_parsed_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Ai.Name.FormatParsedAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameFormatted result = api.ai().name().formatParsed(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.name.format_parsed(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.ai.name.format_parsed(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.ai.name.formatParsed(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->ai()->name()->formatParsed($request);
```

{{< /tab >}}

{{< /tabs >}}
## Genderize

Detect person's gender from name string. 
Returns [**AiNameGenderHypothesisList**](/email/reference-model-ai-name-gender-hypothesis-list/) model. Requires:

{{< expand-list title="request" >}}

Genderize method request. Type: [**AiNameGenderizeRequest**](/email/reference-model-ai-name-genderize-request/).

{{< tabs tabTotal="6" tabID="ai_name_genderize_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameGenderizeRequest
{ 
    Name = "John Cane"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameGenderizeRequest request = Models.aiNameGenderizeRequest()
    .name("John Cane")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.AiNameGenderizeRequest(
    name='John Cane')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = AiNameGenderizeRequest.new(
    name: 'John Cane')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.AiNameGenderizeRequest()
    .name('John Cane')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::AiNameGenderizeRequest()
    ->name('John Cane')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="ai_name_genderize_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Ai.Name.GenderizeAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameGenderHypothesisList result = api.ai().name().genderize(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.name.genderize(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.ai.name.genderize(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.ai.name.genderize(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->ai()->name()->genderize($request);
```

{{< /tab >}}

{{< /tabs >}}
## GenderizeParsed

Detect person's gender from parsed name. 
Returns [**AiNameGenderHypothesisList**](/email/reference-model-ai-name-gender-hypothesis-list/) model. Requires:

{{< expand-list title="request" >}}

Gender detection request data. Type: [**AiNameParsedRequest**](/email/reference-model-ai-name-parsed-request/).

{{< tabs tabTotal="6" tabID="ai_name_genderize_parsed_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameParsedRequest
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
AiNameParsedRequest request = Models.aiNameParsedRequest()
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
request = models.AiNameParsedRequest(
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
request = AiNameParsedRequest.new(
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
let request = Models.aiNameParsedRequest()
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
$request = Models::aiNameParsedRequest()
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

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="ai_name_genderize_parsed_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Ai.Name.GenderizeParsedAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameGenderHypothesisList result = api.ai().name().genderizeParsed(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.name.genderize_parsed(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.ai.name.genderize_parsed(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.ai.name.genderizeParsed(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->ai()->name()->genderizeParsed($request);
```

{{< /tab >}}

{{< /tabs >}}
## Match

Compare people's names. Uses options for comparing instructions. 
Returns [**AiNameMatchResult**](/email/reference-model-ai-name-match-result/) model. Requires:

{{< expand-list title="request" >}}

Match method request. Type: [**AiNameMatchRequest**](/email/reference-model-ai-name-match-request/).

{{< tabs tabTotal="6" tabID="ai_name_match_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameMatchRequest
{ 
    Name = "John Michael Cane",
    OtherName = "Cane J."
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameMatchRequest request = Models.aiNameMatchRequest()
    .name("John Michael Cane")
    .otherName("Cane J.")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.AiNameMatchRequest(
    name='John Michael Cane',
    other_name='Cane J.')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = AiNameMatchRequest.new(
    name: 'John Michael Cane',
    other_name: 'Cane J.')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.AiNameMatchRequest()
    .name('John Michael Cane')
    .otherName('Cane J.')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::AiNameMatchRequest()
    ->name('John Michael Cane')
    ->other_name('Cane J.')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="ai_name_match_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Ai.Name.MatchAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameMatchResult result = api.ai().name().match(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.name.match(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.ai.name.match(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.ai.name.match(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->ai()->name()->match($request);
```

{{< /tab >}}

{{< /tabs >}}
## MatchParsed

Compare people's parsed names and attributes. Uses options for comparing instructions. 
Returns [**AiNameMatchResult**](/email/reference-model-ai-name-match-result/) model. Requires:

{{< expand-list title="request" >}}

Parsed names to match. Type: [**AiNameMatchParsedRequest**](/email/reference-model-ai-name-match-parsed-request/).

{{< tabs tabTotal="6" tabID="ai_name_match_parsed_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameMatchParsedRequest
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
            Score = 0,5,
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
            Score = 0,5
        }
    },
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
AiNameMatchParsedRequest request = Models.aiNameMatchParsedRequest()
    .otherParsedName(Arrays.<AiNameComponent>asList(
        Models.aiNameComponent()
            .value("J")
            .category("FirstInitial")
            .score(1)
            .build(),
        Models.aiNameComponent()
            .value("Cane")
            .category("LastName")
            .score(0,5)
            .position(3)
            .build(),
        Models.aiNameComponent()
            .value("%f%L")
            .category("Format")
            .build(),
        Models.aiNameComponent()
            .value("0.5")
            .category("Score")
            .score(0,5)
            .build()))
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
request = models.AiNameMatchParsedRequest(
    other_parsed_name=[
        models.AiNameComponent(
            value='J',
            category='FirstInitial',
            score=1),
        models.AiNameComponent(
            value='Cane',
            category='LastName',
            score=0,5,
            position=3),
        models.AiNameComponent(
            value='%f%L',
            category='Format'),
        models.AiNameComponent(
            value='0.5',
            category='Score',
            score=0,5)],
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
request = AiNameMatchParsedRequest.new(
  other_parsed_name: [
    AiNameComponent.new(
      value: 'J',
      category: 'FirstInitial',
      score: 1),
    AiNameComponent.new(
      value: 'Cane',
      category: 'LastName',
      score: 0,5,
      position: 3),
    AiNameComponent.new(
      value: '%f%L',
      category: 'Format'),
    AiNameComponent.new(
      value: '0.5',
      category: 'Score',
      score: 0,5)],
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
let request = Models.aiNameMatchParsedRequest()
    .otherParsedName([
        Models.aiNameComponent()
            .value('J')
            .category('FirstInitial')
            .score(1)
            .build(),
        Models.aiNameComponent()
            .value('Cane')
            .category('LastName')
            .score(0,5)
            .position(3)
            .build(),
        Models.aiNameComponent()
            .value('%f%L')
            .category('Format')
            .build(),
        Models.aiNameComponent()
            .value('0.5')
            .category('Score')
            .score(0,5)
            .build()])
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
$request = Models::aiNameMatchParsedRequest()
    ->otherParsedName(array(
        Models::aiNameComponent()
            ->value('J')
            ->category('FirstInitial')
            ->score(1)
            ->build(),
        Models::aiNameComponent()
            ->value('Cane')
            ->category('LastName')
            ->score(0,5)
            ->position(3)
            ->build(),
        Models::aiNameComponent()
            ->value('%f%L')
            ->category('Format')
            ->build(),
        Models::aiNameComponent()
            ->value('0.5')
            ->category('Score')
            ->score(0,5)
            ->build()))
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

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="ai_name_match_parsed_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Ai.Name.MatchParsedAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameMatchResult result = api.ai().name().matchParsed(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.name.match_parsed(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.ai.name.match_parsed(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.ai.name.matchParsed(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->ai()->name()->matchParsed($request);
```

{{< /tab >}}

{{< /tabs >}}
## Parse

Parse name to components. 
Returns [**AiNameComponentList**](/email/reference-model-ai-name-component-list/) model. Requires:

{{< expand-list title="request" >}}

Parse method request. Type: [**AiNameParseRequest**](/email/reference-model-ai-name-parse-request/).

{{< tabs tabTotal="6" tabID="ai_name_parse_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

{{< tabs tabTotal="6" tabID="ai_name_parse_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Ai.Name.ParseAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameComponentList result = api.ai().name().parse(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.name.parse(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.ai.name.parse(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.ai.name.parse(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->ai()->name()->parse($request);
```

{{< /tab >}}

{{< /tabs >}}
## ParseEmailAddress

Parse person's name out of an email address. 
Returns [**AiNameExtractedList**](/email/reference-model-ai-name-extracted-list/) model. Requires:

{{< expand-list title="request" >}}

ParseEmailAddress method request. Type: [**AiNameParseEmailAddressRequest**](/email/reference-model-ai-name-parse-email-address-request/).

{{< tabs tabTotal="6" tabID="ai_name_parse_email_address_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiNameParseEmailAddressRequest
{ 
    EmailAddress = "john-cane@gmail.com"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameParseEmailAddressRequest request = Models.aiNameParseEmailAddressRequest()
    .emailAddress("john-cane@gmail.com")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.AiNameParseEmailAddressRequest(
    email_address='john-cane@gmail.com')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = AiNameParseEmailAddressRequest.new(
    email_address: 'john-cane@gmail.com')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.AiNameParseEmailAddressRequest()
    .emailAddress('john-cane@gmail.com')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::AiNameParseEmailAddressRequest()
    ->email_address('john-cane@gmail.com')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="ai_name_parse_email_address_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Ai.Name.ParseEmailAddressAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameExtractedList result = api.ai().name().parseEmailAddress(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.name.parse_email_address(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.ai.name.parse_email_address(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.ai.name.parseEmailAddress(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->ai()->name()->parseEmailAddress($request);
```

{{< /tab >}}

{{< /tabs >}}

## More APIs

{{< list-of-articles-in-this-section >}}
