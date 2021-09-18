---
title: "CalendarGetAsFileRequest"
type: docs
url: /reference-model-calendar-get-as-file-request/
weight: 2
---

Request model for [EmailCloud.Calendar.GetAsFile](/email/reference-calendar-api/#getasfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**fileName** |**string**|Calendar document file name. |
**format** |**string**|File format./nEnum, available values: Ics, Msg |
**storage** |**string**|Storage name. |[optional] 
**folder** |**string**|Path to folder in storage. |[optional] 

## Example

{{< tabs tabTotal="6" tabID="calendar_get_as_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarGetAsFileRequest
{ 
    FileName = "calendar.msg",
    Format = "Ics",
    Storage = "First Storage",
    Folder = "calendar/file/location/on/storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarGetAsFileRequest request = Models.calendarGetAsFileRequest()
    .fileName("calendar.msg")
    .format("Ics")
    .storage("First Storage")
    .folder("calendar/file/location/on/storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CalendarGetAsFileRequest(
    file_name='calendar.msg',
    format='Ics',
    storage='First Storage',
    folder='calendar/file/location/on/storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CalendarGetAsFileRequest.new(
    file_name: 'calendar.msg',
    format: 'Ics',
    storage: 'First Storage',
    folder: 'calendar/file/location/on/storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CalendarGetAsFileRequest()
    .fileName('calendar.msg')
    .format('Ics')
    .storage('First Storage')
    .folder('calendar/file/location/on/storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CalendarGetAsFileRequest()
    ->file_name('calendar.msg')
    ->format('Ics')
    ->storage('First Storage')
    ->folder('calendar/file/location/on/storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

