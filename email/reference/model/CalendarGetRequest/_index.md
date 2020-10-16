---
title: "CalendarGetRequest"
type: docs
url: /reference-model-calendar-get-request/
weight: 2
---

Request model for [EmailCloud.Calendar.Get](/email/reference-calendar-api/#get) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**fileName** |**string**|iCalendar file name in storage. |
**folder** |**string**|Path to folder in storage. |[optional] 
**storage** |**string**|Storage name. |[optional] 

## Example

{{< tabs tabTotal="6" tabID="calendar_get_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarGetRequest
{ 
    FileName = "calendar.ics",
    Folder = "calendar/location/on/storage",
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarGetRequest request = Models.calendarGetRequest()
    .fileName("calendar.ics")
    .folder("calendar/location/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CalendarGetRequest(
    file_name='calendar.ics',
    folder='calendar/location/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CalendarGetRequest.new(
    file_name: 'calendar.ics',
    folder: 'calendar/location/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CalendarGetRequest()
    .fileName('calendar.ics')
    .folder('calendar/location/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CalendarGetRequest()
    ->file_name('calendar.ics')
    ->folder('calendar/location/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

