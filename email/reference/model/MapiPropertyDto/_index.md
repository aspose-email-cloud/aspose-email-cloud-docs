---
title: "MapiPropertyDto"
type: docs
url: /reference-model-mapi-property-dto/
weight: 1
---
Mapi property             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Descriptor** | [**MapiPropertyDescriptor**](/email/reference-model-mapi-property-descriptor/) | Property descriptor              | [optional] 
**Discriminator** | **string** |  | 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="mapi_property_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mapiPropertyDto = new MapiPropertyDto
{
    Descriptor = new MapiKnownPropertyDescriptor
    {
        Name = "DisplayName"
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiPropertyDto mapiPropertyDto = Models.mapiPropertyDto()
    .descriptor(Models.mapiKnownPropertyDescriptor()
        .name("DisplayName")
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
mapi_property_dto = models.MapiPropertyDto(
    descriptor=models.MapiKnownPropertyDescriptor(
        name='DisplayName'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
mapi_property_dto = MapiPropertyDto.new(
  descriptor: MapiKnownPropertyDescriptor.new(
    name: 'DisplayName'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let mapiPropertyDto = Models.mapiPropertyDto()
    .descriptor(Models.mapiKnownPropertyDescriptor()
        .name('DisplayName')
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapiPropertyDto = Models::mapiPropertyDto()
    ->descriptor(Models::mapiKnownPropertyDescriptor()
        ->name('DisplayName')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

