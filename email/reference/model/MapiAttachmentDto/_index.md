---
title: "MapiAttachmentDto"
type: docs
url: /reference-model-mapi-attachment-dto/
weight: 1
---
Mapi attachment             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Name** | **string** | Attachment&#39;s name              | [optional] 
**DataBase64** | **string** | Attachment data represented as Base64 string.              | [optional] 


## Example

{{< tabs tabTotal="6" tabID="mapi_attachment_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mapiAttachmentDto = new MapiAttachmentDto
{
    Name = "some-file.txt",
    DataBase64 = "U29tZSBmaWxlIHRleHQ="
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiAttachmentDto mapiAttachmentDto = Models.mapiAttachmentDto()
    .name("some-file.txt")
    .dataBase64("U29tZSBmaWxlIHRleHQ=")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
mapi_attachment_dto = models.MapiAttachmentDto(
    name='some-file.txt',
    data_base64='U29tZSBmaWxlIHRleHQ=')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
mapi_attachment_dto = MapiAttachmentDto.new(
  name: 'some-file.txt',
  data_base64: 'U29tZSBmaWxlIHRleHQ=')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let mapiAttachmentDto = Models.mapiAttachmentDto()
    .name('some-file.txt')
    .dataBase64('U29tZSBmaWxlIHRleHQ=')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapiAttachmentDto = Models::mapiAttachmentDto()
    ->name('some-file.txt')
    ->dataBase64('U29tZSBmaWxlIHRleHQ=')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

