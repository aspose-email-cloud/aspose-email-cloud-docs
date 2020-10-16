---
title: "CalendarGetAsAlternateRequest"
type: docs
url: /reference-model-calendar-get-as-alternate-request/
weight: 2
---

Request model for [EmailCloud.Calendar.GetAsAlternate](/email/reference-calendar-api/#getasalternate) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**fileName** |**string**|iCalendar file name in storage |
**calendarAction** |**string**|iCalendar method type Enum, available values: Create, Update, Cancel |
**sequenceId** |**string**|The sequence id |[optional] 
**folder** |**string**|Path to folder in storage |[optional] 
**storage** |**string**|Storage name |[optional] 

## Example

{{< tabs tabTotal="6" tabID="calendar_get_as_alternate_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarGetAsAlternateRequest
{ 
    FileName = "calendar.ics",
    CalendarAction = "Create",
    Folder = "calendar/location/on/storage",
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarGetAsAlternateRequest request = Models.calendarGetAsAlternateRequest()
    .fileName("calendar.ics")
    .calendarAction("Create")
    .folder("calendar/location/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CalendarGetAsAlternateRequest(
    file_name='calendar.ics',
    calendar_action='Create',
    folder='calendar/location/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CalendarGetAsAlternateRequest.new(
    file_name: 'calendar.ics',
    calendar_action: 'Create',
    folder: 'calendar/location/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CalendarGetAsAlternateRequest()
    .fileName('calendar.ics')
    .calendarAction('Create')
    .folder('calendar/location/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CalendarGetAsAlternateRequest()
    ->file_name('calendar.ics')
    ->calendar_action('Create')
    ->folder('calendar/location/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

