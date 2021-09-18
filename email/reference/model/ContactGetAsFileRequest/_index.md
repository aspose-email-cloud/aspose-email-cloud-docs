---
title: "ContactGetAsFileRequest"
type: docs
url: /reference-model-contact-get-as-file-request/
weight: 2
---

Request model for [EmailCloud.Contact.GetAsFile](/email/reference-contact-api/#getasfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**fileName** |**string**|Calendar document file name |
**toFormat** |**string**|File format./nEnum, available values: VCard, WebDav, Msg |
**fromFormat** |**string**|File format to convert from./nEnum, available values: VCard, WebDav, Msg |
**storage** |**string**|Storage name |[optional] 
**folder** |**string**|Path to folder in storage |[optional] 

## Example

{{< tabs tabTotal="6" tabID="contact_get_as_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ContactGetAsFileRequest
{ 
    FileName = "contact.msg",
    ToFormat = "VCard",
    FromFormat = "Msg",
    Storage = "First Storage",
    Folder = "folder/on/storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactGetAsFileRequest request = Models.contactGetAsFileRequest()
    .fileName("contact.msg")
    .toFormat("VCard")
    .fromFormat("Msg")
    .storage("First Storage")
    .folder("folder/on/storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ContactGetAsFileRequest(
    file_name='contact.msg',
    to_format='VCard',
    from_format='Msg',
    storage='First Storage',
    folder='folder/on/storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ContactGetAsFileRequest.new(
    file_name: 'contact.msg',
    to_format: 'VCard',
    from_format: 'Msg',
    storage: 'First Storage',
    folder: 'folder/on/storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ContactGetAsFileRequest()
    .fileName('contact.msg')
    .toFormat('VCard')
    .fromFormat('Msg')
    .storage('First Storage')
    .folder('folder/on/storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ContactGetAsFileRequest()
    ->file_name('contact.msg')
    ->to_format('VCard')
    ->from_format('Msg')
    ->storage('First Storage')
    ->folder('folder/on/storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

