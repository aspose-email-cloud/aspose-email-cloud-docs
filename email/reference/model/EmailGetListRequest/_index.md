---
title: "EmailGetListRequest"
type: docs
url: /reference-model-email-get-list-request/
weight: 2
---

Request model for [EmailCloud.Email.GetList](/email/reference-email-api/#getlist) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**format** |**string**|Email document format./nEnum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft |
**folder** |**string**|Path to folder in storage. |[optional] 
**storage** |**string**|Storage name. |[optional] 
**itemsPerPage** |**int?**|Count of items on page. |[optional] [default to 10]
**pageNumber** |**int?**|Page number. |[optional] [default to 0]

## Example

{{< tabs tabTotal="6" tabID="email_get_list_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailGetListRequest
{ 
    Format = "Eml",
    Folder = "folder/on/storage",
    Storage = "First Storage",
    ItemsPerPage = 10,
    PageNumber = 0
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailGetListRequest request = Models.emailGetListRequest()
    .format("Eml")
    .folder("folder/on/storage")
    .storage("First Storage")
    .itemsPerPage(10)
    .pageNumber(0)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailGetListRequest(
    format='Eml',
    folder='folder/on/storage',
    storage='First Storage',
    items_per_page=10,
    page_number=0)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailGetListRequest.new(
    format: 'Eml',
    folder: 'folder/on/storage',
    storage: 'First Storage',
    items_per_page: 10,
    page_number: 0)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.EmailGetListRequest()
    .format('Eml')
    .folder('folder/on/storage')
    .storage('First Storage')
    .itemsPerPage(10)
    .pageNumber(0)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::EmailGetListRequest()
    ->format('Eml')
    ->folder('folder/on/storage')
    ->storage('First Storage')
    ->items_per_page(10)
    ->page_number(0)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

