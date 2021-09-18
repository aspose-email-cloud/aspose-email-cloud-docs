---
title: "MapiMessageAsFileRequest"
type: docs
url: /reference-model-mapi-message-as-file-request/
weight: 1
---
Convert MapiMessage to file request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Format** | **string** | Email document format. Enum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft | 
**Value** | [**MapiMessageDto**](/email/reference-model-mapi-message-dto/) | MAPI message model.              | 


## Example

{{< tabs tabTotal="6" tabID="mapi_message_as_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mapiMessageAsFileRequest = new MapiMessageAsFileRequest
{
    Format = "Msg",
    Value = new MapiMessageDto
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
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiMessageAsFileRequest mapiMessageAsFileRequest = Models.mapiMessageAsFileRequest()
    .format("Msg")
    .value(Models.mapiMessageDto()
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
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
mapi_message_as_file_request = models.MapiMessageAsFileRequest(
    format='Msg',
    value=models.MapiMessageDto(
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
        subject_prefix='Re: '))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
mapi_message_as_file_request = MapiMessageAsFileRequest.new(
  format: 'Msg',
  value: MapiMessageDto.new(
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
    subject_prefix: 'Re: '))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let mapiMessageAsFileRequest = Models.mapiMessageAsFileRequest()
    .format('Msg')
    .value(Models.mapiMessageDto()
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
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapiMessageAsFileRequest = Models::mapiMessageAsFileRequest()
    ->format('Msg')
    ->value(Models::mapiMessageDto()
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
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

