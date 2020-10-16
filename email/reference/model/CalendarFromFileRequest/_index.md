---
title: "CalendarFromFileRequest"
type: docs
url: /reference-model-calendar-from-file-request/
weight: 2
---

Request model for [EmailCloud.Calendar.FromFile](/email/reference-calendar-api/#fromfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**file** |**System.IO.Stream**|File to convert |

## Example

{{< tabs tabTotal="6" tabID="calendar_from_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CalendarFromFileRequest
{ 
    File = new MemoryStream(File.ReadAllBytes("/path/to/calendar.ics"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CalendarFromFileRequest request = Models.calendarFromFileRequest()
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/calendar.ics")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CalendarFromFileRequest(
    file='/path/to/calendar.ics')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CalendarFromFileRequest.new(
    file: File.new('/path/to/calendar.ics'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CalendarFromFileRequest()
    .file(fs.readFileSync('/path/to/calendar.ics'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CalendarFromFileRequest()
    ->file(new SplFileObject('/path/to/calendar.ics'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

