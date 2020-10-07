---
title: "MapiResponseTypePropertyDto"
type: docs
url: /reference-model-mapi-response-type-property-dto/
weight: 1
---
Mapi property with response type value             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Value** | **string** | Represents the types of recipient responses that are received for a meeting. Enum, available values: Unknown, Organizer, Tentative, Accept, Decline, NoResponseReceived | 

Parent class: [MapiPropertyDto](/email/reference-model-mapi-property-dto/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="mapi_response_type_property_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mapiResponseTypePropertyDto = new MapiResponseTypePropertyDto
{
    Value = "Accept",
    Descriptor = new MapiKnownPropertyDescriptor
    {
        Name = "ResponseStatus"
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiResponseTypePropertyDto mapiResponseTypePropertyDto = Models.mapiResponseTypePropertyDto()
    .value("Accept")
    .descriptor(Models.mapiKnownPropertyDescriptor()
        .name("ResponseStatus")
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
mapi_response_type_property_dto = models.MapiResponseTypePropertyDto(
    value='Accept',
    descriptor=models.MapiKnownPropertyDescriptor(
        name='ResponseStatus'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
mapi_response_type_property_dto = MapiResponseTypePropertyDto.new(
  value: 'Accept',
  descriptor: MapiKnownPropertyDescriptor.new(
    name: 'ResponseStatus'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let mapiResponseTypePropertyDto = Models.mapiResponseTypePropertyDto()
    .value('Accept')
    .descriptor(Models.mapiKnownPropertyDescriptor()
        .name('ResponseStatus')
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapiResponseTypePropertyDto = Models::mapiResponseTypePropertyDto()
    ->value('Accept')
    ->descriptor(Models::mapiKnownPropertyDescriptor()
        ->name('ResponseStatus')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

