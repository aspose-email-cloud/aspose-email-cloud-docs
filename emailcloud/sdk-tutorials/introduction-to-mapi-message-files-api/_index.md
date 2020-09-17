---
title: "Introduction to MAPI Message Files API"
type: docs
url: /introduction-to-mapi-message-files-api/
description: " Instructions on how to use MAPI message files API in Aspose.Email Cloud SDK. How to work with MAPI in Cloud SDK for .NET, Java, PHP, Python, Ruby, Node.js."
weight: 90
---

## **MAPI Message Files**
[Aspose.Email Cloud](https://products.aspose.cloud/email/family) supports files in Microsoft Outlook Email format ([MSG](https://docs.fileformat.com/email/msg/) files).

First of all, the MSG file could be represented as a list of properties. See this JSON example:

<details>
  <summary>MSG file properties list represented as a JSON array</summary>

```json
{
  "properties": [
    {
      "value": "High",
      "descriptor": {
        "name": "Importance",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiImportancePropertyDto"
    },
    {
      "value": "IPM.Note",
      "descriptor": {
        "name": "MessageClass",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "value": 0,
      "descriptor": {
        "name": "Sensitivity",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiIntPropertyDto"
    },
    {
      "value": "Re: Some subject",
      "descriptor": {
        "name": "TagSubject",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "valueBase64": "U01UUDpGUk9NQEFTUE9TRS5DT00A",
      "descriptor": {
        "name": "SentRepresentingSearchKey",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiBinaryPropertyDto"
    },
    {
      "value": "Re: ",
      "descriptor": {
        "name": "SubjectPrefix",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "value": "From Address <from@aspose.com>",
      "descriptor": {
        "name": "SentRepresentingName",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "value": null,
      "descriptor": {
        "name": "SentRepresentingAddressType",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "value": "from@aspose.com",
      "descriptor": {
        "name": "SentRepresentingEmailAddress",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "value": "From: \"From Address\" <from@aspose.com>\r\nReply-To: \r\nTo: \"To Address\" <to@aspose.com>\r\nBcc: \r\nCc: \r\nPriority: urgent\r\nX-Priority: High\r\nImportance: High\r\nSensitivity: None\r\nSubject: Re: Some subject\r\nDate: Mon, 1 Jan 1 00:00:00 +0000\r\nX-Unsent: 1\r\nDisposition-Notification-To: \r\nMIME-Version: 1.0\r\n\r\n",
      "descriptor": {
        "name": "TransportMessageHeaders",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "valueBase64": "AAAAAIErH6S+oxAZnW4A3QEPVAIAAAGAZgByAG8AbQBAAGEAcwBwAG8AcwBlAC4AYwBvAG0AAABTAE0AVABQAAAAZgByAG8AbQBAAGEAcwBwAG8AcwBlAC4AYwBvAG0AAAA=",
      "descriptor": {
        "name": "SenderEntryId",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiBinaryPropertyDto"
    },
    {
      "value": "From Address",
      "descriptor": {
        "name": "SenderName",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "valueBase64": "U01UUDpGUk9NQEFTUE9TRS5DT00A",
      "descriptor": {
        "name": "SenderSearchKey",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiBinaryPropertyDto"
    },
    {
      "value": "SMTP",
      "descriptor": {
        "name": "SenderAddressType",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "value": "from@aspose.com",
      "descriptor": {
        "name": "SenderEmailAddress",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "value": null,
      "descriptor": {
        "name": "DisplayBcc",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "value": null,
      "descriptor": {
        "name": "DisplayCc",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "value": "To Address",
      "descriptor": {
        "name": "DisplayTo",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "value": 25,
      "descriptor": {
        "name": "MessageFlags",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiIntPropertyDto"
    },
    {
      "value": true,
      "descriptor": {
        "name": "HasAttachments",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiBooleanPropertyDto"
    },
    {
      "value": "Some subject",
      "descriptor": {
        "name": "NormalizedSubject",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "value": true,
      "descriptor": {
        "name": "RtfInSync",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiBooleanPropertyDto"
    },
    {
      "value": 2,
      "descriptor": {
        "name": "Access",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiIntPropertyDto"
    },
    {
      "value": 0,
      "descriptor": {
        "name": "AccessLevel",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiIntPropertyDto"
    },
    {
      "value": "Some body",
      "descriptor": {
        "name": "Body",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    {
      "valueBase64": "/QAAAP0AAABNRUxBAAAAAHtccnRmMVxhbnNpXGFuc2ljcGcxMjUyXGZyb21odG1sMSBcZmJpZGlzIFxkZWZmMHtcZm9udHRibA0Ke1xmMFxmc3dpc3MgQXJpYWw7fX0NCntcY29sb3J0YmxccmVkMFxncmVlbjBcYmx1ZTA7fQ0KXHVjMVxwYXJkXHBsYWluXGRlZnRhYjM2MCBcZjBcZnMyNA0Ke1wqXGh0bWx0YWc4NCA8Yj59XGh0bWxydGYge1xiIFxodG1scnRmMCBTb21lIGJvZHkNCntcKlxodG1sdGFnOTIgPC9iPn1caHRtbHJ0ZiB9XGh0bWxydGYwIH0=",
      "descriptor": {
        "name": "RtfCompressed",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiBinaryPropertyDto"
    },
    {
      "valueBase64": "PGI+U29tZSBib2R5PC9iPg==",
      "descriptor": {
        "name": "TagHtml",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiBinaryPropertyDto"
    },
    {
      "value": "2020-07-07T13:07:10.7317118Z",
      "descriptor": {
        "name": "CreationTime",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiDateTimePropertyDto"
    },
    {
      "value": "2020-07-07T13:07:10.7317118Z",
      "descriptor": {
        "name": "LastModificationTime",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiDateTimePropertyDto"
    },
    {
      "valueBase64": "zuEv0QAAAAAAAAAAAAAAAA==",
      "descriptor": {
        "name": "SearchKey",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiBinaryPropertyDto"
    },
    {
      "value": 134777,
      "descriptor": {
        "name": "StoreSupportMask",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiIntPropertyDto"
    },
    {
      "value": 65001,
      "descriptor": {
        "name": "InternetCodepage",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiIntPropertyDto"
    },
    {
      "value": false,
      "descriptor": {
        "name": "AgingDontAgeMe",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiBooleanPropertyDto"
    }
  ]
}
```

</details>

These properties could contain different values. It could be integers, strings, bytes, multiple strings, and a lot of other data types. All properties are identified using property Descriptors. Aspose.Email Cloud supports different types of property descriptors:

- *MapiPidTagPropertyDescriptor* - A property, identified by a tag, which consists of a combination of data type and identifier.
- *MapiPidLidPropertyDescriptor* - A property, identified by a long id and a property set.
- *MapiPidNamePropertyDescriptor* - A property, identified by a name and a property set.
- *MapiKnownPropertyDescriptor* - This descriptor implies one of three previous descriptors. It is a property, that is known to Aspose.Email Cloud, so it can be fully identified by the property name.
See all known properties [here](https://apireference.aspose.com/email/net/aspose.email.mapi/knownpropertylist/fields/index).

Aspose.Email Cloud provides 3 different models to represent the MSG file. These models contain a list of all properties and extra fields for easier file operation. For example, [**MapiMessageDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/MapiMessageDto.md) has a string field named *Subject*, which contains a subject for an email message. But this field is just a copy of a property with a [TagSubject](https://apireference.aspose.com/email/net/aspose.email.mapi/knownpropertylist/fields/tagsubject) descriptor:

<details>
  <summary>Part of MapiMessageDto JSON with subject</summary>

```json
{
  //...
  "subject": "Re: Some subject",
  //...
  "properties": [
    //...
    {
      "value": "Re: Some subject",
      "descriptor": {
        "name": "TagSubject",
        "discriminator": "MapiKnownPropertyDescriptor"
      },
      "discriminator": "MapiStringPropertyDto"
    },
    //...
  ],
  //...
}
```

</details>

These 3 MAPI models are:

1. [**MapiMessageDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/MapiMessageDto.md) - represents an email message. Has properties to represent a message's subject, body, sender, recipients, etc.
1. [**MapiCalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/MapiCalendarDto.md) - represents an appointment or a meeting object. Provides properties for meeting start and end, location, recurrence, busy status, etc.
1. [**MapiContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/MapiContactDto.md) - represents a contact. Provides properties for name, telephone, email addresses, etc.

All these models can be converted to the corresponding usual models and back:

- [**MapiMessageDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/MapiMessageDto.md) <-> [**EmailDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailDto.md)
- [**MapiCalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/MapiCalendarDto.md) <-> [**CalendarDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/CalendarDto.md)
- [**MapiContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/MapiContactDto.md) <-> [**ContactDto**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ContactDto.md)

Aspose.Email Cloud also provides methods to save these models to files in different formats and to read these files back to the corresponding models.



{{% alert color="primary" %}} 

MapiMessageDto:

- [MSG](https://docs.fileformat.com/email/msg/)
- [EML](https://docs.fileformat.com/email/eml/)
- [HTML](https://docs.fileformat.com/web/html/)
- [MHTML](https://docs.fileformat.com/web/mhtml/)
- [TNEF](https://docs.fileformat.com/email/tnef/)

MapiCalendarDto:

- [MSG](https://docs.fileformat.com/email/msg/)
- [ICS](https://docs.fileformat.com/email/ics/)

MapiContactDto:

- [MSG](https://docs.fileformat.com/email/msg/)
- [VCF](https://docs.fileformat.com/email/vcf/)

{{% /alert %}} 


## **Quick start with MAPI message files API**

{{% alert color="primary" %}} 

To see how to set up SDKs use the [SDK setup](/emailcloud/sdk-setup/) tutorial.

{{% /alert %}} 

Aspose.Email Cloud SDK provides the same sets of methods for all supported MAPI models:

- Convert from the usual model to a MAPI model.
- Convert from the MAPI model to a usual model.
- Convert a MAPI model object to a file in a specified format.
- Read a file to a MAPI model.
- Save a MAPI model as a file on the cloud storage.
- Read a file from the cloud storage to a MAPI model.

You can see all these methods in action in examples below:
### **MapiMessageDto methods**
#### **Convert EmailDto to MapiMessageDto**

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
EmailDto emailDto = new EmailDto
{
    Subject = "Re: Some subject",
    Body = "Some body",
    IsBodyHtml = true,
    HtmlBody = "<b>Some body</b>",
    BodyType = "Html",
    IsDraft = true,
    Attachments = new List<Attachment>
    {
        new Attachment
        {
            Base64Data =
                Convert.ToBase64String(Encoding.UTF8.GetBytes("Some file content")),
            Name = "some-file.txt"
        }
    },
    DeliveryNotificationOptions = new List<string> {"OnSuccess", "Delay"},
    From = new MailAddress {Address = FromAddress, DisplayName = "From Address"},
    To = new List<MailAddress>
        {new MailAddress {Address = "to@aspose.com", DisplayName = "To Address"}}
};
var mapiMessage = await api.Email.AsMapiAsync(emailDto);
Assert.AreEqual(emailDto.Subject, mapiMessage.Subject);
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```java
EmailDto emailDto = new EmailDto()
    .from(new MailAddress().address(from))
    .addToItem(new MailAddress().address("to@aspose.com"))
    .subject("Some subject")
    .body("Some body")
    .date(new Date());
MapiMessageDto mapiMessageDto = api.email().asMapi(emailDto);
assert emailDto.getSubject().equals(mapiMessageDto.getSubject());
```
{{< /tab >}}
{{< tab tabNum="3" >}}
```py
email_document = models.EmailDto(
    _from=models.MailAddress(address='from@aspose.com'),
    to=[models.MailAddress(address='to@aspose.com')],
    subject='Some subject',
    body='Some body',
    _date=datetime.today())
mapi_message = api.email.as_mapi(email_document)
assert email_document.subject == mapi_message.subject
```
{{< /tab >}}
{{< tab tabNum="4" >}}
```rb
email = EmailDto.new(
  from: MailAddress.new(address: 'from@aspose.com'),
  to: [MailAddress.new(address: 'to@aspose.com')],
  subject: 'Some subject',
  body: 'Some body',
  date: DateTime.now)
mapi_message = api.email.as_mapi(email)
expect(email.subject).to eq mapi_message.subject
```
{{< /tab >}}
{{< tab tabNum="5" >}}
```ts
const emailDto = new EmailDto();
emailDto.from = new MailAddress(undefined, from);
emailDto.to = [new MailAddress(undefined, 'to@aspose.com')];
emailDto.subject = 'Some subject';
emailDto.body = 'Some body';
emailDto.date = new Date();

const mapiMessageDto = await api.email.asMapi(emailDto);
expect(emailDto.subject).to.be.eq(mapiMessageDto.subject);
```
{{< /tab >}}
{{< tab tabNum="6" >}}
```php
$emailDto = (new EmailDto())
    ->setFrom(new MailAddress(null, 'from@aspose.com'))
    ->setTo(array(new MailAddress(null, 'to@aspose.com')))
    ->setSubject('Some subject')
    ->setBody('Some body')
    ->setDate(new DateTime());
$mapiMessage = $api->email()->asMapi($emailDto);
$this->assertEquals($emailDto->getSubject(), $mapiMessage->getSubject());
```
{{< /tab >}}
{{< /tabs >}}
#### **Convert MapiMessageDto to EmailDto**

{{< tabs tabTotal="6" tabID="10" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}
{{< tab tabNum="1" >}}
```cs
MapiMessageDto mapiMessage = new MapiMessageDto
{
    Body = "Some body", Subject = "Re: Some subject", BodyType = "PlainText",
    DeliveryTime = DateTime.Today, DisplayTo = "To Address", MessageBody = "Some body",
    MessageClass = "IPM.Note", MessageFormat = "Ascii", NormalizedSubject = "Some subject",
    SenderName = "From Address", SubjectPrefix = "Re: ", ClientSubmitTime = DateTime.Today,
    SenderAddressType = "SMTP", SenderEmailAddress = "from@aspose.com",
    SenderSmtpAddress = "from@aspose.com",
    Attachments = new List<MapiAttachmentDto>
    {
        new MapiAttachmentDto
        {
            DataBase64 = Convert.ToBase64String(Encoding.UTF8.GetBytes("Some file text")),
            Name = "some-file.txt"
        }
    },
    Flags = new List<string> {"MsgFlagRead", "MsgFlagUnsent", "MsgFlagHasAttach"},
    Recipients = new List<MapiRecipientDto>
    {
        new MapiRecipientDto
        {
            AddressType = "SMTP", DisplayName = "To Address",
            EmailAddress = "to@aspose.com", RecipientType = "MapiTo"
        }
    }
};
var emailDto = await api.Mapi.Message.AsEmailDtoAsync(mapiMessage);
Assert.AreEqual(mapiMessage.Subject, emailDto.Subject);
Assert.AreEqual(mapiMessage.Body, emailDto.Body);
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```java
MapiMessageDto mapiMessage = (MapiMessageDto) new MapiMessageDto()
    .clientSubmitTime(Calendar.getInstance().getTime())
    .senderAddressType("SMTP")
    .senderEmailAddress("from@aspose.com")
    .senderSmtpAddress("from@aspose.com")
    .messageFormat("Ascii")
    .senderName("From Address")
    .messageBody("Some body")
    .displayTo("To Address")
    .deliveryTime(Calendar.getInstance().getTime())
    .normalizedSubject("Some subject")
    .flags(Arrays.asList("MsgFlagRead", "MsgFlagUnsent", "MsgFlagHasAttach"))
    .addRecipientsItem(new MapiRecipientDto()
        .addressType("SMTP")
        .displayName("To address")
        .emailAddress("to@aspose.com")
        .recipientType("MapiTo"))
    .addAttachmentsItem(new MapiAttachmentDto()
        .dataBase64(Base64.encodeToString("Some file text".getBytes(), false))
        .name("some-file.txt"))
    .subjectPrefix("Re: ")
    .messageClass("IPM.Note")
    .body("Some body")
    .subject("Re: Some subject")
    .bodyType("PlainText");
EmailDto emailDto = api.mapi().message().asEmailDto(mapiMessage);
assert mapiMessage.getSubject().equals(emailDto.getSubject());
assert mapiMessage.getBody().equals(emailDto.getBody());
```
{{< /tab >}}
{{< tab tabNum="3" >}}
```py
mapi_message = models.MapiMessageDto(
    sender_address_type='SMTP',
    sender_email_address='from@aspose.com',
    sender_smtp_address='from@aspose.com',
    sender_name='From Address',
    message_body='Some body',
    display_to='To Address',
    delivery_time=datetime.today(),
    flags=['MsgFlagRead', 'MsgFlagUnsent', 'MsgFlagHasAttach'],
    recipients=[models.MapiRecipientDto(
        address_type='SMTP',
        display_name='To address',
        email_address='to@aspose.com',
        recipient_type='MapiTo'
    )],
    attachments=[models.MapiAttachmentDto(
        data_base64=str(base64.b64encode(b'Some file text'), 'utf-8'),
        name='some-file.txt'
    )],
    body='Some body',
    subject='Re: Some subject',
    body_type='PlainText'
)
email = api.mapi.message.as_email_dto(mapi_message)
assert mapi_message.subject == email.subject
assert mapi_message.body == email.body
```
{{< /tab >}}
{{< tab tabNum="4" >}}
```rb
mapi_message = MapiMessageDto.new(
  sender_address_type: 'SMTP',
  sender_email_address: 'from@aspose.com',
  sender_smtp_address: 'from@aspose.com',
  sender_name: 'From Address',
  message_body: 'Some body',
  display_to: 'To Address',
  delivery_time: DateTime.now,
  flags: %w[MsgFlagRead MsgFlagUnsent MsgFlagHasAttach],
  recipients: [MapiRecipientDto.new(
    address_type: 'SMTP',
    display_name: 'To address',
    email_address: 'to@aspose.com',
    recipient_type: 'MapiTo')],
  attachments: [MapiAttachmentDto.new(
    data_base64: Base64.encode64('Some file text'),
    name: 'some-file.txt')],
  body: 'Some body',
  subject: 'Re: Some subject',
  body_type: 'PlainText')
email = api.mapi.message.as_email_dto(mapi_message)
expect(mapi_message.subject).to eq email.subject
expect(mapi_message.body).to eq email.body
```
{{< /tab >}}
{{< tab tabNum="5" >}}
```ts
const mapiMessageDto = new MapiMessageDto();
mapiMessageDto.clientSubmitTime = new Date();
mapiMessageDto.senderAddressType = "SMTP";
mapiMessageDto.senderEmailAddress = "from@aspose.com";
mapiMessageDto.senderSmtpAddress = "from@aspose.com";
mapiMessageDto.messageFormat = "Ascii";
mapiMessageDto.senderName = "From Address";
mapiMessageDto.messageBody = "Some body";
mapiMessageDto.displayTo = "To Address";
mapiMessageDto.deliveryTime = new Date();
mapiMessageDto.normalizedSubject = "Some subject";
mapiMessageDto.flags = ["MsgFlagRead", "MsgFlagUnsent", "MsgFlagHasAttach"];
const recipientDto = new MapiRecipientDto();
recipientDto.addressType = "SMTP";
recipientDto.displayName = "To address";
recipientDto.emailAddress = "to@aspose.com";
recipientDto.recipientType = "MapiTo";
mapiMessageDto.recipients = [recipientDto];
const attachment = new MapiAttachmentDto();
attachment.dataBase64 = Buffer.from("Some file text").toString('base64');
attachment.name = "some-file.txt";
mapiMessageDto.attachments = [attachment];
mapiMessageDto.subjectPrefix = "Re: ";
mapiMessageDto.messageClass = "IPM.Note";
mapiMessageDto.body = "Some body";
mapiMessageDto.subject = "Re: Some subject";
mapiMessageDto.bodyType = "PlainText";

const emailDto = await api.mapi.message.asEmailDto(mapiMessageDto);
expect(mapiMessageDto.subject).to.be.eq(emailDto.subject);
expect(mapiMessageDto.body).to.be.eq(emailDto.body);
```
{{< /tab >}}
{{< tab tabNum="6" >}}
```php
$mapiMessage = (new MapiMessageDto())
    ->setClientSubmitTime(new DateTime())
    ->setSenderAddressType("SMTP")
    ->setSenderEmailAddress("from@aspose.com")
    ->setSenderSmtpAddress("from@aspose.com")
    ->setMessageFormat("Ascii")
    ->setSenderName("From Address")
    ->setMessageBody("Some body")
    ->setDisplayTo("To Address")
    ->setDeliveryTime(new DateTime())
    ->setNormalizedSubject("Some subject")
    ->setFlags(array("MsgFlagRead", "MsgFlagUnsent", "MsgFlagHasAttach"))
    ->setRecipients(array((new MapiRecipientDto())
        ->setAddressType("SMTP")
        ->setDisplayName("To address")
        ->setEmailAddress("to@aspose.com")
        ->setRecipientType("MapiTo")))
    ->setAttachments(array((new MapiAttachmentDto())
        ->setDataBase64(base64_encode("Some file text"))
        ->setName("some-file.txt")))
    ->setSubjectPrefix("Re: ")
    ->setMessageClass("IPM.Note")
    ->setBody("Some body")
    ->setSubject("Re: Some subject")
    ->setBodyType("PlainText");

$emailDto = $api->mapi()->message()->asEmailDto($mapiMessage);
$this->assertEquals($mapiMessage->getSubject(), $emailDto->getSubject());
$this->assertEquals($mapiMessage->getBody(), $emailDto->getBody());
```
{{< /tab >}}

{{< /tabs >}}
#### **Convert MapiMessageDto to a File and Back**
**Convert MapiMessageDto to a File and Back**

{{< tabs tabTotal="6" tabID="17" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var emlStream =
    await Api.Mapi.Message.AsFileAsync(
        new MapiMessageAsFileRequest("Eml", mapiMessage));
using (var memoryStream = new MemoryStream())
{
    await emlStream.CopyToAsync(memoryStream);
    var emlString = Encoding.UTF8.GetString(memoryStream.ToArray());
    Assert.IsTrue(emlString.Contains(mapiMessage.Subject));
}

emlStream.Seek(0, SeekOrigin.Begin);
var mapiMessageConverted =
    await Api.Mapi.Message.FromFileAsync(
        new MapiMessageFromFileRequest("Eml", emlStream));
Assert.AreEqual(mapiMessage.Subject, mapiMessageConverted.Subject);
//Subject is also available as MapiPropertyDto:
var subjectProperty = mapiMessageConverted.Properties.First(p =>
        //There are different Property descriptors supported.
        //Some properties are known to the service, so we can find them by name:
        (p.Descriptor as MapiKnownPropertyDescriptor)?.Name == "TagSubject")
    //Subject is a string, so it is stored in MapiStringPropertyDto:
    as MapiStringPropertyDto;
Assert.AreEqual(mapiMessage.Subject, subjectProperty?.Value);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] emlBytes =
    api.mapi().message().asFile(new MapiMessageAsFileRequest("Eml", mapiMessage));
String emlString = new String(emlBytes, "UTF-8");
assert emlString.contains(mapiMessage.getSubject());
MapiMessageDto mapiMessageConverted =
    api.mapi().message().fromFile(new MapiMessageFromFileRequest("Eml", emlBytes));
assert mapiMessage.getSubject().equals(mapiMessageConverted.getSubject());
boolean subjectFound = false;
//Subject is also available as MapiPropertyDto:
for (MapiPropertyDto property : mapiMessageConverted.getProperties()) {
    if (!property.getDescriptor().getDiscriminator().equals("MapiKnownPropertyDescriptor"))
        continue;
    //There are different Property descriptors supported.
    //Some properties are known to the service:
    MapiKnownPropertyDescriptor knownPropertyDescriptor =
        (MapiKnownPropertyDescriptor) property.getDescriptor();
    //We know, that subject is stored in known property with name TagSubject:
    if (!knownPropertyDescriptor.getName().equals("TagSubject"))
        continue;
    //TagSubject is string property:
    MapiStringPropertyDto mapiStringPropertyDto = (MapiStringPropertyDto) property;
    assert mapiStringPropertyDto.getValue().equals(mapiMessage.getSubject());
    subjectFound = true;
}
assert subjectFound;
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
eml_file = api.mapi.message.as_file(
    models.MapiMessageAsFileRequest('Eml', mapi_message))
with open(eml_file, 'r') as f:
    file_data = f.read()
    assert mapi_message.subject in file_data
mapi_message_converted = api.mapi.message.from_file(
    models.MapiMessageFromFileRequest('Eml', eml_file))
assert mapi_message.subject == mapi_message_converted.subject
# Subject is also available as MapiPropertyDto:
# There are different Property descriptors supported.
# Some properties are known to the service and have MapiKnownPropertyDescriptor
known_properties = [x for x in mapi_message_converted.properties
                    if x.descriptor.discriminator == 'MapiKnownPropertyDescriptor']
# So we can find subject property by known property name:
subject_property = next(x for x in known_properties if x.descriptor.name == 'TagSubject')
assert mapi_message.subject == subject_property.value
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
eml_file = api.mapi.message.as_file(
  MapiMessageAsFileRequest.new(format: 'Eml', value: mapi_message))
eml_content = IO.read(eml_file)
expect(eml_content).to include mapi_message.subject
mapi_message_converted = api.mapi.message.from_file(
  MapiMessageFromFileRequest.new(format: 'Eml', file: eml_file))
expect(mapi_message.subject).to eq mapi_message_converted.subject
# Subject is also available as MapiPropertyDto:
# There are different Property descriptors supported.
# Some properties are known to the service and have MapiKnownPropertyDescriptor
# So we can find subject property by known property name:
subject_property = mapi_message_converted
                   .properties
                   .filter { |i| i.descriptor.discriminator == 'MapiKnownPropertyDescriptor' }
                   .find { |i| i.descriptor.name == 'TagSubject' }
expect(mapi_message.subject).to eq subject_property.value
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const emlFile = await api.mapi.message.asFile(
    new MapiMessageAsFileRequest('Eml', mapiMessageDto));
const emlString = emlFile.toString();
expect(emlString).to.contain(mapiMessageDto.subject);
const mapiMessageDtoConverted = await api.mapi.message.fromFile(
    new MapiMessageFromFileRequest('Eml', emlFile));
expect(mapiMessageDto.subject).to.be.eq(mapiMessageDtoConverted.subject);
//Subject is also available as MapiPropertyDto:
const subjectProperty = mapiMessageDtoConverted.properties
    //There are different Property descriptors supported.
    //Some properties are known to the service:
    .filter(i => i.descriptor.discriminator == 'MapiKnownPropertyDescriptor')
    //So we can find them by name:
    .find(i => (i.descriptor as MapiKnownPropertyDescriptor).name == 'TagSubject');
//Subject is a string, so it is stored in MapiStringPropertyDto:
const subjectString = (subjectProperty as MapiStringPropertyDto).value;
expect(mapiMessageDto.subject).to.be.eq(subjectString);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$emlFile = $api->mapi()->message()->asFile(new MapiMessageAsFileRequest(
    "Eml",
    $mapiMessage
));
$fileContent = $emlFile->fread($emlFile->getSize());
$this->assertRegExp("/" . $mapiMessage->getSubject() . "/", $fileContent);

$mapiMessageConverted = $api->mapi()->message()->fromFile(new MapiMessageFromFileRequest("Eml", $emlFile));
$this->assertEquals($mapiMessage->getSubject(), $mapiMessageConverted->getSubject());
//Subject is also available as MapiPropertyDto:
//There are different Property descriptors supported.
//Some properties are known to the service:
$knownPropertiesArray =
    array_filter($mapiMessageConverted->getProperties(), function ($var) {
        return $var->getDescriptor()->getDiscriminator() == "MapiKnownPropertyDescriptor";
    });
//We know, that subject is stored in known property with name TagSubject:
$subjectProperty = array_values(
    array_filter($knownPropertiesArray, function ($var) {
        /** @noinspection PhpPossiblePolymorphicInvocationInspection */
        return $var->getDescriptor()->getName() == 'TagSubject';
    })
)[0];
$this->assertEquals($mapiMessage->getSubject(), $subjectProperty->getValue());
```

{{< /tab >}}

{{< /tabs >}}
#### **MapiMessageDto and Cloud Storage**

{{< tabs tabTotal="6" tabID="24" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var storageName = "First Storage";
var folder = "a/folder/on/a/storage";
var fileName = "fileName.msg";

// Save as a file on storage:
await api.Mapi.Message.SaveAsync(new MapiMessageSaveRequest(
    new StorageFileLocation(storageName, folder, fileName), mapiMessage, "Msg"));

// Get back from storage:
var mapiMessageFromStorage =
    await api.Mapi.Message.GetAsync(
        new MapiMessageGetRequest("Msg", fileName, folder, storageName));

// Compare
Assert.AreEqual(mapiMessage.Subject, mapiMessageFromStorage.Subject);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String storage = "First Storage";
String folder = "a/folder/on/a/storage";
String fileName = "fileName.msg";

// Save as a file on storage:
api.mapi().message().save(
    new MapiMessageSaveRequest(new StorageFileLocation(storage, folder, fileName),
        mapiMessage, "Msg"));

// Get back from storage:
MapiMessageDto mapiMessageFromStorage =
    api.mapi().message().get(new MapiMessageGetRequest("Msg", fileName, folder, storage));

// Compare
assert mapiMessage.getSubject().equals(mapiMessageFromStorage.getSubject());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
storage = "First Storage"
folder = "a/folder/on/a/storage"
file_name = "fileName.msg"

# Save as a file on storage:
api.mapi.message.save(models.MapiMessageSaveRequest(
    models.StorageFileLocation(storage, folder, file_name),
    mapi_message, 'Msg'))

# Get back from storage:
mapi_message_from_storage = api.mapi.message.get(
    models.MapiMessageGetRequest('Msg', file_name, folder, storage))

# Compare
assert mapi_message.subject == mapi_message_from_storage.subject
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
storage = 'First Storage'
folder = 'a/folder/on/a/storage'
file_name = 'fileName.msg'

# Save as a file on storage:
api.mapi.message.save(
  MapiMessageSaveRequest.new(
    storage_file: StorageFileLocation.new(
      storage: storage,
      folder_path: folder,
      file_name: file_name),
    value: mapi_message,
    format: 'Msg'))

# Get back from storage:
mapi_message_from_storage = api.mapi.message.get(
  MapiMessageGetRequest.new(
    format: 'Msg',
    file_name: file_name,
    folder: folder,
    storage: storage))

# Compare
expect(mapi_message.subject).to eq mapi_message_from_storage.subject
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const storage = "First Storage";
const folder = "a/folder/on/a/storage";
const fileName = "fileName.msg";

// Save as a file on storage:
await api.mapi.message.save(
    new MapiMessageSaveRequest(
        new StorageFileLocation(storage, folder, fileName),
        mapiMessageDto, 'Msg'));

// Get back from storage:
const mapiMessageFromStorage = await api.mapi.message.get(
    new MapiMessageGetRequest('Msg', fileName, folder, storage));

// Compare
expect(mapiMessageDto.subject).to.be.eq(mapiMessageFromStorage.subject);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$storage = "First Storage";
$folder = "a/folder/on/a/storage";
$fileName = "fileName.msg";

// Save as a file on storage:
$api->mapi()->message()->save(new MapiMessageSaveRequest(
    new StorageFileLocation($storage, $folder, $fileName),
    $mapiMessage,
    "Msg"
));

// Get back from storage:
$mapiMessageFromStorage = $api->mapi()->message()->get(new MapiMessageGetRequest(
    "Msg",
    $fileName,
    $folder,
    $storage
));

// Compare
$this->assertEquals($mapiMessage->getSubject(), $mapiMessageFromStorage->getSubject());
```

{{< /tab >}}

{{< /tabs >}}
### **MapiContactDto methods**
#### **Convert ContactDto to MapiContactDto**

{{< tabs tabTotal="6" tabID="31" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
const string surname = "Thomas";
ContactDto contact = new ContactDto
{
    Gender = "Male",
    Surname = surname,
    GivenName = "Alex",
    EmailAddresses = new List<EmailAddress>
    {
        new EmailAddress
        {
            Category = new EnumWithCustomOfEmailAddressCategory("Work", null),
            Address = "alex.thomas@work.com",
            Preferred = true,
            DisplayName = "Alex Thomas"
        }
    },
    PhoneNumbers = new List<PhoneNumber>
    {
        new PhoneNumber
        {
            Category = new EnumWithCustomOfPhoneNumberCategory("Work", null),
            Number = "+49211424721",
            Preferred = true
        }
    }
};

var mapiContact = await api.Contact.AsMapiAsync(
    contact);
Assert.AreEqual(contact.Surname, mapiContact.NameInfo.Surname);

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String surname = "Thomas";
ContactDto contactDto = new ContactDto()
    .gender("Male")
    .surname(surname)
    .givenName("Alex")
    .addEmailAddressesItem(new EmailAddress(
        new EnumWithCustomOfEmailAddressCategory("Work", null),
        "Alex Thomas", true, null, "alex.thomas@work.com", null))
    .addPhoneNumbersItem(new PhoneNumber(
        new EnumWithCustomOfPhoneNumberCategory("Work", null),
        "+49211424721", true));

MapiContactDto mapiContactDto = api.contact().asMapi(contactDto);
assert contactDto.getSurname().equals(
    mapiContactDto.getNameInfo().getSurname());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
contact = models.ContactDto(
    gender='Male',
    surname='Thomas',
    given_name='Alex',
    email_addresses=[
        models.EmailAddress(
            models.EnumWithCustomOfEmailAddressCategory('Work'),
            'Alex Thomas', True, address='alex.thomas@work.com')],
    phone_numbers=[
        models.PhoneNumber(
            models.EnumWithCustomOfPhoneNumberCategory('Work'),
            '+49211424721', True)])
mapi_contact = api.contact.as_mapi(contact)
assert contact.surname == mapi_contact.name_info.surname
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
contact = ContactDto.new(
  surname: 'Cane',
  given_name: 'John',
  gender: 'Male',
  email_addresses: [EmailAddress.new(address: 'address@aspose.com')],
  phone_numbers: [PhoneNumber.new(number: '+4734534643')])

mapi_contact = api.contact.as_mapi(contact)
expect(contact.surname).to eq mapi_contact.name_info.surname
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const contactDto = new ContactDto();
contactDto.surname = surname;
contactDto.givenName = 'John';
contactDto.gender = 'Male';
const emailAddress = new EmailAddress();
emailAddress.address = 'address@aspose.com'
contactDto.emailAddresses = [emailAddress];
contactDto.phoneNumbers = [new PhoneNumber(undefined, '+47234325344')];

const mapiContactDto = await api.contact.asMapi(contactDto);
expect(contactDto.surname).to.be.eq(mapiContactDto.nameInfo.surname);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$contactDto = (new ContactDto())
    ->setSurname('Cane')
    ->setGivenName('John')
    ->setGender('Male')
    ->setEmailAddresses(array(
        (new EmailAddress())->setAddress('address@aspose.com')))
    ->setPhoneNumbers(array(
        (new PhoneNumber())->setNumber('+47235456456')));

$mapiContact = $api->contact()->asMapi($contactDto);
$this->assertEquals(
    $contactDto->getSurname(),
    $mapiContact->getNameInfo()->getSurname());
```

{{< /tab >}}

{{< /tabs >}}
#### **Convert MapiContactDto to ContactDto**

{{< tabs tabTotal="6" tabID="38" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
MapiContactDto mapiContact = new MapiContactDto
{
    ElectronicAddresses = new MapiContactElectronicAddressPropertySetDto
    {
        DefaultEmailAddress = new MapiContactElectronicAddressDto
            {EmailAddress = "email@aspose.com"}
    },
    NameInfo = new MapiContactNamePropertySetDto {GivenName = "Alex", Surname = "Thomas"},
    PersonalInfo = new MapiContactPersonalInfoPropertySetDto
        {BusinessHomePage = "www.aspose.com"},
    ProfessionalInfo = new MapiContactProfessionalPropertySetDto
        {Profession = "GENERAL DIRECTOR"},
    Telephones = new MapiContactTelephonePropertySetDto
        {PrimaryTelephoneNumber = "+49 211 4247 21"}
};

var contactDto = await api.Mapi.Contact.AsContactDtoAsync(mapiContact);
Assert.AreEqual(mapiContact.NameInfo.GivenName, contactDto.GivenName);
Assert.AreEqual(mapiContact.NameInfo.Surname, contactDto.Surname);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiContactDto mapiContact = new MapiContactDto()
    .electronicAddresses(new MapiContactElectronicAddressPropertySetDto()
        .defaultEmailAddress(new MapiContactElectronicAddressDto()
            .emailAddress("email@aspose.com")))
    .nameInfo(new MapiContactNamePropertySetDto()
        .givenName("Alex")
        .surname("Thomas"))
    .personalInfo(new MapiContactPersonalInfoPropertySetDto()
        .businessHomePage("www.aspose.com"))
    .professionalInfo(new MapiContactProfessionalPropertySetDto()
        .profession("GENERAL DIRECTOR"))
    .telephones(new MapiContactTelephonePropertySetDto()
        .primaryTelephoneNumber("+49 211 4247 21"));

ContactDto contactDto = api.mapi().contact().asContactDto(mapiContact);
assert mapiContact.getNameInfo().getGivenName().equals(contactDto.getGivenName());
assert mapiContact.getNameInfo().getSurname().equals(contactDto.getSurname());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
mapi_contact = models.MapiContactDto(
    electronic_addresses=models.MapiContactElectronicAddressPropertySetDto(
        default_email_address=models.MapiContactElectronicAddressDto(
            email_address='email@aspose.com')),
    name_info=models.MapiContactNamePropertySetDto(
        given_name='Alex',
        surname='Thomas'),
    personal_info=models.MapiContactPersonalInfoPropertySetDto(
        business_home_page='www.aspose.com'),
    professional_info=models.MapiContactProfessionalPropertySetDto(
        profession='GENERAL DIRECTOR'),
    telephones=models.MapiContactTelephonePropertySetDto(
        primary_telephone_number='+49 211 4247 21'))

contact = api.mapi.contact.as_contact_dto(mapi_contact)
assert mapi_contact.name_info.given_name == contact.given_name
assert mapi_contact.name_info.surname == contact.surname
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
mapi_contact = MapiContactDto.new(
  electronic_addresses: MapiContactElectronicAddressPropertySetDto.new(
    default_email_address: MapiContactElectronicAddressDto.new(
      email_address: 'email@aspose.com')),
  name_info: MapiContactNamePropertySetDto.new(
    given_name: 'Alex', surname: 'Thomas'),
  personal_info: MapiContactPersonalInfoPropertySetDto.new(
    business_home_page: 'www.aspose.com'),
  professional_info: MapiContactProfessionalPropertySetDto.new(
    profession: 'GENERAL DIRECTOR'),
  telephones: MapiContactTelephonePropertySetDto.new(
    primary_telephone_number: '+49 211 4247 21'))

contact = api.mapi.contact.as_contact_dto(mapi_contact)
expect(mapi_contact.name_info.given_name).to eq contact.given_name
expect(mapi_contact.name_info.surname).to eq contact.surname
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const mapiContactDto = new MapiContactDto();
mapiContactDto.electronicAddresses = new MapiContactElectronicAddressPropertySetDto();
mapiContactDto.electronicAddresses.defaultEmailAddress = new MapiContactElectronicAddressDto();
mapiContactDto.electronicAddresses.defaultEmailAddress.emailAddress = "email@aspose.com";
mapiContactDto.nameInfo = new MapiContactNamePropertySetDto();
mapiContactDto.nameInfo.givenName = "Alex";
mapiContactDto.nameInfo.surname = "Thomas";
mapiContactDto.personalInfo = new MapiContactPersonalInfoPropertySetDto();
mapiContactDto.personalInfo.businessHomePage = "www.aspose.com";
mapiContactDto.professionalInfo = new MapiContactProfessionalPropertySetDto();
mapiContactDto.professionalInfo.profession = "GENERAL DIRECTOR";
mapiContactDto.telephones = new MapiContactTelephonePropertySetDto();
mapiContactDto.telephones.primaryTelephoneNumber = "+49 211 4247 21";

const contactDto = await api.mapi.contact.asContactDto(mapiContactDto);
expect(mapiContactDto.nameInfo.givenName).to.be.eq(contactDto.givenName);
expect(mapiContactDto.nameInfo.surname).to.be.eq(contactDto.surname);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapiContact = (new MapiContactDto())
    ->setElectronicAddresses((new MapiContactElectronicAddressPropertySetDto())
        ->setDefaultEmailAddress((new MapiContactElectronicAddressDto())
            ->setEmailAddress("email@aspose.com")))
    ->setNameInfo((new MapiContactNamePropertySetDto())
        ->setGivenName("Alex")
        ->setSurname("Thomas"))
    ->setPersonalInfo((new MapiContactPersonalInfoPropertySetDto())
        ->setBusinessHomePage("www.aspose.com"))
    ->setProfessionalInfo((new MapiContactProfessionalPropertySetDto())
        ->setProfession("GENERAL DIRECTOR"))
    ->setTelephones((new MapiContactTelephonePropertySetDto())
        ->setPrimaryTelephoneNumber("+49 211 4247 21"));

$contactDto = $api->mapi()->contact()->asContactDto($mapiContact);
$this->assertEquals(
    $mapiContact->getNameInfo()->getGivenName(),
    $contactDto->getGivenName());
$this->assertEquals(
    $mapiContact->getNameInfo()->getSurname(),
    $contactDto->getSurname());
```

{{< /tab >}}

{{< /tabs >}}
#### **Convert MapiContactDto to a File and Back**

{{< tabs tabTotal="6" tabID="45" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var vcardStream =
    await api.Mapi.Contact.AsFileAsync(
        new MapiContactAsFileRequest("VCard", mapiContact));
using (var memoryStream = new MemoryStream())
{
    await vcardStream.CopyToAsync(memoryStream);
    var vcardString = Encoding.UTF8.GetString(memoryStream.ToArray());
    Assert.IsTrue(vcardString.Contains(mapiContact.NameInfo.GivenName));
}

vcardStream.Seek(0, SeekOrigin.Begin);
var mapiContactConverted =
    await api.Mapi.Contact.FromFileAsync(
        new MapiContactFromFileRequest("VCard", vcardStream));
Assert.AreEqual(mapiContact.NameInfo.Surname, mapiContactConverted.NameInfo.Surname);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] vcardBytes = api.mapi().contact().asFile(
    new MapiContactAsFileRequest("VCard", mapiContact));
String vcardString = new String(vcardBytes, "UTF-8");
assert vcardString.contains(mapiContact.getNameInfo().getGivenName());
MapiContactDto mapiContactConverted = api.mapi().contact().fromFile(
    new MapiContactFromFileRequest("VCard", vcardBytes));
assert mapiContact.getNameInfo().getSurname()
    .equals(mapiContactConverted.getNameInfo().getSurname());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
vcard_file = api.mapi.contact.as_file(
    models.MapiContactAsFileRequest('VCard', mapi_contact))
with open(vcard_file, 'r') as f:
    file_data = f.read()
    assert mapi_contact.name_info.given_name in file_data
mapi_contact_converted = api.mapi.contact.from_file(
    models.MapiContactFromFileRequest('VCard', vcard_file))
assert mapi_contact.name_info.surname == mapi_contact_converted.name_info.surname
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
vcard_file = api.mapi.contact.as_file(
  MapiContactAsFileRequest.new(
    format: 'VCard',
    value: mapi_contact))
vcard_content = IO.read(vcard_file)
expect(vcard_content)
  .to include mapi_contact.name_info.given_name
mapi_contact_converted = api.mapi.contact.from_file(
  MapiContactFromFileRequest.new(
    format: 'VCard',
    file: vcard_file))
expect(mapi_contact.name_info.surname).to eq mapi_contact_converted.name_info.surname
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const vcardFile = await api.mapi.contact.asFile(
    new MapiContactAsFileRequest('VCard', mapiContactDto));
const vcardString = vcardFile.toString();
expect(vcardString).to.contain(mapiContactDto.nameInfo.givenName);
const mapiContactDtoConverted = await api.mapi.contact.fromFile(
    new MapiContactFromFileRequest('VCard', vcardFile));
expect(mapiContactDto.nameInfo.surname)
    .to.be.eq(mapiContactDtoConverted.nameInfo.surname);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$vcardFile = $api->mapi()->contact()->asFile(
    new MapiContactAsFileRequest("VCard", $mapiContact));
$fileContent = $vcardFile->fread($vcardFile->getSize());
$this->assertRegExp(
    "/" . $mapiContact->getNameInfo()->getGivenName() . "/",
    $fileContent);
$mapiContactConverted = $api->mapi()->contact()->fromFile(
    new MapiContactFromFileRequest("VCard", $vcardFile));
$this->assertEquals(
    $mapiContact->getNameInfo()->getSurname(),
    $mapiContactConverted->getNameInfo()->getSurname());
```

{{< /tab >}}

{{< /tabs >}}
#### **MapiContactDto and Cloud Storage**

{{< tabs tabTotal="6" tabID="52" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var storageName = "First Storage";
var folder = "a/folder/on/a/storage";
var fileName = "fileName.msg";

await api.Mapi.Contact.SaveAsync(new MapiContactSaveRequest(
    new StorageFileLocation(storageName, folder, fileName),
    mapiContact, "Msg"));
var mapiContactFromStorage = await api.Mapi.Contact.GetAsync(
    new MapiContactGetRequest(
        "Msg", fileName, folder, storageName));
Assert.AreEqual(
    mapiContact.NameInfo.Surname,
    mapiContactFromStorage.NameInfo.Surname);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String storage = "First Storage";
String folder = "a/folder/on/a/storage";
String fileName = "fileName.msg";

api.mapi().contact().save(
    new MapiContactSaveRequest(
        new StorageFileLocation(storage, folder, fileName),
        mapiContact, "Msg"));
MapiContactDto mapiContactFromStorage = api.mapi().contact().get(
    new MapiContactGetRequest("Msg", fileName, folder, storage));
assert mapiContact.getNameInfo().getSurname()
    .equals(mapiContactFromStorage.getNameInfo().getSurname());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
storage = 'First Storage'
folder = 'a/folder/on/a/storage'
file_name = 'fileName.msg'

api.mapi.contact.save(models.MapiContactSaveRequest(
    models.StorageFileLocation(storage, folder, file_name),
    mapi_contact, 'Msg'))
mapi_contact_from_storage = api.mapi.contact.get(
    models.MapiContactGetRequest('Msg', file_name, folder, storage))
assert mapi_contact.name_info.surname == mapi_contact_from_storage.name_info.surname
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
storage = 'First Storage'
folder = 'a/folder/on/a/storage'
file_name = 'fileName.msg'

api.mapi.contact.save(
  MapiContactSaveRequest.new(
    storage_file: StorageFileLocation.new(
      storage: storage,
      folder_path: folder,
      file_name: file_name),
    value: mapi_contact,
    format: 'Msg'))
mapi_contact_from_storage = api.mapi.contact.get(
  MapiContactGetRequest.new(
    format: 'Msg',
    file_name: file_name,
    folder: folder,
    storage: storage))
expect(mapi_contact.name_info.surname)
  .to eq mapi_contact_from_storage.name_info.surname
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const storage = "First Storage";
const folder = "a/folder/on/a/storage";
const fileName = "fileName.msg";

await api.mapi.contact.save(
    new MapiContactSaveRequest(
        new StorageFileLocation(storage, folder, fileName),
        mapiContactDto, 'Msg'));
const mapiContactFromStorage = await api.mapi.contact.get(
    new MapiContactGetRequest('Msg', fileName, folder, storage));
expect(mapiContactDto.nameInfo.surname)
    .to.be.eq(mapiContactFromStorage.nameInfo.surname);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$storage = "First Storage";
$folder = "a/folder/on/a/storage";
$fileName = "fileName.msg";

$api->mapi()->contact()->save(new MapiContactSaveRequest(
    new StorageFileLocation($storage, $folder, $fileName),
    $mapiContact,
    "Msg"
));
$mapiContactFromStorage = $api->mapi()->contact()->get(new MapiContactGetRequest(
    "Msg",
    $fileName,
    $folder,
    $storage
));
$this->assertEquals($mapiContact->getNameInfo()->getSurname(), $mapiContactFromStorage
    ->getNameInfo()->getSurname());
```

{{< /tab >}}

{{< /tabs >}}
### **MapiCalendarDto methods**
#### **Convert CalendarDto to MapiCalendarDto**

{{< tabs tabTotal="6" tabID="59" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
const string location = "Some location";
CalendarDto calendar = new CalendarDto
{
    Location = location, Description = "Some description", Summary = "Some summary",
    StartDate = DateTime.UtcNow.AddDays(1).AddHours(12),
    EndDate = DateTime.UtcNow.AddDays(1).AddHours(13),
    Attendees = new List<MailAddress>
    {
        new MailAddress("Attendee Name", "attendee@am.ru", "Accepted", null)
    },
    Organizer = new MailAddress("Organizer Name", "cloud.em@yandex.ru", null, null),
    Recurrence = new DailyRecurrencePatternDto
    {
        Occurs = 10,
        WeekStart = "Monday"
    }
};
var mapiCalendar = await api.Calendar.AsMapiAsync(calendar);
Assert.AreEqual(calendar.Location, mapiCalendar.Location);
Assert.AreEqual(nameof(MapiCalendarDailyRecurrencePatternDto),
    mapiCalendar.Recurrence.RecurrencePattern.Discriminator);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String location = "Some location";
CalendarDto calendarDto = new CalendarDto()
    .location(location)
    .summary("Some summary")
    .description("Some description")
    .startDate(Calendar.getInstance().getTime())
    .endDate(Calendar.getInstance().getTime())
    .organizer(new MailAddress().address("organizer@aspose.com"))
    .attendees(Collections.singletonList(new MailAddress().address("attendee@aspose.com")))
    .recurrence(new DailyRecurrencePatternDto()
        .occurs(10)
        .weekStart("Monday"));

MapiCalendarDto mapiCalendarDto = api.calendar().asMapi(calendarDto);
assert calendarDto.getLocation().equals(mapiCalendarDto.getLocation());
assert "MapiCalendarDailyRecurrencePatternDto"
    .equals(mapiCalendarDto.getRecurrence().getRecurrencePattern().getDiscriminator());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
calendar = models.CalendarDto()
calendar.attendees = [models.MailAddress(
    'Attendee Name', 'attendee@aspose.com', 'Accepted')]
calendar.description = 'Some description'
calendar.summary = 'Some summary'
calendar.organizer = models.MailAddress(
    'Organizer Name', 'organizer@aspose.com', 'Accepted')
calendar.start_date = datetime.today() + timedelta(days=1)
calendar.end_date = calendar.start_date + timedelta(hours=1)
calendar.location = 'Some location'
calendar.recurrence = models.DailyRecurrencePatternDto(None, 10, None, 'Monday')

mapi_calendar = api.calendar.as_mapi(calendar)
assert calendar.location == mapi_calendar.location
assert 'MapiCalendarDailyRecurrencePatternDto'\
       == mapi_calendar.recurrence.recurrence_pattern.discriminator
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
calendar = CalendarDto.new(
  location: 'Some location',
  summary: 'Some summary',
  description: 'Some description',
  start_date: DateTime.now,
  end_date: DateTime.now,
  organizer: MailAddress.new(address: 'organizer@aspose.com'),
  attendees: [MailAddress.new(address: 'attendee@aspose.com')],
  recurrence: DailyRecurrencePatternDto.new(occurs: 10, week_start: 'Monday'))

mapi_calendar = api.calendar.as_mapi(calendar)
expect(calendar.location).to eq mapi_calendar.location
expect('MapiCalendarDailyRecurrencePatternDto')
  .to eq mapi_calendar.recurrence.recurrence_pattern.discriminator
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const calendar = new CalendarDto();
calendar.attendees = [
    new MailAddress('Attendee Name', 'attendee@am.ru', 'Accepted')
];
calendar.description = 'Some description';
calendar.summary = 'Some summary';
calendar.organizer = new MailAddress('Organizer Name', 'organizer@am.ru');
calendar.startDate = new Date();
calendar.endDate = new Date();
calendar.location = 'Some location';
calendar.recurrence = new DailyRecurrencePatternDto(
    undefined, 10, undefined, "Monday");

const mapiCalendarDto = await api.calendar.asMapi(calendarDto);
expect(calendarDto.location).to.be.eq(mapiCalendarDto.location);
expect('MapiCalendarDailyRecurrencePatternDto').to.be.eq(
    mapiCalendarDto.recurrence.recurrencePattern.discriminator);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$calendar = (new CalendarDto())
    ->setAttendees(array(new MailAddress(
        "Attendee Name",
        "attendee@aspose.com",
        "Accepted"
    )))
    ->setDescription("Some description")
    ->setSummary("Some summary")
    ->setOrganizer(new MailAddress("Organizer Name", "organizer@aspose.com", "Accepted"))
    ->setStartDate(new DateTime())
    ->setEndDate((new DateTime())->add(new DateInterval("PT1H")))
    ->setLocation("Some location")
    ->setRecurrence((new DailyRecurrencePatternDto())
        ->setOccurs(10)
        ->setWeekStart("Monday"));

$mapiCalendar = $api->calendar()->asMapi($calendar);
$this->assertEquals($calendar->getLocation(), $mapiCalendar->getLocation());
$this->assertEquals(
    'MapiCalendarDailyRecurrencePatternDto',
    $mapiCalendar->getRecurrence()->getRecurrencePattern()->getDiscriminator()
```

{{< /tab >}}

{{< /tabs >}}
#### **Convert MapiCalendarDto to CalendarDto**
**How to Convert MapiCalendarDto to CalendarDto:**

{{< tabs tabTotal="6" tabID="66" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
MapiCalendarDto mapiCalendar = new MapiCalendarDto
{
    BusyStatus = "Tentative", EndDate = DateTime.Today.AddDays(1),
    Location = "Some location", StartDate = DateTime.Today, Body = "Some description",
    BodyType = "PlainText", Subject = "Some summary",
    Attendees = new MapiCalendarAttendeesDto
    {
        AppointmentRecipients = new List<MapiRecipientDto>
        {
            new MapiRecipientDto
            {
                AddressType = "SMTP", DisplayName = "Organizer Name",
                EmailAddress = "organizer@aspose.com", RecipientType = "MapiTo"
            },
            new MapiRecipientDto
            {
                AddressType = "SMTP", DisplayName = "Attendee Name",
                EmailAddress = "attendee@aspose.com", RecipientType = "MapiTo"
            }
        }
    },
    ClientIntent = new List<string> {"Manager"},
    Recurrence = new MapiCalendarEventRecurrenceDto
    {
        RecurrencePattern = new MapiCalendarDailyRecurrencePatternDto
            {OccurrenceCount = 10, WeekStartDay = "Monday"}
    },
    Organizer = new MapiElectronicAddressDto {EmailAddress = "organizer@aspose.com"},
};

var calendarDto = await api.Mapi.Calendar.AsCalendarDtoAsync(mapiCalendar);
Assert.AreEqual(mapiCalendar.Subject, calendarDto.Summary);
Assert.AreEqual(mapiCalendar.Location, calendarDto.Location);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiCalendarDto mapiCalendar = (MapiCalendarDto) new MapiCalendarDto()
    .attendees(new MapiCalendarAttendeesDto()
        .addAppointmentRecipientsItem(
            new MapiRecipientDto()
                .addressType("SMTP")
                .displayName("Organizer Name")
                .emailAddress("organizer@aspose.com")
                .recipientType("MapiTo"))
        .addAppointmentRecipientsItem(
            new MapiRecipientDto()
                .addressType("SMTP")
                .displayName("Attendee Name")
                .emailAddress("attendee@aspose.com")
                .recipientType("MapiTo")))
    .addClientIntentItem("Manager")
    .recurrence(new MapiCalendarEventRecurrenceDto()
        .recurrencePattern(new MapiCalendarDailyRecurrencePatternDto()
            .occurrenceCount((long) 10)
            .weekStartDay("Monday")))
    .organizer(new MapiElectronicAddressDto()
        .emailAddress("organizer@aspose.com"))
    .busyStatus("Tentative")
    .startDate(Calendar.getInstance().getTime())
    .endDate(Calendar.getInstance().getTime())
    .location("Some location")
    .body("Some description")
    .bodyType("PlainText")
    .subject("Some summary");

CalendarDto calendarDto = api.mapi().calendar().asCalendarDto(mapiCalendar);
assert mapiCalendar.getSubject().equals(calendarDto.getSummary());
assert mapiCalendar.getLocation().equals(calendarDto.getLocation());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
mapi_calendar = models.MapiCalendarDto(
    attendees=models.MapiCalendarAttendeesDto([
        models.MapiRecipientDto(
            address_type='SMTP',
            display_name='Attendee Name',
            email_address='attendee@aspose.com',
            recipient_type='MapiTo')]),
    client_intent=['Manager'],
    recurrence=models.MapiCalendarEventRecurrenceDto(
        recurrence_pattern=models.MapiCalendarDailyRecurrencePatternDto(
            occurrence_count=10,
            week_start_day='Monday')),
    organizer=models.MapiElectronicAddressDto(None, 'organizer@aspose.com'),
    busy_status='Tentative',
    start_date=datetime.today(),
    end_date=datetime.today(),
    location='Some location',
    body='Some description',
    body_type='PlainText',
    subject='Some summary')

calendar = api.mapi.calendar.as_calendar_dto(mapi_calendar)
assert mapi_calendar.subject == calendar.summary
assert mapi_calendar.location == calendar.location
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
mapi_calendar = MapiCalendarDto.new(
  attendees: MapiCalendarAttendeesDto.new(appointment_recipients: [MapiRecipientDto.new(
    address_type: 'SMTP',
    display_name: 'Attendee Name',
    email_address: 'attendee@aspose.com',
    recipient_type: 'MapiTo')]),
  client_intent: ['Manager'],
  recurrence: MapiCalendarEventRecurrenceDto.new(
    recurrence_pattern: MapiCalendarDailyRecurrencePatternDto.new(
      occurrence_count: 10,
      week_start_day: 'Monday'
    )),
  organizer: MapiElectronicAddressDto.new(email_address: 'organizer@aspose.com'),
  busy_status: 'Tentative',
  start_date: DateTime.now,
  end_date: DateTime.now,
  location: 'Some location',
  body: 'Some description',
  body_type: 'PlainText',
  subject: 'Some summary')

calendar = api.mapi.calendar.as_calendar_dto(mapi_calendar)
expect(mapi_calendar.subject).to eq calendar.summary
expect(mapi_calendar.location).to eq calendar.location
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const mapiCalendarDto = new MapiCalendarDto();
const mapiRecipientDto = new MapiRecipientDto();
mapiRecipientDto.addressType = "SMTP";
mapiRecipientDto.displayName = "Attendee Name";
mapiRecipientDto.emailAddress = "attendee@aspose.com";
mapiRecipientDto.recipientType = "MapiTo";
mapiCalendarDto.attendees = new MapiCalendarAttendeesDto([mapiRecipientDto]);
mapiCalendarDto.clientIntent = ["Manager"];
const recurrence = new MapiCalendarEventRecurrenceDto();
const recurrencePatternDto = new MapiCalendarDailyRecurrencePatternDto();
recurrencePatternDto.occurrenceCount = 10;
recurrencePatternDto.weekStartDay = "Monday";
recurrence.recurrencePattern = recurrencePatternDto;
mapiCalendarDto.recurrence = recurrence;
mapiCalendarDto.organizer = new MapiElectronicAddressDto(undefined, "organizer@aspose.com");
mapiCalendarDto.busyStatus = "Tentative";
mapiCalendarDto.startDate = td.getDate(undefined, 1);
mapiCalendarDto.endDate = td.getDate(mapiCalendarDto.startDate, 1);
mapiCalendarDto.location = "Some location";
mapiCalendarDto.body = "Some description";
mapiCalendarDto.bodyType = "PlainText";
mapiCalendarDto.subject = "Some summary";

const calendarDto = await td.api().mapi.calendar.asCalendarDto(mapiCalendarDto);
expect(mapiCalendarDto.subject).to.be.eq(calendarDto.summary);
expect(mapiCalendarDto.location).to.be.eq(calendarDto.location);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapiCalendar = (new MapiCalendarDto())
    ->setAttendees((new MapiCalendarAttendeesDto())
        ->setAppointmentRecipients(array((new MapiRecipientDto())
            ->setAddressType("SMTP")
            ->setDisplayName("Organizer Name")
            ->setEmailAddress("organizer@aspose.com")
            ->setRecipientType("MapiTo")))
        ->setAppointmentRecipients(array((new MapiRecipientDto())
            ->setAddressType("SMTP")
            ->setDisplayName("Attendee Name")
            ->setEmailAddress("attendee@aspose.com")
            ->setRecipientType("MapiTo"))))
    ->setClientIntent(array("Manager"))
    ->setRecurrence((new MapiCalendarEventRecurrenceDto())
        ->setRecurrencePattern((new MapiCalendarDailyRecurrencePatternDto())
            ->setOccurrenceCount(10)
            ->setWeekStartDay("Monday")))
    ->setOrganizer((new MapiElectronicAddressDto())
        ->setEmailAddress("organizer@aspose.com"))
    ->setBusyStatus("Tentative")
    ->setStartDate(new DateTime())
    ->setEndDate(new DateTime())
    ->setLocation("Some location")
    ->setBody("Some description")
    ->setBodyType("PlainText")
    ->setSubject("Some summary");

$calendarDto = $api->mapi()->calendar()->asCalendarDto($mapiCalendar);
$this->assertEquals($mapiCalendar->getSubject(), $calendarDto->getSummary());
$this->assertEquals($mapiCalendar->getLocation(), $calendarDto->getLocation());
```

{{< /tab >}}

{{< /tabs >}}
#### **Convert MapiCalendarDto to a File and Back**

{{< tabs tabTotal="6" tabID="73" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var icsStream = await api.Mapi.Calendar.AsFileAsync(
        new MapiCalendarAsFileRequest("Ics", mapiCalendar));
using (var memoryStream = new MemoryStream())
{
    await icsStream.CopyToAsync(memoryStream);
    var icsString = Encoding.UTF8.GetString(memoryStream.ToArray());
    Assert.IsTrue(icsString.Contains(mapiCalendar.Location));
}

icsStream.Seek(0, SeekOrigin.Begin);
var mapiCalendarConverted = await api.Mapi.Calendar.FromFileAsync(
    new MapiCalendarFromFileRequest(icsStream));
Assert.AreEqual(mapiCalendar.Location, mapiCalendarConverted.Location);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] ics = api.mapi().calendar().asFile(
    new MapiCalendarAsFileRequest("Ics", mapiCalendar));
String calendarContent = new String(ics, "UTF-8");
assert calendarContent.contains(mapiCalendar.getLocation());

MapiCalendarDto mapiCalendarConverted =
    api.mapi().calendar().fromFile(
        new MapiCalendarFromFileRequest(ics));
assert mapiCalendar.getLocation()
    .equals(mapiCalendarConverted.getLocation());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
ics_file = api.mapi.calendar.as_file(
    models.MapiCalendarAsFileRequest('Ics', mapi_calendar))
with open(ics_file, 'r') as f:
    file_data = f.read()
    assert mapi_calendar.location in file_data
mapi_calendar_converted = api.mapi.calendar.from_file(
    models.MapiCalendarFromFileRequest(ics_file))
assert mapi_calendar.location == mapi_calendar_converted.location
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
ics_file = api.mapi.calendar.as_file(
  MapiCalendarAsFileRequest.new(format: 'Ics', value: mapi_calendar))
ics_content = IO.read(ics_file)
expect(ics_content).to include mapi_calendar.location
mapi_calendar_converted = api.mapi.calendar.from_file(
  MapiCalendarFromFileRequest.new(file: ics_file))
expect(mapi_calendar.location).to eq mapi_calendar_converted.location
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const icsFile = await td.api().mapi.calendar.asFile(
    new MapiCalendarAsFileRequest('Ics', mapiCalendarDto));
const icsString = icsFile.toString();
expect(icsString).to.contain(mapiCalendarDto.location);
const mapiCalendarDtoConverted = await td.api().mapi.calendar.fromFile(
    new MapiCalendarFromFileRequest(icsFile));
expect(mapiCalendarDto.location).to.be.eq(mapiCalendarDtoConverted.location);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$ics = $api->mapi()->calendar()->asFile(
    new MapiCalendarAsFileRequest(
        "Ics",
        $mapiCalendar));
$fileContent = $ics->fread($ics->getSize());
$this->assertRegExp("/" . $mapiCalendar->getLocation() . "/", $fileContent);

$mapiCalendarConverted = $api->mapi()->calendar()->fromFile(
    new MapiCalendarFromFileRequest($ics));
$this->assertEquals($mapiCalendar->getLocation(), $mapiCalendarConverted->getLocation());
```

{{< /tab >}}

{{< /tabs >}}
#### **MapiCalendarDto and Cloud Storage**

{{< tabs tabTotal="6" tabID="80" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs

var storageName = "First Storage";
var folder = "a/folder/on/a/storage";
var fileName = "fileName.msg";

await api.Mapi.Calendar.SaveAsync(
    new MapiCalendarSaveRequest(
        new StorageFileLocation(storageName, folder, fileName),
        mapiCalendar, "Msg"));
var mapiCalendarFromStorage =
    await api.Mapi.Calendar.GetAsync(
        new MapiCalendarGetRequest(fileName, folder, storageName));
Assert.AreEqual(mapiCalendar.Location, mapiCalendarFromStorage.Location);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String storage = "First Storage";
String folder = "a/folder/on/a/storage";
String fileName = "fileName.msg";

api.mapi().calendar().save(
    new MapiCalendarSaveRequest(
        new StorageFileLocation(storage, folder, fileName),
        mapiCalendar, "Msg"));
MapiCalendarDto mapiCalendarFromStorage =
    api.mapi().calendar().get(
        new MapiCalendarGetRequest(fileName, folder, storage));
assert mapiCalendar.getLocation().equals(mapiCalendarFromStorage.getLocation());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
storage = "First Storage"
folder = "a/folder/on/a/storage"
file_name = "fileName.msg"

api.mapi.calendar.save(models.MapiCalendarSaveRequest(
    models.StorageFileLocation(storage, folder, file_name),
    mapi_calendar, 'Msg'))
mapi_calendar_from_storage = api.mapi.calendar.get(
    models.MapiCalendarGetRequest(file_name, folder, storage))
assert mapi_calendar.location == mapi_calendar_from_storage.location
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
storage = "First Storage"
folder = "a/folder/on/a/storage"
file_name = "fileName.msg"

api.mapi.calendar.save(
  MapiCalendarSaveRequest.new(
    storage_file: StorageFileLocation.new(
      storage: storage,
      folder_path: folder,
      file_name: file_name),
    value: mapi_calendar,
    format: 'Msg'))
mapi_calendar_from_storage = api.mapi.calendar.get(
  MapiCalendarGetRequest.new(file_name: file_name, folder: folder, storage: storage))
expect(mapi_calendar.location).to eq mapi_calendar_from_storage.location
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const storage = "First Storage";
const folder = "a/folder/on/a/storage";
const fileName = "fileName.msg";

await api.mapi.calendar.save(
    new MapiCalendarSaveRequest(
        new StorageFileLocation(storage, folder, fileName),
        mapiCalendarDto, 'Msg'));
const mapiCalendarFromStorage = await api.mapi.calendar.get(
    new MapiCalendarGetRequest(fileName, folder, storage));
expect(mapiCalendarDto.location).to.be.eq(mapiCalendarFromStorage.location);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$storage = "First Storage";
$folder = "a/folder/on/a/storage";
$fileName = "fileName.msg";

$api->mapi()->calendar()->save(new MapiCalendarSaveRequest(
    new StorageFileLocation($storage, $folder, $fileName),
    $mapiCalendar,
    "Msg"
));
$mapiCalendarFromStorage = $api->mapi()->calendar()->get(new MapiCalendarGetRequest(
    $fileName,
    $folder,
    $storage
));
$this->assertEquals($mapiCalendar->getLocation(), $mapiCalendarFromStorage->getLocation());
```

{{< /tab >}}

{{< /tabs >}}
## **More Tutorials**
Take a look at other tutorials, you may find answers on your questions there:
