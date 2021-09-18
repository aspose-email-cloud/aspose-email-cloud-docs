---
title: "CalendarConvertRequest"
type: docs
url: /reference-model-calendar-convert-request/
weight: 2
---

Request model for [EmailCloud.Calendar.Convert](/email/reference-calendar-api/#convert) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**format** |**string**|File format. Enum, available values: Ics, Msg |
**file** |**System.IO.Stream**|File to convert |

## Example

{{< tabs tabTotal="6" tabID="calendar_convert_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarConvertRequest
{ 
    Format = "Ics",
    File = new MemoryStream(File.ReadAllBytes("/path/to/calendar.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarConvertRequest request = Models.calendarConvertRequest()
    .format("Ics")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/calendar.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CalendarConvertRequest(
    format='Ics',
    file='/path/to/calendar.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CalendarConvertRequest.new(
    format: 'Ics',
    file: File.new('/path/to/calendar.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CalendarConvertRequest()
    .format('Ics')
    .file(fs.readFileSync('/path/to/calendar.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CalendarConvertRequest()
    ->format('Ics')
    ->file(new SplFileObject('/path/to/calendar.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

