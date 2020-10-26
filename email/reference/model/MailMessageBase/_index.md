---
title: "MailMessageBase"
type: docs
url: /reference-model-mail-message-base/
weight: 1
---
Universal object that stores email messages in different formats.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Discriminator** | **string** |  | 


## Example

{{< tabs tabTotal="6" tabID="mail_message_base_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mailMessageBase = new MailMessageBase
{
    
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MailMessageBase mailMessageBase = Models.mailMessageBase()
    
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
mail_message_base = models.MailMessageBase(
    )
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
mail_message_base = MailMessageBase.new(
  )
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let mailMessageBase = Models.mailMessageBase()
    
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mailMessageBase = Models::mailMessageBase()
    
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

