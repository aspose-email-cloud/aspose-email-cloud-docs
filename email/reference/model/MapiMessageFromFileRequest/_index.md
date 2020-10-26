---
title: "MapiMessageFromFileRequest"
type: docs
url: /reference-model-mapi-message-from-file-request/
weight: 2
---

Request model for [EmailCloud.Mapi.Message.FromFile](/email/reference-mapi-message-api/#fromfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**format** |**string**|File format Enum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft |
**file** |**System.IO.Stream**|File to convert |

## Example

{{< tabs tabTotal="6" tabID="mapi_message_from_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiMessageFromFileRequest
{ 
    Format = "Msg",
    File = new MemoryStream(File.ReadAllBytes("/path/to/message.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiMessageFromFileRequest request = Models.mapiMessageFromFileRequest()
    .format("Msg")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/message.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MapiMessageFromFileRequest(
    format='Msg',
    file='/path/to/message.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MapiMessageFromFileRequest.new(
    format: 'Msg',
    file: File.new('/path/to/message.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.MapiMessageFromFileRequest()
    .format('Msg')
    .file(fs.readFileSync('/path/to/message.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::MapiMessageFromFileRequest()
    ->format('Msg')
    ->file(new SplFileObject('/path/to/message.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

