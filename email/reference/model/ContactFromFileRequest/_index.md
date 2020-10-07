---
title: "ContactFromFileRequest"
type: docs
url: /reference-model-contact-from-file-request/
weight: 2
---

Request model for [EmailCloud.Contact.FromFile](/email/reference-contact-api/#fromfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**format** |**string**|File format Enum, available values: VCard, WebDav, Msg |
**file** |**System.IO.Stream**|File to convert |

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="contact_from_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ContactFromFileRequest
{ 
    Format = "Msg",
    File = new MemoryStream(File.ReadAllBytes("/path/to/contact.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactFromFileRequest request = Models.contactFromFileRequest()
    .format("Msg")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/contact.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ContactFromFileRequest(
    format='Msg',
    file='/path/to/contact.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ContactFromFileRequest.new(
    format: 'Msg',
    file: File.new('/path/to/contact.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ContactFromFileRequest()
    .format('Msg')
    .file(fs.readFileSync('/path/to/contact.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ContactFromFileRequest()
    ->format('Msg')
    ->file(new SplFileObject('/path/to/contact.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

