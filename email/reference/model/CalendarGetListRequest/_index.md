---
title: "CalendarGetListRequest"
type: docs
url: /reference-model-calendar-get-list-request/
weight: 2
---

Request model for [EmailCloud.Calendar.GetList](/email/reference-calendar-api/#getlist) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**folder** |**string**|Path to folder in storage. |
**itemsPerPage** |**int?**|Count of items on page. |[optional] [default to 10]
**pageNumber** |**int?**|Page number. |[optional] [default to 0]
**storage** |**string**|Storage name. |[optional] 

## Example

{{< tabs tabTotal="6" tabID="calendar_get_list_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarGetListRequest
{ 
    Folder = "some/folder/on/storage",
    ItemsPerPage = 10,
    PageNumber = 0,
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarGetListRequest request = Models.calendarGetListRequest()
    .folder("some/folder/on/storage")
    .itemsPerPage(10)
    .pageNumber(0)
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CalendarGetListRequest(
    folder='some/folder/on/storage',
    items_per_page=10,
    page_number=0,
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CalendarGetListRequest.new(
    folder: 'some/folder/on/storage',
    items_per_page: 10,
    page_number: 0,
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CalendarGetListRequest()
    .folder('some/folder/on/storage')
    .itemsPerPage(10)
    .pageNumber(0)
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CalendarGetListRequest()
    ->folder('some/folder/on/storage')
    ->items_per_page(10)
    ->page_number(0)
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

