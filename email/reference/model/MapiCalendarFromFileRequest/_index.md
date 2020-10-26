---
title: "MapiCalendarFromFileRequest"
type: docs
url: /reference-model-mapi-calendar-from-file-request/
weight: 2
---

Request model for [EmailCloud.Mapi.Calendar.FromFile](/email/reference-mapi-calendar-api/#fromfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**file** |**System.IO.Stream**|File to convert |

## Example

{{< tabs tabTotal="6" tabID="mapi_calendar_from_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiCalendarFromFileRequest
{ 
    File = new MemoryStream(File.ReadAllBytes("/path/to/calendar.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiCalendarFromFileRequest request = Models.mapiCalendarFromFileRequest()
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/calendar.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MapiCalendarFromFileRequest(
    file='/path/to/calendar.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MapiCalendarFromFileRequest.new(
    file: File.new('/path/to/calendar.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.MapiCalendarFromFileRequest()
    .file(fs.readFileSync('/path/to/calendar.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::MapiCalendarFromFileRequest()
    ->file(new SplFileObject('/path/to/calendar.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

