---
title: "MapiContactGetRequest"
type: docs
url: /reference-model-mapi-contact-get-request/
weight: 2
---

Request model for [EmailCloud.Mapi.Contact.Get](/email/reference-mapi-contact-api/#get) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**format** |**string**|Contact document format. Enum, available values: VCard, WebDav, Msg |
**fileName** |**string**|Contact document file name. |
**folder** |**string**|Path to folder in storage. |[optional] 
**storage** |**string**|Storage name. |[optional] 

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="mapi_contact_get_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiContactGetRequest
{ 
    Format = "VCard",
    FileName = "contact.vcf",
    Folder = "folder/on/storage",
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiContactGetRequest request = Models.mapiContactGetRequest()
    .format("VCard")
    .fileName("contact.vcf")
    .folder("folder/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MapiContactGetRequest(
    format='VCard',
    file_name='contact.vcf',
    folder='folder/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MapiContactGetRequest.new(
    format: 'VCard',
    file_name: 'contact.vcf',
    folder: 'folder/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.MapiContactGetRequest()
    .format('VCard')
    .fileName('contact.vcf')
    .folder('folder/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::MapiContactGetRequest()
    ->format('VCard')
    ->file_name('contact.vcf')
    ->folder('folder/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

