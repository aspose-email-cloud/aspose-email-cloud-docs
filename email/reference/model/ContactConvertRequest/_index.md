---
title: "ContactConvertRequest"
type: docs
url: /reference-model-contact-convert-request/
weight: 2
---

Request model for [EmailCloud.Contact.Convert](/email/reference-contact-api/#convert) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**toFormat** |**string**|File format to convert to Enum, available values: VCard, WebDav, Msg |
**fromFormat** |**string**|File format to convert from Enum, available values: VCard, WebDav, Msg |
**file** |**System.IO.Stream**|File to convert |

## Example

{{< tabs tabTotal="6" tabID="contact_convert_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ContactConvertRequest
{ 
    ToFormat = "VCard",
    FromFormat = "Msg",
    File = new MemoryStream(File.ReadAllBytes("/path/to/contact.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactConvertRequest request = Models.contactConvertRequest()
    .toFormat("VCard")
    .fromFormat("Msg")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/contact.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ContactConvertRequest(
    to_format='VCard',
    from_format='Msg',
    file='/path/to/contact.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ContactConvertRequest.new(
    to_format: 'VCard',
    from_format: 'Msg',
    file: File.new('/path/to/contact.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ContactConvertRequest()
    .toFormat('VCard')
    .fromFormat('Msg')
    .file(fs.readFileSync('/path/to/contact.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ContactConvertRequest()
    ->to_format('VCard')
    ->from_format('Msg')
    ->file(new SplFileObject('/path/to/contact.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

