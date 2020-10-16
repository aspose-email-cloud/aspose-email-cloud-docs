---
title: "MapiStringPropertyDto"
type: docs
url: /reference-model-mapi-string-property-dto/
weight: 1
---
Mapi property with string value             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Value** | **string** | Property value              | [optional] 

Parent class: [MapiPropertyDto](/email/reference-model-mapi-property-dto/)

## Example

{{< tabs tabTotal="6" tabID="mapi_string_property_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mapiStringPropertyDto = new MapiStringPropertyDto
{
    Value = "SomeName",
    Descriptor = new MapiKnownPropertyDescriptor
    {
        Name = "DisplayName"
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiStringPropertyDto mapiStringPropertyDto = Models.mapiStringPropertyDto()
    .value("SomeName")
    .descriptor(Models.mapiKnownPropertyDescriptor()
        .name("DisplayName")
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
mapi_string_property_dto = models.MapiStringPropertyDto(
    value='SomeName',
    descriptor=models.MapiKnownPropertyDescriptor(
        name='DisplayName'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
mapi_string_property_dto = MapiStringPropertyDto.new(
  value: 'SomeName',
  descriptor: MapiKnownPropertyDescriptor.new(
    name: 'DisplayName'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let mapiStringPropertyDto = Models.mapiStringPropertyDto()
    .value('SomeName')
    .descriptor(Models.mapiKnownPropertyDescriptor()
        .name('DisplayName')
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapiStringPropertyDto = Models::mapiStringPropertyDto()
    ->value('SomeName')
    ->descriptor(Models::mapiKnownPropertyDescriptor()
        ->name('DisplayName')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

