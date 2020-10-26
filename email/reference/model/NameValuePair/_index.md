---
title: "NameValuePair"
type: docs
url: /reference-model-name-value-pair/
weight: 1
---
Name-Value property             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Name** | **string** | Property name              | [optional] 
**Value** | **string** | Property value              | [optional] 


## Example

{{< tabs tabTotal="6" tabID="name_value_pair_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var nameValuePair = new NameValuePair
{
    Name = "name",
    Value = "value"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
NameValuePair nameValuePair = Models.nameValuePair()
    .name("name")
    .value("value")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
name_value_pair = models.NameValuePair(
    name='name',
    value='value')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
name_value_pair = NameValuePair.new(
  name: 'name',
  value: 'value')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let nameValuePair = Models.nameValuePair()
    .name('name')
    .value('value')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$nameValuePair = Models::nameValuePair()
    ->name('name')
    ->value('value')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

