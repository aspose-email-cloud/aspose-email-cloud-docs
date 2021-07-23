---
title: "AI Powered Name API"
type: docs
url: /name-api/
weight: 16
description: "Process names with Artificial Intelligence functionality called Name API by using Aspose.Email Cloud API."
---

## **Introduction**
**Name API** is an AI feature developed by Aspose. This is a modern approach, which provides you with numerous useful functions to process names.

[Aspose.Email Cloud](https://products.aspose.cloud/email/family) now supports Artificial Intelligence functionalities and below we are going to emphasize **Name API** features.

**Name API** supports:
- Person's gender detection ([Genderize](/email/reference-ai-name-api/#genderize))
- Format name ([Format](/email/reference-ai-name-api/#format))
- Compare names ([Match](/email/reference-ai-name-api/#match))
- Expand name into list of possible alternatives ([Expand](/email/reference-ai-name-api/#expand))
- Complete name ([Complete](/email/reference-ai-name-api/#complete))
- Parse out a person's name from an email address ([ParseEmailAddress](/email/reference-ai-name-api/#parseemailaddress))
- Parse name to components ([Parse](/email/reference-ai-name-api/#parse))


{{% alert color="primary" %}} 

How to setup Aspose.Email Cloud SDKs: [**SDK setup**](/email/sdk-setup/).

{{% /alert %}}

## **How To Detect a Person's Gender By Name**

You can parse the name of a person and try determining the gender. The API result contains a list of hypotheses about a person's gender. All hypotheses include score, so you can use the most scored version, which will be the first in a list.

{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var result = await api.Ai.Name.GenderizeAsync(
    new AiNameGenderizeRequest("John Cane"));
Assert.GreaterOrEqual(result.Value.Count, 1);
Assert.True(result.Value.Any(item => item.Gender == "Male"));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ListResponseOfAiNameGenderHypothesis result = api.ai().name().genderize(
        new AiNameGenderizeRequest().name("John Cane"));
assert result.getValue().size() >= 1;
assert result.getValue().get(0).getGender().equals("Male");
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
result = api.ai.name.genderize(
    models.AiNameGenderizeRequest('John Cane'))
assert len(result.value) >= 1
assert result.value[0].gender == 'Male'
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
result = api.ai.name.genderize(
  AiNameGenderizeRequest.new(name: 'John Cane'))
expect(result.value.count).to be >= 1
expect(result.value[0].gender).to eq 'Male'
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const result = await api.ai.name.genderize(
    new AiNameGenderizeRequest('John Cane'));
expect(result.value.length).to.be.at.least(1);
expect(result.value[0].gender).to.be.equal('Male');
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = api->ai()->name()->genderize(
    new AiNameGenderizeRequest("John Cane"));
$this->assertGreaterThanOrEqual(1, count($result->getValue()));
$this->assertEquals('Male', $result->getValue()[0]->getGender());
```

{{< /tab >}}

{{< /tabs >}}

## **How To Compare Names To Determine The Similarity**

The AI feature of Aspose.Email Cloud API enables you to compare the names to find out if they belong to the same person or not. As a result of the comparison, the answer is the similarity score and the list of mismatches.

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
const string first = "John Michael Cane";
const string second = "Cane J.";
var result = await api.Ai.Name.MatchAsync(
    new AiNameMatchRequest(first, second));
Assert.True(result.Similarity > 0.5);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
final String first = "John Michael Cane";
final String second = "Cane J.";
AiNameMatchResult result = api.ai().name().match(
    new AiNameMatchRequest()
        .name(first)
        .otherName(second));
assert result.getSimilarity() >= 0.5;
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
first = 'John Michael Cane'
second = 'Cane J.'
result = api.ai.name.match(
    models.AiNameMatchRequest(first, second))
assert result.similarity >= 0.5
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
first = 'John Michael Cane'
second = 'Cane J.'
result = api.ai.name.match(
  AiNameMatchRequest.new(name: first, other_name: second))
expect(result.similarity).to be >= 0.5
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const first = 'John Michael Cane';
const second = 'Cane J.';
const result = await api.ai.name.match(
    new AiNameMatchRequest(first, second));
expect(result.similarity).to.be.at.least(0.5);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$first = "John Michael Cane";
$second = "Cane J.";
$result = api->ai()->name()->match(
    new AiNameMatchRequest($first, $second));
$this->assertGreaterThan(0.5, $result->getSimilarity());
```

{{< /tab >}}

{{< /tabs >}}

## **How To Format a Person's Name Using a Defined Format**

Aspose.Email Cloud is also capable of formatting a person's name in a correct case and name order using options for formatting instructions. So based on the instructions provided, the name sequence and case format are adjusted.

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var result = await api.Ai.Name.FormatAsync(
    new AiNameFormatRequest(
        "Mr. John Michael Cane",
        format: "%t%L%f%m"));
Assert.AreEqual("Mr. Cane J. M.", result.Name);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiNameFormatted result = api.ai().name().format(
    new AiNameFormatRequest()
        .name("Mr. John Michael Cane")
        .format("%t%L%f%m"));
assert result.getName().equals("Mr. Cane J. M.");
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
result = api.ai.name.format(
    models.AiNameFormatRequest(
        'Mr. John Michael Cane',
        format='%t%L%f%m'))
assert result.name == 'Mr. Cane J. M.'
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
result = api.ai.name.format(
  AiNameFormatRequest.new(
    name: 'Mr. John Michael Cane',
    format: '%t%L%f%m'))
expect(result.name).to eq 'Mr. Cane J. M.'
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const result = await api.ai.name.format(
    new AiNameFormatRequest(
        'Mr. John Michael Cane',
        undefined,
        undefined,
        undefined,
        undefined,
        '%t%L%f%m'));
expect(result.name).to.be.equal('Mr. Cane J. M.');
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = api->ai()->name()->format(
    new AiNameFormatRequest(
        "Mr. John Michael Cane",
        null,
        null,
        null,
        null,
        "%t%L%f%m"));
$this->assertEquals("Mr. Cane J. M.", $result->getName());
```

{{< /tab >}}

{{< /tabs >}}

## **How To Display Possible Alternatives For Name**

The AI feature of API provides a unique feature to display the person's name into a list of possible alternatives.

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
const string name = "Smith Bobby";
var result = await api.Ai.Name.ExpandAsync(
    new AiNameExpandRequest(name));
var expandedNames = result.Names
    .Select(weightedName => weightedName.Name)
    .ToList();
Assert.Contains("Mr. Smith", expandedNames);
Assert.Contains("B. Smith", expandedNames);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String name = "Smith Bobby";
AiNameWeightedVariants result = api.ai().name().expand(
    new AiNameExpandRequest().name(name));
ArrayList<String> expandedNames = new ArrayList<String>();
for (AiNameWeighted weighted : result.getNames()) {
    expandedNames.add(weighted.getName());
}
assert expandedNames.contains("Mr. Smith");
assert expandedNames.contains("B. Smith");
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
name = 'Smith Bobby'
result = api.ai.name.expand(
    models.AiNameExpandRequest(name))
expanded_names = list(
    weighted.name for weighted in result.names)
assert 'Mr. Smith' in expanded_names
assert 'B. Smith' in expanded_names
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
name = 'Smith Bobby'
result = api.ai.name.expand(
    AiNameExpandRequest.new(name: name))
mr = result.names.find do |weighted|
  weighted.name == 'Mr. Smith'
end
initial = result.names.find do |weighted|
  weighted.name == 'B. Smith'
end
expect(mr).not_to be_nil
expect(initial).not_to be_nil
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const result = await api.ai.name.expand(
    new AiNameExpandRequest('Smith Bobby'));
const names = result.names
    .map(weighted => weighted.name);
expect(names).to.contain('Mr. Smith');
expect(names).to.contain('B. Smith');
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$name = "Smith Bobby";
$result = api->ai()->name()->expand(
    new AiNameExpandRequest($name));
$expandedNames = array_map(function ($weightedName) {
    return $weightedName->getName();
}, $result->getNames());
$this->assertContains("Mr. Smith", $expandedNames);
$this->assertContains("B. Smith", $expandedNames);
```

{{< /tab >}}

{{< /tabs >}}

## **How To Guess Name Based On Initials**

Get the most probable names for given starting characters. The feature is similar to the recipient field in email client software. You start typing the name and based on initials provided, the possible names are listed. Please take a look over the following example where possible names starting with "**Dav**".

{{< tabs tabTotal="6" tabID="5" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
const string prefix = "Dav";
var result = await api.Ai.Name.CompleteAsync(
    new AiNameCompleteRequest(prefix));
var names = result.Names
    .Select(weightedName => $"{prefix}{weightedName.Name}")
    .ToList();
Assert.Contains("David", names);
Assert.Contains("Dave", names);
Assert.Contains("Davis", names);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String prefix = "Dav";
AiNameWeightedVariants result = api.ai().name().complete(
    new AiNameCompleteRequest().name(prefix));
ArrayList<String> names = new ArrayList<String>();
for (AiNameWeighted weighted : result.getNames()) {
    names.add(prefix + weighted.getName());
}
assert names.contains("David");
assert names.contains("Dave");
assert names.contains("Davis");
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
prefix = 'Dav'
result = api.ai.name.complete(
    models.AiNameCompleteRequest(prefix))
names = list(prefix + weighted.name for weighted in result.names)
assert 'David' in names
assert 'Dave' in names
assert 'Davis' in names
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
prefix = 'Dav'
result = api.ai.name.complete(
  AiNameCompleteRequest.new(name: prefix))
names = result.names.map do |weighted|
  "#{prefix}#{weighted.name}"
end
expect(names).to include 'David'
expect(names).to include 'Davis'
expect(names).to include 'Dave'
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const prefix = 'Dav';
const result = await api.ai.name.complete(
    new AiNameCompleteRequest(prefix));
const names = result.names
    .map(weighted => prefix + weighted.name);
expect(names).to.contain('David');
expect(names).to.contain('Davis');
expect(names).to.contain('Dave');
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$prefix = "Dav";
$result = api->ai()->name()->complete(
    new AiNameCompleteRequest($prefix));
$names = array_map(function ($weightedName) use ($prefix) {
    return $prefix . $weightedName->getName();
}, $result->getNames());
$this->assertContains("David", $names);
$this->assertContains("Dave", $names);
$this->assertContains("Davis", $names);
```

{{< /tab >}}

{{< /tabs >}}

## **How To Parse Name From Email Address**

The API enables you to determine the name of the person through an email address. It tries to identify the Firstname and Lastname while parsing the given email address.

{{< tabs tabTotal="6" tabID="6" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
const string address = "john-cane@gmail.com";
var result = await api.Ai.Name.ParseEmailAddressAsync(
    new AiNameParseEmailAddressRequest(address));
var extractedValues = result.Value
    .SelectMany(value => value.Name)
    .ToList();
var givenName = extractedValues.First(value => value.Category == "GivenName");
var surName = extractedValues.First(value => value.Category == "Surname");
Assert.AreEqual("John", givenName.Value);
Assert.AreEqual("Cane", surName.Value);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String address = "john-cane@gmail.com";
ListResponseOfAiNameExtracted result = api.ai().name().parseEmailAddress(
    new AiNameParseEmailAddressRequest().emailAddress(address));
String givenName = null;
String surname = null;
for (AiNameExtracted extracted : result.getValue()) {
    for (AiNameExtractedComponent component : extracted.getName()) {
        if (component.getCategory().equals("GivenName")) {
            givenName = component.getValue();
        }
        if (component.getCategory().equals("Surname")) {
            surname = component.getValue();
        }
    }
}
assert "John".equals(givenName);
assert "Cane".equals(surname);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
address = 'john-cane@gmail.com'
result = api.ai.name.parse_email_address(
    models.AiNameParseEmailAddressRequest(address))
names = (extracted.name for extracted in result.value)
extracted_values = list(functools.reduce(lambda a, b: a + b, names))
given_name = next((x for x in extracted_values if x.category == 'GivenName'))
surname = next((x for x in extracted_values if x.category == 'Surname'))
assert given_name.value == 'John'
assert surname.value == 'Cane'
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
address = 'john-cane@gmail.com'
result = api.ai.name.parse_email_address(
  AiNameParseEmailAddressRequest.new(
    email_address: address))
extracted_values = result.value
                         .map(&:name)
                         .reduce(:+)
given_name = extracted_values.find do |item|
  item.category == 'GivenName'
end                   
surname = extracted_values.find do |item|
  item.category == 'Surname'
end                
expect(given_name.value).to eq 'John'
expect(surname.value).to eq 'Cane'
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const result = await api.ai.name.parseEmailAddress(
    new AiNameParseEmailAddressRequest('john-cane@gmail.com'));
const extractedValues = result.value
    .map(extracted => extracted.name)
    .reduce((accumulator, value) => accumulator.concat(value));
const givenName = extractedValues.find(
    extracted => extracted.category == 'GivenName');
const surname = extractedValues.find(
    extracted => extracted.category == 'Surname');
expect(givenName.value).to.be.equal('John');
expect(surname.value).to.be.equal('Cane');
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$address = "john-cane@gmail.com";
$result = api->ai()->name()->parseEmailAddress(
    new AiNameParseEmailAddressRequest($address));
$extractedNames = array_map(function ($value) {
    return $value->getName();
}, $result->getValue());
$reduced = array_reduce($extractedNames, 'array_merge', array());
$givenName = array_values(array_filter($reduced, function ($value) {
    return $value->getCategory() == "GivenName";
}))[0];
$surname = array_values(array_filter($reduced, function ($value) {
    return $value->getCategory() == "Surname";
}))[0];
$this->assertEquals("John", $givenName->getValue());
$this->assertEquals("Cane", $surname->getValue());
```

{{< /tab >}}

{{< /tabs >}}

## **More Tutorials**
See more Aspose Email Tutorials: 
{{< list-of-articles-in-this-section >}}
