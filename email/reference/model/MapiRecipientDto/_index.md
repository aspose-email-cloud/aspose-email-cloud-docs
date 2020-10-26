---
title: "MapiRecipientDto"
type: docs
url: /reference-model-mapi-recipient-dto/
weight: 1
---
Represents the recipient information in the Microsoft Outlook Message.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**EmailAddress** | **string** | Email address of the message recipient or sender.              | [optional] 
**AddressType** | **string** | Type of the address of the message recipient or sender.              | [optional] 
**DisplayName** | **string** | Display name of the message recipient or sender.              | [optional] 
**RecipientType** | **string** | Represent the PR_RECIPIENT_TYPE property which contains the recipient type for a message recipient. Enum, available values: Unknown, MapiBcc, MapiCc, MapiP1, MapiSubmitted, MapiTo | 


## Example

{{< tabs tabTotal="6" tabID="mapi_recipient_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mapiRecipientDto = new MapiRecipientDto
{
    EmailAddress = "to@aspose.com",
    AddressType = "SMTP",
    DisplayName = "To Address",
    RecipientType = "MapiTo"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiRecipientDto mapiRecipientDto = Models.mapiRecipientDto()
    .emailAddress("to@aspose.com")
    .addressType("SMTP")
    .displayName("To Address")
    .recipientType("MapiTo")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
mapi_recipient_dto = models.MapiRecipientDto(
    email_address='to@aspose.com',
    address_type='SMTP',
    display_name='To Address',
    recipient_type='MapiTo')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
mapi_recipient_dto = MapiRecipientDto.new(
  email_address: 'to@aspose.com',
  address_type: 'SMTP',
  display_name: 'To Address',
  recipient_type: 'MapiTo')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let mapiRecipientDto = Models.mapiRecipientDto()
    .emailAddress('to@aspose.com')
    .addressType('SMTP')
    .displayName('To Address')
    .recipientType('MapiTo')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapiRecipientDto = Models::mapiRecipientDto()
    ->emailAddress('to@aspose.com')
    ->addressType('SMTP')
    ->displayName('To Address')
    ->recipientType('MapiTo')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

