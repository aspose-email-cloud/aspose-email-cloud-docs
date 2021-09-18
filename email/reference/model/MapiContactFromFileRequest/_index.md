---
title: "MapiContactFromFileRequest"
type: docs
url: /reference-model-mapi-contact-from-file-request/
weight: 2
---

Request model for [EmailCloud.Mapi.Contact.FromFile](/email/reference-mapi-contact-api/#fromfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**format** |**string**|File format. Enum, available values: VCard, WebDav, Msg |
**file** |**System.IO.Stream**|File to convert |

## Example

{{< tabs tabTotal="6" tabID="mapi_contact_from_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiContactFromFileRequest
{ 
    Format = "Msg",
    File = new MemoryStream(File.ReadAllBytes("/path/to/contact.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiContactFromFileRequest request = Models.mapiContactFromFileRequest()
    .format("Msg")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/contact.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MapiContactFromFileRequest(
    format='Msg',
    file='/path/to/contact.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MapiContactFromFileRequest.new(
    format: 'Msg',
    file: File.new('/path/to/contact.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.MapiContactFromFileRequest()
    .format('Msg')
    .file(fs.readFileSync('/path/to/contact.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::MapiContactFromFileRequest()
    ->format('Msg')
    ->file(new SplFileObject('/path/to/contact.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

