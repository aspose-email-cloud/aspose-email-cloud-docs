---
title: "Introduction to MAPI Message Files API"
type: docs
url: /introduction-to-mapi-message-files-api/
description: " Instructions on how to use MAPI message files API in Aspose.Email Cloud SDK. How to work with MAPI in Cloud SDK for .NET, Java, PHP, Python, Ruby, Node.js."
weight: 90
---

## **MAPI Message Files**
[Aspose.Email Cloud](https://products.aspose.cloud/email/family) supports files in Microsoft Outlook Email format ([MSG ](https://docs.fileformat.com/email/msg/)files).

First of all, the MSG file could be represented as a list of properties. See this JSON example:

MSG file properties list represented as a JSON array

{{< tabs tabTotal="1" tabID="6" tabName1="JS" >}}
{{< tab tabNum="1" >}}
```java
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
```
{{< /tab >}}
{{< /tabs >}}


These properties could contain different values. It could be integers, strings, bytes, multiple strings, and a lot of other data types. All properties are identified using property Descriptors. Aspose.Email Cloud supports different types of property descriptors:

- MapiPidTagPropertyDescriptor - A property, identified by a tag, which consists of a combination of data type and identifier.
- MapiPidLidPropertyDescriptor - A property, identified by a long id and a property set.
- MapiPidNamePropertyDescriptor - A property, identified by a name and a property set.
- MapiKnownPropertyDescriptor - This descriptor implies one of three previous descriptors. It is a property, that is known to Aspose.Email Cloud, so it can be fully identified by the property name. 
See all known properties [here](https://apireference.aspose.com/email/net/aspose.email.mapi/knownpropertylist/fields/index).

Aspose.Email Cloud provides 3 different models to represent the MSG file. These models contain a list of all properties and extra fields for easier file operation. For example, MapiMessageDto has a string field named Subject, which contains a subject for an email message. But this field is just a copy of a property with a [TagSubject ](https://apireference.aspose.com/email/net/aspose.email.mapi/knownpropertylist/fields/tagsubject)descriptor:

Part of MapiMessageDto JSON with subject

{{< tabs tabTotal="1" tabID="6" tabName1="JS" >}}
{{< tab tabNum="1" >}}
```java

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

{{< /tab >}}
{{< /tabs >}}

These 3 MAPI models are:

1. MapiMessageDto - represents an email message. Has properties to represent a message's subject, body, sender, recipients, etc.
1. MapiCalendarDto - represents an appointment or a meeting object. Provides properties for meeting start and end, location, recurrence, busy status, etc.
1. MapiContactDto - represents a contact. Provides properties for name, telephone, email addresses, etc.

All these models can be converted to the corresponding usual models and back:

- MapiMessageDto <-> EmailDto
- MapiCalendarDto <-> CalendarDto
- MapiContactDto <-> ContactDto

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

To see how to set up SDKs use the [SDK setup](/sdk-setup/) tutorial.

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
**How to Convert EmailDto to MapiMessageDto**

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="Typescript" tabName4="Python" tabName5="Ruby" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```java

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

    From = new MailAddress {Address = "from@aspose.com", DisplayName = "From Address"},

    To = new List<MailAddress>

        {new MailAddress {Address = "to@aspose.com", DisplayName = "To Address"}}

};

MapiMessageDto mapiMessage = await emailApi.ConvertEmailModelToMapiModelAsync(

    new ConvertEmailModelToMapiModelRequest(emailDto));

Assert.AreEqual(emailDto.Subject, mapiMessage.Subject);

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

EmailDto emailDto = new EmailDto()

    .from(new MailAddress().address("from@aspose.com"))

    .addToItem(new MailAddress().address("to@aspose.com"))

    .subject("Some subject")

    .body("Some body")

    .date(Calendar.getInstance().getTime());

MapiMessageDto mapiMessageDto = api.convertEmailModelToMapiModel(

    new ConvertEmailModelToMapiModelRequestData(emailDto));

assert emailDto.getSubject().equals(mapiMessageDto.getSubject());

```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java

let emailDto = new models.EmailDto();

emailDto.from = new models.MailAddress(undefined, 'from@aspose.com');

emailDto.to = [new models.MailAddress(undefined, 'to@aspose.com')];

emailDto.subject = 'Some subject';

emailDto.body = 'Some body';

emailDto.date = new Date();

const mapiMessageDto = await api.convertEmailModelToMapiModel(

    new requests.ConvertEmailModelToMapiModelRequest(emailDto));

expect(emailDto.subject).to.be.eq(mapiMessageDto.body.subject);

```

{{< /tab >}}

{{< tab tabNum="4" >}}

```java

email\_document = models.EmailDto()

email\_document.\_from = models.MailAddress(address='from@aspose.com')

email\_document.to = [models.MailAddress(address='to@aspose.com')]

email\_document.subject = 'Some subject'

email\_document.body = 'Some body'

email\_document.\_date = datetime.today()

mapi\_message = email.convert\_email\_model\_to\_mapi\_model(

    requests.ConvertEmailModelToMapiModelRequest(email\_document))

assert email\_document.subject == mapi\_message.subject

```

{{< /tab >}}

{{< tab tabNum="5" >}}

```java

email = EmailDto.new

email.from = MailAddress.new(nil, 'from@aspose.com')

email.to = [MailAddress.new(nil, 'to@aspose.com')]

email.subject = 'Some subject'

email.body = 'Some body'

email.date = DateTime.now

mapi\_message = @api.convert\_email\_model\_to\_mapi\_model(

    ConvertEmailModelToMapiModelRequestData.new(email))

expect(email.subject).to eq mapi\_message.subject

```

{{< /tab >}}

{{< tab tabNum="6" >}}

```java

$emailDto = (new EmailDto())

    ->setFrom(new MailAddress(null, 'from@aspose.com'))

    ->setTo(array(new MailAddress(null, 'to@aspose.com')))

    ->setSubject('Some subject')

    ->setBody('Some body')

    ->setDate(new DateTime());

$mapiMessage = $api->convertEmailModelToMapiModel(

    new ConvertEmailModelToMapiModelRequest($emailDto)

);

$this->assertEquals($emailDto->getSubject(), $mapiMessage->getSubject());

```

{{< /tab >}}

{{< /tabs >}}
#### **Convert MapiMessageDto to EmailDto**
**How to Convert MapiMessageDto to EmailDto:**

{{< tabs tabTotal="6" tabID="10" tabName1="C#" tabName2="Java" tabName3="Typescript" tabName4="Python" tabName5="Ruby" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```java

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

EmailDto emailDto =

    await emailApi.ConvertMapiMessageModelToEmailModelAsync(

        new ConvertMapiMessageModelToEmailModelRequest(

            mapiMessage));

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

EmailDto emailDto = api.convertMapiMessageModelToEmailModel(

    new ConvertMapiMessageModelToEmailModelRequestData(

        mapiMessage));

assert mapiMessage.getSubject().equals(emailDto.getSubject());

assert mapiMessage.getBody().equals(emailDto.getBody());

```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java

const mapiMessageDto = new models.MapiMessageDto();

mapiMessageDto.clientSubmitTime = td.getDate();

mapiMessageDto.senderAddressType = "SMTP";

mapiMessageDto.senderEmailAddress = "from@aspose.com";

mapiMessageDto.senderSmtpAddress = "from@aspose.com";

mapiMessageDto.messageFormat = "Ascii";

mapiMessageDto.senderName = "From Address";

mapiMessageDto.messageBody = "Some body";

mapiMessageDto.displayTo = "To Address";

mapiMessageDto.deliveryTime = td.getDate();

mapiMessageDto.normalizedSubject = "Some subject";

mapiMessageDto.flags = ["MsgFlagRead", "MsgFlagUnsent", "MsgFlagHasAttach"];

const recipientDto = new models.MapiRecipientDto();

recipientDto.addressType = "SMTP";

recipientDto.displayName = "To address";

recipientDto.emailAddress = "to@aspose.com";

recipientDto.recipientType = "MapiTo";

mapiMessageDto.recipients = [recipientDto];

const attachment = new models.MapiAttachmentDto();

attachment.dataBase64 = Buffer.from("Some file text").toString('base64');

attachment.name = "some-file.txt";

mapiMessageDto.attachments = [attachment];

mapiMessageDto.subjectPrefix = "Re: ";

mapiMessageDto.messageClass = "IPM.Note";

mapiMessageDto.body = "Some body";

mapiMessageDto.subject = "Re: Some subject";

mapiMessageDto.bodyType = "PlainText";

const emailDto = await api.convertMapiMessageModelToEmailModel(

    new requests.ConvertMapiMessageModelToEmailModelRequest(mapiMessageDto));

expect(mapiMessageDto.subject).to.be.eq(emailDto.body.subject);

expect(mapiMessageDto.body).to.be.eq(emailDto.body.body);

```

{{< /tab >}}

{{< tab tabNum="4" >}}

```java

mapi\_message = models.MapiMessageDto()

mapi\_message.sender\_address\_type = 'SMTP'

mapi\_message.sender\_email\_address = 'from@aspose.com'

mapi\_message.sender\_smtp\_address = 'from@aspose.com'

mapi\_message.sender\_name = 'From Address'

mapi\_message.message\_body = 'Some body'

mapi\_message.display\_to = 'To Address'

mapi\_message.delivery\_time = datetime.today()

mapi\_message.flags = ['MsgFlagRead',    'MsgFlagUnsent',    'MsgFlagHasAttach']

recipient\_dto = models.MapiRecipientDto()

recipient\_dto.address\_type = 'SMTP'

recipient\_dto.display\_name = 'To address'

recipient\_dto.email\_address = 'to@aspose.com'

recipient\_dto.recipient\_type = 'MapiTo'

mapi\_message.recipients = [recipient\_dto]

attachment = models.MapiAttachmentDto()

attachment.data\_base64 = str(base64.b64encode(b'Some file text'), 'utf-8')

attachment.name = 'some-file.txt'

mapi\_message.attachments = [attachment]

mapi\_message.body = 'Some body'

mapi\_message.subject = 'Re: Some subject'

mapi\_message.body\_type = 'PlainText'

email\_dto = email.convert\_mapi\_message\_model\_to\_email\_model(

    requests.ConvertMapiMessageModelToEmailModelRequest(mapi\_message))

assert mapi\_message.subject == email\_dto.subject

assert mapi\_message.body == email\_dto.body

```

{{< /tab >}}

{{< tab tabNum="5" >}}

```java

mapi\_message\_dto = MapiMessageDto.new

mapi\_message\_dto.sender\_address\_type = 'SMTP'

mapi\_message\_dto.sender\_email\_address = 'from@aspose.com'

mapi\_message\_dto.sender\_smtp\_address = 'from@aspose.com'

mapi\_message\_dto.sender\_name = 'From Address'

mapi\_message\_dto.message\_body = 'Some body'

mapi\_message\_dto.display\_to = 'To Address'

mapi\_message\_dto.delivery\_time = DateTime.now

mapi\_message\_dto.flags = %w[MsgFlagRead MsgFlagUnsent MsgFlagHasAttach]

recipient\_dto = MapiRecipientDto.new

recipient\_dto.address\_type = 'SMTP'

recipient\_dto.display\_name = 'To address'

recipient\_dto.email\_address = 'to@aspose.com'

recipient\_dto.recipient\_type = 'MapiTo'

mapi\_message\_dto.recipients = [recipient\_dto]

attachment = MapiAttachmentDto.new

attachment.data\_base64 = Base64.encode64('Some file text')

attachment.name = 'some-file.txt'

mapi\_message\_dto.attachments = [attachment]

mapi\_message\_dto.body = 'Some body'

mapi\_message\_dto.subject = 'Re: Some subject'

mapi\_message\_dto.body\_type = 'PlainText'

email = @api.convert\_mapi\_message\_model\_to\_email\_model(

  ConvertMapiMessageModelToEmailModelRequestData.new(mapi\_message))

expect(mapi\_message.subject).to eq email.subject

expect(mapi\_message.body).to eq email.body

```

{{< /tab >}}

{{< tab tabNum="6" >}}

```java

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

        ->setDataBase64(base64\_encode("Some file text"))

        ->setName("some-file.txt")))

    ->setSubjectPrefix("Re: ")

    ->setMessageClass("IPM.Note")

    ->setBody("Some body")

    ->setSubject("Re: Some subject")

    ->setBodyType("PlainText");

$emailDto = $api->convertMapiMessageModelToEmailModel(

    new ConvertMapiMessageModelToEmailModelRequest(

        $mapiMessage

    )

);

$this->assertEquals($mapiMessage->getSubject(), $emailDto->getSubject());

$this->assertEquals($mapiMessage->getBody(), $emailDto->getBody());

```

{{< /tab >}}

{{< /tabs >}}
#### **Convert MapiMessageDto to a File and Back**
**Convert MapiMessageDto to a File and Back**

{{< tabs tabTotal="6" tabID="17" tabName1="C#" tabName2="Java" tabName3="Typescript" tabName4="Python" tabName5="Ruby" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```java

//Convert to a file in EML format:

var emlStream = await emailApi.ConvertMapiMessageModelToFileAsync(

    new ConvertMapiMessageModelToFileRequest(

        "Eml", mapiMessage));

//EML is a text format, let's check it contains subject as text:

using (var memoryStream = new MemoryStream())

{

    await emlStream.CopyToAsync(memoryStream);

    var emlString = Encoding.UTF8.GetString(memoryStream.ToArray());

    Assert.IsTrue(emlString.Contains(mapiMessage.Subject));

}

emlStream.Seek(0, SeekOrigin.Begin);

//Convert file back to a MapiMessageDto object:

var mapiMessageConverted = await EmailApi.GetEmailFileAsMapiModelAsync(

    new GetEmailFileAsMapiModelRequest("Eml", emlStream));

//Check the subject:

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

//Convert to a file in EML format:

byte[] emlBytes = api.convertMapiMessageModelToFile(

    new ConvertMapiMessageModelToFileRequestData(

        "Eml", mapiMessage));

//EML is a text format, let's check it contains subject as text:

String emlString = new String(emlBytes, "UTF-8");

assert emlString.contains(mapiMessage.getSubject());

//Convert file back to a MapiMessageDto object:

MapiMessageDto mapiMessageConverted = api.getEmailFileAsMapiModel(

    new GetEmailFileAsMapiModelRequestData("Eml", emlBytes));

//Check the subject:

assert mapiMessage.getSubject().equals(mapiMessageConverted.getSubject());

String subject = "";

//Subject is also available as MapiPropertyDto:

for (MapiPropertyDto property: mapiMessageConverted.getProperties()) {

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

    MapiStringPropertyDto mapiStringPropertyDto = (MapiStringPropertyDto)property;

    subject = mapiStringPropertyDto.getValue();

}

assert subject.equals(mapiMessage.getSubject());

```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java

//Convert to a file in EML format:

const emlFile = await api.convertMapiMessageModelToFile(

    new requests.ConvertMapiMessageModelToFileRequest('Eml', mapiMessageDto));

//EML is a text format, let's check it contains subject as text:

const emlString = emlFile.body.toString();

expect(emlString).to.contain(mapiMessageDto.subject);

//Convert file back to a MapiMessageDto object:

const mapiMessageDtoConverted = await api.getEmailFileAsMapiModel(

    new requests.GetEmailFileAsMapiModelRequest('Eml', emlFile.body));

//Check the subject:

expect(mapiMessageDto.subject).to.be.eq(mapiMessageDtoConverted.body.subject);

//Subject is also available as MapiPropertyDto:

const subjectProperty = mapiMessageDtoConverted.body.properties

    //There are different Property descriptors supported.

    //Some properties are known to the service:

    .filter(i => i.descriptor.discriminator == 'MapiKnownPropertyDescriptor')

    //So we can find them by name:

    .find(i => (i.descriptor as models.MapiKnownPropertyDescriptor).name == 'TagSubject');

//Subject is a string, so it is stored in MapiStringPropertyDto:

const subjectString = (subjectProperty as models.MapiStringPropertyDto).value;

expect(mapiMessageDto.subject).to.be.eq(subjectString);

```

{{< /tab >}}

{{< tab tabNum="4" >}}

```java

\# Convert to a file in EML format:

eml\_file = email.convert\_mapi\_message\_model\_to\_file(

    requests.ConvertMapiMessageModelToFileRequest('Eml', mapi\_message))

\# EML is a text format, let's check it contains subject as text:

with open(eml\_file, 'r') as f:

    file\_data = f.read()

    assert mapi\_message.subject in file\_data

\# Convert file back to a MapiMessageDto object:

mapi\_message\_converted = email.get\_email\_file\_as\_mapi\_model(

    requests.GetEmailFileAsMapiModelRequest('Eml', eml\_file))

\# Check the subject:

assert mapi\_message.subject == mapi\_message\_converted.subject

\# Subject is also available as MapiPropertyDto:

\# There are different Property descriptors supported.

\# Some properties are known to the service and have MapiKnownPropertyDescriptor

known\_properties = [x for x in mapi\_message\_converted.properties

                    if x.descriptor.discriminator == 'MapiKnownPropertyDescriptor']

\# So we can find subject property by known property name:

subject\_property = next(x for x in known\_properties if x.descriptor.name == 'TagSubject')

assert mapi\_message.subject == subject\_property.value

```

{{< /tab >}}

{{< tab tabNum="5" >}}

```java

\# Convert to a file in EML format:

eml\_file = @api.convert\_mapi\_message\_model\_to\_file(

  ConvertMapiMessageModelToFileRequestData.new('Eml', mapi\_message))

\# EML is a text format, let's check it contains subject as text:

eml\_content = IO.read(eml\_file)

expect(eml\_content).to include mapi\_message.subject

\# Convert file back to a MapiMessageDto object:

mapi\_message\_converted = @api.get\_email\_file\_as\_mapi\_model(

  GetEmailFileAsMapiModelRequestData.new('Eml', eml\_file))

\# Check the subject:

expect(mapi\_message.subject).to eq mapi\_message\_converted.subject

\# Subject is also available as MapiPropertyDto:

\# There are different Property descriptors supported.

\# Some properties are known to the service and have MapiKnownPropertyDescriptor

\# So we can find subject property by known property name:

subject\_property = mapi\_message\_converted

                   .properties

                   .filter { |i| i.descriptor.discriminator == 'MapiKnownPropertyDescriptor' }

                   .find { |i| i.descriptor.name == 'TagSubject' }

expect(mapi\_message.subject).to eq subject\_property.value

```

{{< /tab >}}

{{< tab tabNum="6" >}}

```java

//Convert to a file in EML format:

$emlFile = $api->convertMapiMessageModelToFile(

    new ConvertMapiMessageModelToFileRequest(

        "Eml",

        $mapiMessage

    )

);

//EML is a text format, let's check it contains subject as text:

$fileContent = $emlFile->fread($emlFile->getSize());

$this->assertRegExp("/" . $mapiMessage->getSubject() . "/", $fileContent);

//Convert file back to a MapiMessageDto object:

$mapiMessageConverted = $api->getEmailFileAsMapiModel(

    new GetEmailFileAsMapiModelRequest("Eml", $emlFile)

);

//Check the subject:

$this->assertEquals($mapiMessage->getSubject(), $mapiMessageConverted->getSubject());

//Subject is also available as MapiPropertyDto:

//There are different Property descriptors supported.

//Some properties are known to the service:

$knownPropertiesArray =

    array\_filter($mapiMessageConverted->getProperties(), function ($var) {

        return $var->getDescriptor()->getDiscriminator() == "MapiKnownPropertyDescriptor";

    });

//We know, that subject is stored in known property with name TagSubject:

$subjectProperty = array\_values(

    array\_filter($knownPropertiesArray, function ($var) {

        /\*\* @noinspection PhpPossiblePolymorphicInvocationInspection \*/

        return $var->getDescriptor()->getName() == 'TagSubject';

    })

)[0];

$this->assertEquals($mapiMessage->getSubject(), $subjectProperty->getValue());

```

{{< /tab >}}

{{< /tabs >}}
#### **MapiMessageDto and Cloud Storage**
**How to Work with MapiMessageDto and Cloud Storage**

{{< tabs tabTotal="6" tabID="24" tabName1="C#" tabName2="Java" tabName3="Typescript" tabName4="Python" tabName5="Ruby" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```java

var storageName = "First Storage";

var folder = "a/folder/on/a/storage";

var fileName = "fileName.msg";

// Save as a file on storage:

await emailApi.SaveMapiMessageModelAsync(

    new SaveMapiMessageModelRequest(

        "Msg", fileName, new StorageModelRqOfMapiMessageDto(

            mapiMessage, new StorageFolderLocation(storageName, folder))));

// Get back from storage:

var mapiMessageFromStorage = await emailApi.GetMapiMessageModelAsync(

    new GetMapiMessageModelRequest(

        "Msg", fileName, folder, storageName));

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

api.saveMapiMessageModel(

    new SaveMapiMessageModelRequestData(

        "Msg", fileName, new StorageModelRqOfMapiMessageDto(

        mapiMessage, new StorageFolderLocation(storage, folder))));

// Get back from storage:

MapiMessageDto mapiMessageFromStorage = api.getMapiMessageModel(

    new GetMapiMessageModelRequestData(

        "Msg", fileName, folder, storage));

// Compare

assert mapiMessage.getSubject().equals(mapiMessageFromStorage.getSubject());

```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java

const storage = "First Storage";

const folder = "a/folder/on/a/storage";

const fileName = "fileName.msg";

// Save as a file on storage:

await api.saveMapiMessageModel(

    new requests.SaveMapiMessageModelRequest('Msg', fileName,

        new models.StorageModelRqOfMapiMessageDto(

            mapiMessageDto,

            new models.StorageFolderLocation(storage, folder))));

// Get back from storage:

const mapiMessageFromStorage = await api.getMapiMessageModel(

    new requests.GetMapiMessageModelRequest('Msg', fileName, folder, storage));

// Compare

expect(mapiMessageDto.subject).to.be.eq(mapiMessageFromStorage.body.subject);

```

{{< /tab >}}

{{< tab tabNum="4" >}}

```java

storage = "First Storage"

folder = "a/folder/on/a/storage"

file\_name = "fileName.msg"

\# Save as a file on storage:

email.save\_mapi\_message\_model(

    requests.SaveMapiMessageModelRequest(

        'Msg', file\_name,

        models.StorageModelRqOfMapiMessageDto(

            mapi\_message,

            models.StorageFolderLocation(storage, folder))))

\# Get back from storage:

mapi\_message\_from\_storage = email.get\_mapi\_message\_model(

    requests.GetMapiMessageModelRequest('Msg', file\_name, folder, storage))

\# Compare

assert mapi\_message.subject == mapi\_message\_from\_storage.subject

```

{{< /tab >}}

{{< tab tabNum="5" >}}

```java

 storage = 'First Storage'

folder = 'a/folder/on/a/storage'

file\_name = 'fileName.msg'

\# Save as a file on storage:

@api.save\_mapi\_message\_model(

  SaveMapiMessageModelRequestData.new(

    'Msg', file\_name,

    StorageModelRqOfMapiMessageDto.new(

      mapi\_message,

      StorageFolderLocation.new(storage, folder)

    )

  )

)

\# Get back from storage:

mapi\_message\_from\_storage = @api.get\_mapi\_message\_model(

  GetMapiMessageModelRequestData.new('Msg', file\_name, @folder, @storage))

\# Compare

expect(mapi\_message.subject).to eq mapi\_message\_from\_storage.subject

```

{{< /tab >}}

{{< tab tabNum="6" >}}

```java

$storage = "First Storage";

$folder = "a/folder/on/a/storage";

$fileName = "fileName.msg";

// Save as a file on storage:

$api->saveMapiMessageModel(

    new SaveMapiMessageModelRequest(

        "Msg",

        $fileName,

        new StorageModelRqOfMapiMessageDto(

            $mapiMessage,

            new StorageFolderLocation($storage, $folder)

        )

    )

);

// Get back from storage:

$mapiMessageFromStorage = $api->getMapiMessageModel(

    new GetMapiMessageModelRequest(

        "Msg",

        $fileName,

        $folder,

        $storage

    )

);

// Compare

$this->assertEquals($mapiMessage->getSubject(), $mapiMessageFromStorage->getSubject());

```

{{< /tab >}}

{{< /tabs >}}
### **MapiContactDto methods**
#### **Convert ContactDto to MapiContactDto**
**How to Convert ContactDto to MapiContactDto**

{{< tabs tabTotal="6" tabID="31" tabName1="C#" tabName2="Java" tabName3="Typescript" tabName4="Python" tabName5="Ruby" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```java

ContactDto contact = new ContactDto

{

    Gender = "Male",

    Surname = "Thomas",

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

MapiContactDto mapiContact = await emailApi.ConvertContactModelToMapiModelAsync(

    new ConvertContactModelToMapiModelRequest(contact));

Assert.AreEqual(Contact.Surname, mapiContact.NameInfo.Surname);

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

ContactDto contactDto = new ContactDto()

    .gender("Male")

    .surname("Thomas")

    .givenName("Alex")

    .addEmailAddressesItem(new EmailAddress(

        new EnumWithCustomOfEmailAddressCategory("Work", null),

        "Alex Thomas", true, null, "alex.thomas@work.com", null))

    .addPhoneNumbersItem(new PhoneNumber(

        new EnumWithCustomOfPhoneNumberCategory("Work", null),

        "+49211424721", true));

MapiContactDto mapiContactDto = api.convertContactModelToMapiModel(

    new ConvertContactModelToMapiModelRequestData(contactDto));

assert contactDto.getSurname().equals(mapiContactDto.getNameInfo().getSurname());

```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java

let contactDto = new models.ContactDto();

contactDto.surname = 'Cane';

contactDto.givenName = 'John';

contactDto.gender = 'Male';

const emailAddress = new models.EmailAddress();

emailAddress.address = 'address@aspose.com'

contactDto.emailAddresses = [emailAddress];

contactDto.phoneNumbers = [new models.PhoneNumber(undefined, '+47234325344')];

const mapiContactDto = await api.convertContactModelToMapiModel(

    new requests.ConvertContactModelToMapiModelRequest(contactDto));

expect(contactDto.surname).to.be.eq(mapiContactDto.body.nameInfo.surname);

```

{{< /tab >}}

{{< tab tabNum="4" >}}

```java

contact = models.ContactDto(

    gender='Male',

    surname='Thomas',

    given\_name='Alex',

    email\_addresses=[

        models.EmailAddress(

            models.EnumWithCustomOfEmailAddressCategory('Work'),

            'Alex Thomas', True, address='alex.thomas@work.com')],

    phone\_numbers=[

        models.PhoneNumber(

            models.EnumWithCustomOfPhoneNumberCategory('Work'),

            '+49211424721', True)])

mapi\_contact = email.convert\_contact\_model\_to\_mapi\_model(

    requests.ConvertContactModelToMapiModelRequest(contact))

assert contact.surname == mapi\_contact.name\_info.surname

```

{{< /tab >}}

{{< tab tabNum="5" >}}

```java

contact = ContactDto.new

contact.surname = 'Cane'

contact.given\_name = 'John'

contact.gender = 'Male'

contact.email\_addresses = [EmailAddress.new(nil, nil, nil, nil, 'address@aspose.com')]

contact.phone\_numbers = [PhoneNumber.new(nil, '+4734534643')]

mapi\_contact = @api.convert\_contact\_model\_to\_mapi\_model(

  ConvertContactModelToMapiModelRequestData.new(contact)

)

expect(contact.surname).to eq mapi\_contact.name\_info.surname

```

{{< /tab >}}

{{< tab tabNum="6" >}}

```java

$contactDto = (new ContactDto())

    ->setSurname('Cane')

    ->setGivenName('John')

    ->setGender('Male')

    ->setEmailAddresses(array((new EmailAddress())->setAddress('address@aspose.com')))

    ->setPhoneNumbers(array((new PhoneNumber())->setNumber('+47235456456')));

$mapiContact = $api->convertContactModelToMapiModel(

    new ConvertContactModelToMapiModelRequest($contactDto)

);

$this->assertEquals($contactDto->getSurname(), $mapiContact->getNameInfo()->getSurname());

```

{{< /tab >}}

{{< /tabs >}}
#### **Convert MapiContactDto to ContactDto**
**How to Convert MapiContactDto to ContactDto:**

{{< tabs tabTotal="6" tabID="38" tabName1="C#" tabName2="Java" tabName3="Typescript" tabName4="Python" tabName5="Ruby" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```java

MapiContactDto mapiContact = new MapiContactDto

{

    ElectronicAddresses = new MapiContactElectronicAddressPropertySetDto

    {

        DefaultEmailAddress = new MapiContactElectronicAddressDto

            {EmailAddress = "email@aspose.com"}

    },

    NameInfo = new MapiContactNamePropertySetDto {GivenName = "Alex", Surname = "Thomas"},

    PersonalInfo = new MapiContactPersonalInfoPropertySetDto

        {BusinessHomePage = ""},

    ProfessionalInfo = new MapiContactProfessionalPropertySetDto

        {Profession = "GENERAL DIRECTOR"},

    Telephones = new MapiContactTelephonePropertySetDto

        {PrimaryTelephoneNumber = "+49 211 4247 21"}

};

var contactDto =

    await emailApi.ConvertMapiContactModelToContactModelAsync(

        new ConvertMapiContactModelToContactModelRequest(

            mapiContact));

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

        .businessHomePage(""))

    .professionalInfo(new MapiContactProfessionalPropertySetDto()

        .profession("GENERAL DIRECTOR"))

    .telephones(new MapiContactTelephonePropertySetDto()

        .primaryTelephoneNumber("+49 211 4247 21"));

ContactDto contactDto = api.convertMapiContactModelToContactModel(

    new ConvertMapiContactModelToContactModelRequestData(

        mapiContact));

assert mapiContact.getNameInfo().getGivenName().equals( contactDto.getGivenName());

assert mapiContact.getNameInfo().getSurname().equals( contactDto.getSurname());

```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java

const mapiContactDto = new models.MapiContactDto();

mapiContactDto.electronicAddresses = new models.MapiContactElectronicAddressPropertySetDto();

mapiContactDto.electronicAddresses.defaultEmailAddress = new models.MapiContactElectronicAddressDto();

mapiContactDto.electronicAddresses.defaultEmailAddress.emailAddress = "email@aspose.com";

mapiContactDto.nameInfo = new models.MapiContactNamePropertySetDto();

mapiContactDto.nameInfo.givenName = "Alex";

mapiContactDto.nameInfo.surname = "Thomas";

mapiContactDto.personalInfo = new models.MapiContactPersonalInfoPropertySetDto();

mapiContactDto.personalInfo.businessHomePage = "www.aspose.com";

mapiContactDto.professionalInfo = new models.MapiContactProfessionalPropertySetDto();

mapiContactDto.professionalInfo.profession = "GENERAL DIRECTOR";

mapiContactDto.telephones = new models.MapiContactTelephonePropertySetDto();

mapiContactDto.telephones.primaryTelephoneNumber = "+49 211 4247 21";

const contactDto = await api.convertMapiContactModelToContactModel(

    new requests.ConvertMapiContactModelToContactModelRequest(mapiContactDto));

expect(mapiContactDto.nameInfo.givenName).to.be.eq(contactDto.body.givenName);

expect(mapiContactDto.nameInfo.surname).to.be.eq(contactDto.body.surname);

```

{{< /tab >}}

{{< tab tabNum="4" >}}

```java

mapi\_contact = models.MapiContactDto()

electronic\_addresses = models.MapiContactElectronicAddressPropertySetDto()

electronic\_addresses.default\_email\_address = models.MapiContactElectronicAddressDto()

electronic\_addresses.default\_email\_address.email\_address = 'email@aspose.com'

mapi\_contact.electronic\_addresses = electronic\_addresses

name\_info = models.MapiContactNamePropertySetDto()

name\_info.given\_name = 'Alex'

name\_info.surname = 'Thomas'

mapi\_contact.name\_info = name\_info

mapi\_contact.personal\_info = models.MapiContactPersonalInfoPropertySetDto()

mapi\_contact.personal\_info.business\_home\_page = 'www.aspose.com'

mapi\_contact.professional\_info = models.MapiContactProfessionalPropertySetDto()

mapi\_contact.professional\_info.profession = 'GENERAL DIRECTOR'

mapi\_contact.telephones = models.MapiContactTelephonePropertySetDto()

mapi\_contact.telephones.primary\_telephone\_number = '+49 211 4247 21'

contact = email.convert\_mapi\_contact\_model\_to\_contact\_model(

  requests.ConvertMapiContactModelToContactModelRequest(mapi\_contact))

assert mapi\_contact.name\_info.given\_name == contact.given\_name

assert mapi\_contact.name\_info.surname == contact.surname

```

{{< /tab >}}

{{< tab tabNum="5" >}}

```java

mapi\_contact = MapiContactDto.new

electronic\_addresses = MapiContactElectronicAddressPropertySetDto.new

electronic\_addresses.default\_email\_address = MapiContactElectronicAddressDto.new

electronic\_addresses.default\_email\_address.email\_address = 'email@aspose.com'

mapi\_contact.electronic\_addresses = electronic\_addresses

name\_info = MapiContactNamePropertySetDto.new

name\_info.given\_name = 'Alex'

name\_info.surname = 'Thomas'

mapi\_contact.name\_info = name\_info

mapi\_contact.personal\_info = MapiContactPersonalInfoPropertySetDto.new

mapi\_contact.personal\_info.business\_home\_page = 'www.aspose.com'

mapi\_contact.professional\_info = MapiContactProfessionalPropertySetDto.new

mapi\_contact.professional\_info.profession = 'GENERAL DIRECTOR'

mapi\_contact.telephones = MapiContactTelephonePropertySetDto.new

mapi\_contact.telephones.primary\_telephone\_number = '+49 211 4247 21'

contact = @api.convert\_mapi\_contact\_model\_to\_contact\_model(

  ConvertMapiContactModelToContactModelRequestData.new(mapi\_contact))

expect(mapi\_contact.name\_info.given\_name).to eq contact.given\_name

expect(mapi\_contact.name\_info.surname).to eq contact.surname

```

{{< /tab >}}

{{< tab tabNum="6" >}}

```java

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

$contactDto = $api->convertMapiContactModelToContactModel(

    new ConvertMapiContactModelToContactModelRequest(

        $mapiContact

    )

);

$this->assertEquals(

    $mapiContact->getNameInfo()->getGivenName(),

    $contactDto->getGivenName()

);

$this->assertEquals($mapiContact->getNameInfo()->getSurname(), $contactDto->getSurname());

```

{{< /tab >}}

{{< /tabs >}}
#### **Convert MapiContactDto to a File and Back**
**How to Convert MapiContactDto to a File and Back:**

{{< tabs tabTotal="6" tabID="45" tabName1="C#" tabName2="Java" tabName3="Typescript" tabName4="Python" tabName5="Ruby" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```java

var vcardStream = await emailApi.ConvertMapiContactModelToFileAsync(

    new ConvertMapiContactModelToFileRequest(

        "VCard", mapiContact));

using (var memoryStream = new MemoryStream())

{

    await vcardStream.CopyToAsync(memoryStream);

    var vcardString = Encoding.UTF8.GetString(memoryStream.ToArray());

    Assert.IsTrue(vcardString.Contains(mapiContact.NameInfo.GivenName));

}

vcardStream.Seek(0, SeekOrigin.Begin);

var mapiContactConverted = await emailApi.GetContactFileAsMapiModelAsync(

    new GetContactFileAsMapiModelRequest("VCard", vcardStream));

Assert.AreEqual(mapiContact.NameInfo.Surname, mapiContactConverted.NameInfo.Surname);

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

byte[] vcardBytes = api.convertMapiContactModelToFile(

    new ConvertMapiContactModelToFileRequestData(

        "VCard", mapiContact));

String vcardString = new String(vcardBytes, "UTF-8");

assert vcardString.contains(mapiContact.getNameInfo().getGivenName());

MapiContactDto mapiContactConverted = api.getContactFileAsMapiModel(

    new GetContactFileAsMapiModelRequestData("VCard", vcardBytes));

assert mapiContact.getNameInfo().getSurname().equals( mapiContactConverted.getNameInfo().getSurname());

```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java

const vcardFile = await api.convertMapiContactModelToFile(

    new requests.ConvertMapiContactModelToFileRequest('VCard', mapiContactDto));

const vcardString = vcardFile.body.toString();

expect(vcardString).to.contain(mapiContactDto.nameInfo.givenName);

const mapiContactDtoConverted = await api.getContactFileAsMapiModel(

    new requests.GetContactFileAsMapiModelRequest('VCard', vcardFile.body));

expect(mapiContactDto.nameInfo.surname).to.be.eq(mapiContactDtoConverted.body.nameInfo.surname);

```

{{< /tab >}}

{{< tab tabNum="4" >}}

```java

vcard\_file = email.convert\_mapi\_contact\_model\_to\_file(

    requests.ConvertMapiContactModelToFileRequest('VCard', mapi\_contact))

with open(vcard\_file, 'r') as f:

    file\_data = f.read()

    assert mapi\_contact.name\_info.given\_name in file\_data

mapi\_contact\_converted = email.get\_contact\_file\_as\_mapi\_model(

    requests.GetContactFileAsMapiModelRequest('VCard', vcard\_file))

assert mapi\_contact.name\_info.surname == mapi\_contact\_converted.name\_info.surname

```

{{< /tab >}}

{{< tab tabNum="5" >}}

```java

vcard\_file = @api.convert\_mapi\_contact\_model\_to\_file(

  ConvertMapiContactModelToFileRequestData.new('VCard', mapi\_contact))

vcard\_content = IO.read(vcard\_file)

expect(vcard\_content).to include mapi\_contact.name\_info.given\_name

mapi\_contact\_converted = @api.get\_contact\_file\_as\_mapi\_model(

  GetContactFileAsMapiModelRequestData.new('VCard', vcard\_file))

expect(mapi\_contact.name\_info.surname).to eq mapi\_contact\_converted.name\_info.surname

```

{{< /tab >}}

{{< tab tabNum="6" >}}

```java

$vcardFile = $api->convertMapiContactModelToFile(

    new ConvertMapiContactModelToFileRequest(

        "VCard",

        $mapiContact

    )

);

$fileContent = $vcardFile->fread($vcardFile->getSize());

$this->assertRegExp("/" . $mapiContact->getNameInfo()->getGivenName() . "/", $fileContent);

$mapiContactConverted = $api->getContactFileAsMapiModel(

    new GetContactFileAsMapiModelRequest("VCard", $vcardFile)

);

$this->assertEquals($mapiContact->getNameInfo()->getSurname(), $mapiContactConverted

    ->getNameInfo()->getSurname());

```

{{< /tab >}}

{{< /tabs >}}
#### **MapiContactDto and Cloud Storage**
**Work with MapiContactDto and Cloud Storage**

{{< tabs tabTotal="6" tabID="52" tabName1="C#" tabName2="Java" tabName3="Typescript" tabName4="Python" tabName5="Ruby" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```java

var storageName = "First Storage";

var folder = "a/folder/on/a/storage";

var fileName = "fileName.msg";



await emailApi.SaveMapiContactModelAsync(

    new SaveMapiContactModelRequest(

        "Msg", fileName, new StorageModelRqOfMapiContactDto(

            mapiContact, new StorageFolderLocation(storage, folder))));

var mapiContactFromStorage = await emailApi.GetMapiContactModelAsync(

    new GetMapiContactModelRequest(

        "Msg", fileName, folder, storage));

Assert.AreEqual(mapiContact.NameInfo.Surname, mapiContactFromStorage.NameInfo.Surname);

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

String storage = "First Storage";

String folder = "a/folder/on/a/storage";

String fileName = "fileName.msg";


api.saveMapiContactModel(

    new SaveMapiContactModelRequestData(

        "Msg", fileName, new StorageModelRqOfMapiContactDto(

        mapiContact, new StorageFolderLocation(storage, folder))));

MapiContactDto mapiContactFromStorage = api.getMapiContactModel(

    new GetMapiContactModelRequestData(

        "Msg", fileName, folder, storage));

assert mapiContact.getNameInfo().getSurname().equals(mapiContactFromStorage.getNameInfo().getSurname());

```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java

const storage = "First Storage";

const folder = "a/folder/on/a/storage";

const fileName = "fileName.msg";


await api.saveMapiContactModel(

    new requests.SaveMapiContactModelRequest('Msg', fileName,

        new models.StorageModelRqOfMapiContactDto(mapiContactDto, new models.StorageFolderLocation(storage, folder))));

const mapiContactFromStorage = await api.getMapiContactModel(

    new requests.GetMapiContactModelRequest('Msg', fileName, folder, storage));

expect(mapiContactDto.nameInfo.surname).to.be.eq(mapiContactFromStorage.body.nameInfo.surname);

```

{{< /tab >}}

{{< tab tabNum="4" >}}

```java

storage = "First Storage"

folder = "a/folder/on/a/storage"

file\_name = "fileName.msg"



email.save\_mapi\_contact\_model(

    requests.SaveMapiContactModelRequest(

        'Msg', file\_name,

        models.StorageModelRqOfMapiContactDto(mapi\_contact, models.StorageFolderLocation(storage, folder))))

mapi\_contact\_from\_storage = email.get\_mapi\_contact\_model(

    requests.GetMapiContactModelRequest('Msg', file\_name, folder, storage))

assert mapi\_contact.name\_info.surname == mapi\_contact\_from\_storage.name\_info.surname

```

{{< /tab >}}

{{< tab tabNum="5" >}}

```java

storage = 'First Storage'

folder = 'a/folder/on/a/storage'

file\_name = 'fileName.msg'

@api.save\_mapi\_contact\_model(

  SaveMapiContactModelRequestData.new(

    'Msg', file\_name,

    StorageModelRqOfMapiContactDto.new(mapi\_contact, StorageFolderLocation.new(storage, folder))))

mapi\_contact\_from\_storage = @api.get\_mapi\_contact\_model(

  GetMapiContactModelRequestData.new('Msg', file\_name, @folder, @storage))

expect(mapi\_contact.name\_info.surname).to eq mapi\_contact\_from\_storage.name\_info.surname

```

{{< /tab >}}

{{< tab tabNum="6" >}}

```java

$storage = "First Storage";

$folder = "a/folder/on/a/storage";

$fileName = "fileName.msg";


$api->saveMapiContactModel(

    new SaveMapiContactModelRequest(

        "Msg",

        $fileName,

        new StorageModelRqOfMapiContactDto(

            $mapiContact,

            new StorageFolderLocation($storage, $folder)

        )

    )

);

$mapiContactFromStorage = $api->getMapiContactModel(

    new GetMapiContactModelRequest(

        "Msg",

        $fileName,

        $folder,

        $storage

    )

);

$this->assertEquals($mapiContact->getNameInfo()->getSurname(), $mapiContactFromStorage

    ->getNameInfo()->getSurname());

```

{{< /tab >}}

{{< /tabs >}}
### **MapiCalendarDto methods**
#### **Convert CalendarDto to MapiCalendarDto**
**How to Convert CalendarDto to MapiCalendarDto:**

{{< tabs tabTotal="6" tabID="59" tabName1="C#" tabName2="Java" tabName3="Typescript" tabName4="Python" tabName5="Ruby" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```java

CalendarDto calendar = new CalendarDto

{

    Location = Location, Description = "Some description", Summary = "Some summary",

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

var mapiCalendar = await emailApi.ConvertCalendarModelToMapiModelAsync(

    new ConvertCalendarModelToMapiModelRequest(calendar));

Assert.AreEqual(calendar.Location, mapiCalendar.Location);

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

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

MapiCalendarDto mapiCalendarDto = api.convertCalendarModelToMapiModel(

    new ConvertCalendarModelToMapiModelRequestData(calendarDto));

assert calendarDto.getLocation().equals(mapiCalendarDto.getLocation());



```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java

let calendar = new models.CalendarDto();

calendar.attendees = [

    new models.MailAddress('Attendee Name', 'attendee@am.ru', 'Accepted')

];

calendar.description = 'Some description';

calendar.summary = 'Some summary';

calendar.organizer = new models.MailAddress('Organizer Name', 'organizer@am.ru');

calendar.startDate = new Date();

calendar.endDate = new Date();

calendar.location = 'Some location';

calendar.recurrence = new models.DailyRecurrencePatternDto(undefined, 10, undefined, "Monday");

const mapiCalendarDto = await api.convertCalendarModelToMapiModel(

    new requests.ConvertCalendarModelToMapiModelRequest(calendar));

expect(calendar.location).to.be.eq(mapiCalendarDto.body.location);



```

{{< /tab >}}

{{< tab tabNum="4" >}}

```java

calendar = models.CalendarDto()

calendar.attendees = [models.MailAddress('Attendee Name', 'attendee@aspose.com', 'Accepted')]

calendar.description = 'Some description'

calendar.summary = 'Some summary'

calendar.organizer = models.MailAddress('Organizer Name', 'organizer@aspose.com', 'Accepted')

calendar.start\_date = datetime.today() + timedelta(days=1)

calendar.end\_date = calendar.start\_date + timedelta(hours=1)

calendar.location = 'Some location'

calendar.recurrence = models.DailyRecurrencePatternDto(None, 10, None, 'Monday')

mapi\_calendar = email.convert\_calendar\_model\_to\_mapi\_model(

    requests.ConvertCalendarModelToMapiModelRequest(calendar))

assert calendar.location == mapi\_calendar.location



```

{{< /tab >}}

{{< tab tabNum="5" >}}

```java

calendar = CalendarDto.new

calendar.location = 'Some location'

calendar.summary = 'Some summary'

calendar.description = 'Some description'

calendar.start\_date = DateTime.now

calendar.end\_date = DateTime.now + 1

calendar.organizer = MailAddress.new nil, 'organizer@aspose.com'

calendar.attendees = [MailAddress.new(nil, 'attendee@aspose.com')]

calendar.recurrence = DailyRecurrencePatternDto.new(nil, 10, nil, 'Monday')

mapi\_calendar = @api.convert\_calendar\_model\_to\_mapi\_model(

  ConvertCalendarModelToMapiModelRequestData.new(calendar))

expect(calendar.location).to eq mapi\_calendar.location

```

{{< /tab >}}

{{< tab tabNum="6" >}}

```java

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

$mapiCalendar = $api->convertCalendarModelToMapiModel(

    new ConvertCalendarModelToMapiModelRequest($calendar)

);

$this->assertEquals($calendar->getLocation(), $mapiCalendar->getLocation());

```

{{< /tab >}}

{{< /tabs >}}
#### **Convert MapiCalendarDto to CalendarDto**
**How to Convert MapiCalendarDto to CalendarDto:**

{{< tabs tabTotal="6" tabID="66" tabName1="C#" tabName2="Java" tabName3="Typescript" tabName4="Python" tabName5="Ruby" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```java

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

CalendarDto calendarDto =

    await emailApi.ConvertMapiCalendarModelToCalendarModelAsync(

        new ConvertMapiCalendarModelToCalendarModelRequest(

            mapiCalendar));

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

CalendarDto calendarDto = api.convertMapiCalendarModelToCalendarModel(

    new ConvertMapiCalendarModelToCalendarModelRequestData(

        mapiCalendar));

assert mapiCalendar.getSubject().equals(calendarDto.getSummary());

assert mapiCalendar.getLocation().equals(calendarDto.getLocation());

```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java

const mapiCalendarDto = new models.MapiCalendarDto();

const mapiRecipientDto = new models.MapiRecipientDto();

mapiRecipientDto.addressType = "SMTP";

mapiRecipientDto.displayName = "Attendee Name";

mapiRecipientDto.emailAddress = "attendee@aspose.com";

mapiRecipientDto.recipientType = "MapiTo";

mapiCalendarDto.attendees = new models.MapiCalendarAttendeesDto([mapiRecipientDto]);

mapiCalendarDto.clientIntent = ["Manager"];

const recurrence = new models.MapiCalendarEventRecurrenceDto();

const recurrencePatternDto = new models.MapiCalendarDailyRecurrencePatternDto();

recurrencePatternDto.occurrenceCount = 10;

recurrencePatternDto.weekStartDay = "Monday";

recurrence.recurrencePattern = recurrencePatternDto;

mapiCalendarDto.recurrence = recurrence;

mapiCalendarDto.organizer = new models.MapiElectronicAddressDto(undefined, "organizer@aspose.com");

mapiCalendarDto.busyStatus = "Tentative";

mapiCalendarDto.startDate = new Date();

mapiCalendarDto.endDate = new Date();

mapiCalendarDto.location = "Some location";

mapiCalendarDto.body = "Some description";

mapiCalendarDto.bodyType = "PlainText";

mapiCalendarDto.subject = "Some summary";

const calendarDto = await api.convertMapiCalendarModelToCalendarModel(

    new requests.ConvertMapiCalendarModelToCalendarModelRequest(mapiCalendarDto));

expect(mapiCalendarDto.subject).to.be.eq(calendarDto.body.summary);

expect(mapiCalendarDto.location).to.be.eq(calendarDto.body.location);

```

{{< /tab >}}

{{< tab tabNum="4" >}}

```java

mapi\_calendar = models.MapiCalendarDto()

mapi\_recipient = models.MapiRecipientDto()

mapi\_recipient.address\_type = 'SMTP'

mapi\_recipient.display\_name = 'Attendee Name'

mapi\_recipient.email\_address = 'attendee@aspose.com'

mapi\_recipient.recipient\_type = 'MapiTo'

mapi\_calendar.attendees = models.MapiCalendarAttendeesDto([mapi\_recipient])

mapi\_calendar.client\_intent = ['Manager']

recurrence = models.MapiCalendarEventRecurrenceDto()

recurrence\_pattern = models.MapiCalendarDailyRecurrencePatternDto()

recurrence\_pattern.occurrence\_count = 10

recurrence\_pattern.week\_start\_day = 'Monday'

recurrence.recurrence\_pattern = recurrence\_pattern

mapi\_calendar.recurrence = recurrence

mapi\_calendar.organizer = models.MapiElectronicAddressDto(None, 'organizer@aspose.com')

mapi\_calendar.busy\_status = 'Tentative'

mapi\_calendar.start\_date = datetime.today()

mapi\_calendar.end\_date = datetime.today()

mapi\_calendar.location = 'Some location'

mapi\_calendar.body = 'Some description'

mapi\_calendar.body\_type = 'PlainText'

mapi\_calendar.subject = 'Some summary'

calendar = email.convert\_mapi\_calendar\_model\_to\_calendar\_model(

    requests.ConvertMapiCalendarModelToCalendarModelRequest(mapi\_calendar))

assert mapi\_calendar.subject == calendar.summary

assert mapi\_calendar.location == calendar.location

```

{{< /tab >}}

{{< tab tabNum="5" >}}

```java

mapi\_calendar = MapiCalendarDto.new

mapi\_recipient = MapiRecipientDto.new

mapi\_recipient.address\_type = 'SMTP'

mapi\_recipient.display\_name = 'Attendee Name'

mapi\_recipient.email\_address = 'attendee@aspose.com'

mapi\_recipient.recipient\_type = 'MapiTo'

mapi\_calendar.attendees = MapiCalendarAttendeesDto.new([mapi\_recipient])

mapi\_calendar.client\_intent = ['Manager']

recurrence = MapiCalendarEventRecurrenceDto.new

recurrence\_pattern = MapiCalendarDailyRecurrencePatternDto.new

recurrence\_pattern.occurrence\_count = 10

recurrence\_pattern.week\_start\_day = 'Monday'

recurrence.recurrence\_pattern = recurrence\_pattern

mapi\_calendar.recurrence = recurrence

mapi\_calendar.organizer = MapiElectronicAddressDto.new(nil, 'organizer@aspose.com')

mapi\_calendar.busy\_status = 'Tentative'

mapi\_calendar.start\_date = DateTime.now

mapi\_calendar.end\_date = DateTime.now + 1

mapi\_calendar.location = 'Some location'

mapi\_calendar.body = 'Some description'

mapi\_calendar.body\_type = 'PlainText'

mapi\_calendar.subject = 'Some summary'

calendar = @api.convert\_mapi\_calendar\_model\_to\_calendar\_model(

  ConvertMapiCalendarModelToCalendarModelRequestData.new(mapi\_calendar))

expect(mapi\_calendar.subject).to eq calendar.summary

expect(mapi\_calendar.location).to eq calendar.location

```

{{< /tab >}}

{{< tab tabNum="6" >}}

```java

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

$calendarDto = $api->convertMapiCalendarModelToCalendarModel(

    new ConvertMapiCalendarModelToCalendarModelRequest(

        $mapiCalendar

    )

);

$this->assertEquals($mapiCalendar->getSubject(), $calendarDto->getSummary());

$this->assertEquals($mapiCalendar->getLocation(), $calendarDto->getLocation());

```

{{< /tab >}}

{{< /tabs >}}
#### **Convert MapiCalendarDto to a File and Back**
**How to Convert MapiCalendarDto to a File and Back:**

{{< tabs tabTotal="6" tabID="73" tabName1="C#" tabName2="Java" tabName3="Typescript" tabName4="Python" tabName5="Ruby" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```java

var icsStream = await emailApi.ConvertMapiCalendarModelToFileAsync(

    new ConvertMapiCalendarModelToFileRequest(

        "Ics", mapiCalendar));

using (var memoryStream = new MemoryStream())

{

    await icsStream.CopyToAsync(memoryStream);

    var icsString = Encoding.UTF8.GetString(memoryStream.ToArray());

    Assert.IsTrue(icsString.Contains(mapiCalendar.Location));

}

icsStream.Seek(0, SeekOrigin.Begin);

var mapiCalendarConverted = await emailApi.GetCalendarFileAsMapiModelAsync(

    new GetCalendarFileAsMapiModelRequest(icsStream));

Assert.AreEqual(mapiCalendar.Location, mapiCalendarConverted.Location);

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

byte[] ics = api.convertMapiCalendarModelToFile(

    new ConvertMapiCalendarModelToFileRequestData(

        "Ics", mapiCalendar));

String calendarContent = new String(ics, "UTF-8");

assert calendarContent.contains(mapiCalendar.getLocation());

MapiCalendarDto mapiCalendarConverted = api.getCalendarFileAsMapiModel(

    new GetCalendarFileAsMapiModelRequestData(ics));

assert mapiCalendar.getLocation().equals(mapiCalendarConverted.getLocation());

```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java

const icsFile = await api.convertMapiCalendarModelToFile(

    new requests.ConvertMapiCalendarModelToFileRequest('Ics', mapiCalendarDto));

const icsString = icsFile.body.toString();

expect(icsString).to.contain(mapiCalendarDto.location);

const mapiCalendarDtoConverted = await api.getCalendarFileAsMapiModel(

    new requests.GetCalendarFileAsMapiModelRequest(icsFile.body));

expect(mapiCalendarDto.location).to.be.eq(mapiCalendarDtoConverted.body.location);

```

{{< /tab >}}

{{< tab tabNum="4" >}}

```java

ics\_file = email.convert\_mapi\_calendar\_model\_to\_file(

    requests.ConvertMapiCalendarModelToFileRequest('Ics', mapi\_calendar))

with open(ics\_file, 'r') as f:

    file\_data = f.read()

    assert mapi\_calendar.location in file\_data

mapi\_calendar\_converted = email.get\_calendar\_file\_as\_mapi\_model(

    requests.GetCalendarFileAsMapiModelRequest(ics\_file))

assert mapi\_calendar.location == mapi\_calendar\_converted.location

```

{{< /tab >}}

{{< tab tabNum="5" >}}

```java

ics\_file = @api.convert\_mapi\_calendar\_model\_to\_file(

  ConvertMapiCalendarModelToFileRequestData.new('Ics', mapi\_calendar))

ics\_content = IO.read(ics\_file)

expect(ics\_content).to include mapi\_calendar.location

mapi\_calendar\_converted = @api.get\_calendar\_file\_as\_mapi\_model(

  GetCalendarFileAsMapiModelRequestData.new(ics\_file))

expect(mapi\_calendar.location).to eq mapi\_calendar\_converted.location

```

{{< /tab >}}

{{< tab tabNum="6" >}}

```java

$ics = $api->convertMapiCalendarModelToFile(

    new ConvertMapiCalendarModelToFileRequest(

        "Ics",

        $mapiCalendar

    )

);

$fileContent = $ics->fread($ics->getSize());

$this->assertRegExp("/" . $mapiCalendar->getLocation() . "/", $fileContent);

$mapiCalendarConverted = $api->getCalendarFileAsMapiModel(

    new GetCalendarFileAsMapiModelRequest($ics)

);

$this->assertEquals($mapiCalendar->getLocation(), $mapiCalendarConverted->getLocation());

```

{{< /tab >}}

{{< /tabs >}}
#### **MapiCalendarDto and Cloud Storage**
**How to Work with MapiCalendarDto and Cloud Storage:**

{{< tabs tabTotal="6" tabID="80" tabName1="C#" tabName2="Java" tabName3="Typescript" tabName4="Python" tabName5="Ruby" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```java

var storageName = "First Storage";

var folder = "a/folder/on/a/storage";

var fileName = "fileName.msg";



await emailApi.SaveMapiCalendarModelAsync(

    new SaveMapiCalendarModelRequest(

        fileName, "Msg", new StorageModelRqOfMapiCalendarDto(

            mapiCalendar, new StorageFolderLocation(storageName, folder))));

var mapiCalendarFromStorage = await emailApi.GetMapiCalendarModelAsync(

    new GetMapiCalendarModelRequest(

        fileName, folder, storageName));

Assert.AreEqual(mapiCalendar.Location, mapiCalendarFromStorage.Location);

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

String storage = "First Storage";

String folder = "a/folder/on/a/storage";

String fileName = "fileName.msg";

api.saveMapiCalendarModel(

    new SaveMapiCalendarModelRequestData(

        fileName, "Msg", new StorageModelRqOfMapiCalendarDto(

        mapiCalendar, new StorageFolderLocation(storage, folder))));

MapiCalendarDto mapiCalendarFromStorage = api.getMapiCalendarModel(

    new GetMapiCalendarModelRequestData(

        fileName, folder, storage));

assert mapiCalendar.getLocation().equals(mapiCalendarFromStorage.getLocation());

```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java

const storage = "First Storage";

const folder = "a/folder/on/a/storage";

const fileName = "fileName.msg";


await api.saveMapiCalendarModel(

    new requests.SaveMapiCalendarModelRequest(fileName, "Msg",

        new models.StorageModelRqOfMapiCalendarDto(

            mapiCalendarDto,

            new models.StorageFolderLocation(storage, folder))));

const mapiCalendarFromStorage = await api().getMapiCalendarModel(

    new requests.GetMapiCalendarModelRequest(fileName, folder, storage));

expect(mapiCalendarDto.location).to.be.eq(mapiCalendarFromStorage.body.location);

```

{{< /tab >}}

{{< tab tabNum="4" >}}

```java

storage = "First Storage"

folder = "a/folder/on/a/storage"

file\_name = "fileName.msg"



email.save\_mapi\_calendar\_model(

    requests.SaveMapiCalendarModelRequest(

        file\_name, 'Msg',

        models.StorageModelRqOfMapiCalendarDto(

            mapi\_calendar,

            models.StorageFolderLocation(storage, folder))))

mapi\_calendar\_from\_storage = email.get\_mapi\_calendar\_model(

    requests.GetMapiCalendarModelRequest(file\_name, folder, storage))

assert mapi\_calendar.location == mapi\_calendar\_from\_storage.location

```

{{< /tab >}}

{{< tab tabNum="5" >}}

```java

storage = 'First Storage'

folder = 'a/folder/on/a/storage'

file\_name = 'fileName.msg'

@api.save\_mapi\_calendar\_model(

  SaveMapiCalendarModelRequestData.new(

    file\_name, 'Msg',

    StorageModelRqOfMapiCalendarDto.new(

      mapi\_calendar,

      StorageFolderLocation.new(storage, folder))))

mapi\_calendar\_from\_storage = @api.get\_mapi\_calendar\_model(

  GetMapiCalendarModelRequestData.new(file\_name, @folder, @storage))

expect(mapi\_calendar.location).to eq mapi\_calendar\_from\_storage.location

```

{{< /tab >}}

{{< tab tabNum="6" >}}

```java

$storage = "First Storage";

$folder = "a/folder/on/a/storage";

$fileName = "fileName.msg";


$api->saveMapiCalendarModel(

    new SaveMapiCalendarModelRequest(

        $fileName,

        "Msg",

        new StorageModelRqOfMapiCalendarDto(

            $mapiCalendar,

            new StorageFolderLocation($storage, $folder)

        )

    )

);

$mapiCalendarFromStorage = $api->getMapiCalendarModel(

    new GetMapiCalendarModelRequest(

        $fileName,

        $folder,

        $storage

    )

);

$this->assertEquals($mapiCalendar->getLocation(), $mapiCalendarFromStorage->getLocation());

```

{{< /tab >}}

{{< /tabs >}}
## **More Tutorials**
Take a look at other tutorials, you may find answers on your questions there:
