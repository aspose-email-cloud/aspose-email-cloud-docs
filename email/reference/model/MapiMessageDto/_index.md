---
title: "MapiMessageDto"
type: docs
url: /reference-model-mapi-message-dto/
weight: 1
---
Represents an Outlook Message format document.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**MessageBody** | **string** | Message text              | [optional] 
**ClientSubmitTime** | **DateTime?** | Date and time the message sender submitted a message.              | 
**ConversationTopic** | **string** | Topic of the first message in a conversation thread.              | [optional] 
**DeliveryTime** | **DateTime?** | Date and time a message was delivered.              | 
**DisplayBcc** | **string** | List of the display names of any blind carbon copy (BCC) message recipients, separated by semicolons (;).              | [optional] 
**DisplayCc** | **string** | List of the display names of any carbon copy (CC) message recipients, separated by semicolons (;).              | [optional] 
**DisplayName** | **string** | Display name for the message.              | [optional] 
**DisplayNamePrefix** | **string** | Prefix of the display name.              | [optional] 
**DisplayTo** | **string** | List of the display names of the primary (To) message recipients, separated by semicolons (;).              | [optional] 
**Flags** | **List&lt;string&gt;** | Message flags.              Items: Mapi message flags./nEnum, available values: MsgFlagZero, MsgFlagRead, MsgFlagUnmodified, MsgFlagSubmit, MsgFlagUnsent, MsgFlagHasAttach, MsgFlagFromMe, MsgFlagAssociated, MsgFlagResend, MsgFlagNotifyRead, MsgFlagNotifyUnread, MsgFlagEverRead, MsgFlagOriginX400, MsgFlagOriginInternet, MsgFlagOriginMiscExt | [optional] 
**Headers** | **Dictionary&lt;string, string&gt;** | Transport message headers              | [optional] 
**InternetMessageId** | **string** | Internet message id of the message.              | [optional] 
**MessageFormat** | **string** | Represents outlook message format./nEnum, available values: Ascii, Unicode | 
**NormalizedSubject** | **string** | Normalized subject of the message.              | [optional] 
**ReadReceiptRequested** | **bool?** | Value indicating whether the read receipt is requested. | 
**ReplyTo** | **string** | Reply to names. | [optional] 
**SenderAddressType** | **string** | Message sender&#39;s e-mail address type. | [optional] 
**SenderEmailAddress** | **string** | Message sender&#39;s e-mail address. | [optional] 
**SenderName** | **string** | Message sender&#39;s display name. | [optional] 
**SenderSmtpAddress** | **string** | Message sender&#39;s e-mail address. | [optional] 
**SentRepresentingAddressType** | **string** | Address type for the messaging user represented by the sender. | [optional] 
**SentRepresentingEmailAddress** | **string** | E-mail address for the messaging user represented by the sender. | [optional] 
**SentRepresentingName** | **string** | Display name for the messaging user represented by the sender. | [optional] 
**SentRepresentingSmtpAddress** | **string** | E-mail address for the messaging user represented by the sender. | [optional] 
**TransportMessageHeaders** | **string** | Transport-specific message envelope information. | [optional] 

Parent class: [MapiMessageItemBaseDto](/email/reference-model-mapi-message-item-base-dto/)

## Example

{{< tabs tabTotal="6" tabID="mapi_message_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mapiMessageDto = new MapiMessageDto
{
    MessageBody = "Some body",
    ClientSubmitTime = DateTime.Today,
    DeliveryTime = DateTime.Today,
    DisplayTo = "To Address",
    Flags = new List<MapiMessageFlag>
    {
        "MsgFlagRead",
        "MsgFlagUnsent",
        "MsgFlagHasAttach"
    },
    NormalizedSubject = "Some subject",
    SenderAddressType = "SMTP",
    SenderEmailAddress = "from@aspose.com",
    SenderName = "From Address",
    SenderSmtpAddress = "from@aspose.com",
    Attachments = new List<MapiAttachmentDto>
    {
        new MapiAttachmentDto
        {
            Name = "some-file.txt",
            DataBase64 = "U29tZSBmaWxlIHRleHQ="
        }
    },
    Body = "Some body",
    MessageClass = "IPM.Note",
    Recipients = new List<MapiRecipientDto>
    {
        new MapiRecipientDto
        {
            EmailAddress = "to@aspose.com",
            AddressType = "SMTP",
            DisplayName = "To Address",
            RecipientType = "MapiTo"
        }
    },
    Subject = "Re: Some subject",
    SubjectPrefix = "Re: "
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiMessageDto mapiMessageDto = Models.mapiMessageDto()
    .messageBody("Some body")
    .clientSubmitTime(Calendar.getInstance().getTime())
    .deliveryTime(Calendar.getInstance().getTime())
    .displayTo("To Address")
    .flags(Arrays.<MapiMessageFlag>asList(
        "MsgFlagRead",
        "MsgFlagUnsent",
        "MsgFlagHasAttach"))
    .normalizedSubject("Some subject")
    .senderAddressType("SMTP")
    .senderEmailAddress("from@aspose.com")
    .senderName("From Address")
    .senderSmtpAddress("from@aspose.com")
    .attachments(Arrays.<MapiAttachmentDto>asList(
        Models.mapiAttachmentDto()
            .name("some-file.txt")
            .dataBase64("U29tZSBmaWxlIHRleHQ=")
            .build()))
    .body("Some body")
    .messageClass("IPM.Note")
    .recipients(Arrays.<MapiRecipientDto>asList(
        Models.mapiRecipientDto()
            .emailAddress("to@aspose.com")
            .addressType("SMTP")
            .displayName("To Address")
            .recipientType("MapiTo")
            .build()))
    .subject("Re: Some subject")
    .subjectPrefix("Re: ")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
mapi_message_dto = models.MapiMessageDto(
    message_body='Some body',
    client_submit_time=datetime.today(),
    delivery_time=datetime.today(),
    display_to='To Address',
    flags=[
        'MsgFlagRead',
        'MsgFlagUnsent',
        'MsgFlagHasAttach'],
    normalized_subject='Some subject',
    sender_address_type='SMTP',
    sender_email_address='from@aspose.com',
    sender_name='From Address',
    sender_smtp_address='from@aspose.com',
    attachments=[
        models.MapiAttachmentDto(
            name='some-file.txt',
            data_base64='U29tZSBmaWxlIHRleHQ=')],
    body='Some body',
    message_class='IPM.Note',
    recipients=[
        models.MapiRecipientDto(
            email_address='to@aspose.com',
            address_type='SMTP',
            display_name='To Address',
            recipient_type='MapiTo')],
    subject='Re: Some subject',
    subject_prefix='Re: ')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
mapi_message_dto = MapiMessageDto.new(
  message_body: 'Some body',
  client_submit_time: DateTime.now,
  delivery_time: DateTime.now,
  display_to: 'To Address',
  flags: [
    'MsgFlagRead',
    'MsgFlagUnsent',
    'MsgFlagHasAttach'],
  normalized_subject: 'Some subject',
  sender_address_type: 'SMTP',
  sender_email_address: 'from@aspose.com',
  sender_name: 'From Address',
  sender_smtp_address: 'from@aspose.com',
  attachments: [
    MapiAttachmentDto.new(
      name: 'some-file.txt',
      data_base64: 'U29tZSBmaWxlIHRleHQ=')],
  body: 'Some body',
  message_class: 'IPM.Note',
  recipients: [
    MapiRecipientDto.new(
      email_address: 'to@aspose.com',
      address_type: 'SMTP',
      display_name: 'To Address',
      recipient_type: 'MapiTo')],
  subject: 'Re: Some subject',
  subject_prefix: 'Re: ')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let mapiMessageDto = Models.mapiMessageDto()
    .messageBody('Some body')
    .clientSubmitTime(new Date())
    .deliveryTime(new Date())
    .displayTo('To Address')
    .flags([
        'MsgFlagRead',
        'MsgFlagUnsent',
        'MsgFlagHasAttach'])
    .normalizedSubject('Some subject')
    .senderAddressType('SMTP')
    .senderEmailAddress('from@aspose.com')
    .senderName('From Address')
    .senderSmtpAddress('from@aspose.com')
    .attachments([
        Models.mapiAttachmentDto()
            .name('some-file.txt')
            .dataBase64('U29tZSBmaWxlIHRleHQ=')
            .build()])
    .body('Some body')
    .messageClass('IPM.Note')
    .recipients([
        Models.mapiRecipientDto()
            .emailAddress('to@aspose.com')
            .addressType('SMTP')
            .displayName('To Address')
            .recipientType('MapiTo')
            .build()])
    .subject('Re: Some subject')
    .subjectPrefix('Re: ')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapiMessageDto = Models::mapiMessageDto()
    ->messageBody('Some body')
    ->clientSubmitTime(new DateTime())
    ->deliveryTime(new DateTime())
    ->displayTo('To Address')
    ->flags(array(
        'MsgFlagRead',
        'MsgFlagUnsent',
        'MsgFlagHasAttach'))
    ->normalizedSubject('Some subject')
    ->senderAddressType('SMTP')
    ->senderEmailAddress('from@aspose.com')
    ->senderName('From Address')
    ->senderSmtpAddress('from@aspose.com')
    ->attachments(array(
        Models::mapiAttachmentDto()
            ->name('some-file.txt')
            ->dataBase64('U29tZSBmaWxlIHRleHQ=')
            ->build()))
    ->body('Some body')
    ->messageClass('IPM.Note')
    ->recipients(array(
        Models::mapiRecipientDto()
            ->emailAddress('to@aspose.com')
            ->addressType('SMTP')
            ->displayName('To Address')
            ->recipientType('MapiTo')
            ->build()))
    ->subject('Re: Some subject')
    ->subjectPrefix('Re: ')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

