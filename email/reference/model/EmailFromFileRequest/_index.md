---
title: "EmailFromFileRequest"
type: docs
url: /reference-model-email-from-file-request/
weight: 2
---

Request model for [EmailCloud.Email.FromFile](/email/reference-email-api/#fromfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**format** |**string**| Enum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft |
**file** |**System.IO.Stream**|File to convert |

## Example

{{< tabs tabTotal="6" tabID="email_from_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailFromFileRequest
{ 
    Format = "Eml",
    File = new MemoryStream(File.ReadAllBytes("/path/to/message.eml"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailFromFileRequest request = Models.emailFromFileRequest()
    .format("Eml")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/message.eml")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailFromFileRequest(
    format='Eml',
    file='/path/to/message.eml')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailFromFileRequest.new(
    format: 'Eml',
    file: File.new('/path/to/message.eml'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.EmailFromFileRequest()
    .format('Eml')
    .file(fs.readFileSync('/path/to/message.eml'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::EmailFromFileRequest()
    ->format('Eml')
    ->file(new SplFileObject('/path/to/message.eml'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

