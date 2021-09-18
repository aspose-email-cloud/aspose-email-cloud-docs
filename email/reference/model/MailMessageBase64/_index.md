---
title: "MailMessageBase64"
type: docs
url: /reference-model-mail-message-base64/
weight: 1
---
Email message represented as file, encoded to Base64 format.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**ValueBase64** | **string** | Email message file data encoded to Base64 string.              | 
**Format** | **string** | Email document format./nEnum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft | 

Parent class: [MailMessageBase](/email/reference-model-mail-message-base/)

## Example

{{< tabs tabTotal="6" tabID="mail_message_base64_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mailMessageBase64 = new MailMessageBase64
{
    ValueBase64 = "RnJvbTogZkBmLnVzClRvOiB0QHQudXMKU3ViamVjdDogUwoKQm9keQ=="
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MailMessageBase64 mailMessageBase64 = Models.mailMessageBase64()
    .valueBase64("RnJvbTogZkBmLnVzClRvOiB0QHQudXMKU3ViamVjdDogUwoKQm9keQ==")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
mail_message_base64 = models.MailMessageBase64(
    value_base64='RnJvbTogZkBmLnVzClRvOiB0QHQudXMKU3ViamVjdDogUwoKQm9keQ==')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
mail_message_base64 = MailMessageBase64.new(
  value_base64: 'RnJvbTogZkBmLnVzClRvOiB0QHQudXMKU3ViamVjdDogUwoKQm9keQ==')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let mailMessageBase64 = Models.mailMessageBase64()
    .valueBase64('RnJvbTogZkBmLnVzClRvOiB0QHQudXMKU3ViamVjdDogUwoKQm9keQ==')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mailMessageBase64 = Models::mailMessageBase64()
    ->valueBase64('RnJvbTogZkBmLnVzClRvOiB0QHQudXMKU3ViamVjdDogUwoKQm9keQ==')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

