---
title: "EmailConvertRequest"
type: docs
url: /reference-model-email-convert-request/
weight: 2
---

Request model for [EmailCloud.Email.Convert](/email/reference-email-api/#convert) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**fromFormat** |**string**|File format to convert from. Enum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft |
**toFormat** |**string**|File format to convert to. Enum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft |
**file** |**System.IO.Stream**|File to convert |

## Example

{{< tabs tabTotal="6" tabID="email_convert_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailConvertRequest
{ 
    FromFormat = "Msg",
    ToFormat = "Mhtml",
    File = new MemoryStream(File.ReadAllBytes("/path/to/message.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailConvertRequest request = Models.emailConvertRequest()
    .fromFormat("Msg")
    .toFormat("Mhtml")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/message.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailConvertRequest(
    from_format='Msg',
    to_format='Mhtml',
    file='/path/to/message.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailConvertRequest.new(
    from_format: 'Msg',
    to_format: 'Mhtml',
    file: File.new('/path/to/message.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.EmailConvertRequest()
    .fromFormat('Msg')
    .toFormat('Mhtml')
    .file(fs.readFileSync('/path/to/message.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::EmailConvertRequest()
    ->from_format('Msg')
    ->to_format('Mhtml')
    ->file(new SplFileObject('/path/to/message.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

