---
title: "MapiCalendarGetRequest"
type: docs
url: /reference-model-mapi-calendar-get-request/
weight: 2
---

Request model for [EmailCloud.Mapi.Calendar.Get](/email/reference-mapi-calendar-api/#get) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**fileName** |**string**|Calendar file name in storage. |
**folder** |**string**|Path to folder in storage. |[optional] 
**storage** |**string**|Storage name. |[optional] 

## Example

{{< tabs tabTotal="6" tabID="mapi_calendar_get_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiCalendarGetRequest
{ 
    FileName = "calendar.msg",
    Folder = "calendar/location/on/storage",
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiCalendarGetRequest request = Models.mapiCalendarGetRequest()
    .fileName("calendar.msg")
    .folder("calendar/location/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MapiCalendarGetRequest(
    file_name='calendar.msg',
    folder='calendar/location/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MapiCalendarGetRequest.new(
    file_name: 'calendar.msg',
    folder: 'calendar/location/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.MapiCalendarGetRequest()
    .fileName('calendar.msg')
    .folder('calendar/location/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::MapiCalendarGetRequest()
    ->file_name('calendar.msg')
    ->folder('calendar/location/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

