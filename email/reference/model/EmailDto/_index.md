---
title: "EmailDto"
type: docs
url: /reference-model-email-dto/
weight: 1
---
Email message representation.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**AlternateViews** | [**List&lt;AlternateView&gt;**](/email/reference-model-alternate-view/) | Collection of alternate views of message.              | [optional] 
**Attachments** | [**List&lt;Attachment&gt;**](/email/reference-model-attachment/) | Email message attachments.              | [optional] 
**Bcc** | [**List&lt;MailAddress&gt;**](/email/reference-model-mail-address/) | BCC recipients.              | [optional] 
**Body** | **string** | Email message body as plain text.              | [optional] 
**BodyEncoding** | **string** | Body encoding.              | [optional] 
**BodyType** | **string** | The content type of message body. Enum, available values: PlainText, Html, Rtf | 
**Cc** | [**List&lt;MailAddress&gt;**](/email/reference-model-mail-address/) | CC recipients.              | [optional] 
**Date** | **DateTime?** | Message date.              | 
**DeliveryNotificationOptions** | **List&lt;string&gt;** | Delivery notifications. Items: Email delivery notification options. Enum, available values: Delay, Never, None, OnFailure, OnSuccess | [optional] 
**From** | [**MailAddress**](/email/reference-model-mail-address/) | From address.              | [optional] 
**Headers** | **Dictionary&lt;string, string&gt;** | Document headers.              | [optional] 
**HtmlBody** | **string** | HTML body.              | [optional] 
**HtmlBodyText** | **string** | Html body as plain text. Read only.              | [optional] 
**IsBodyHtml** | **bool?** | Indicates whether the message body is in Html.              | 
**IsDraft** | **bool?** | Indicates whether or not a message has been sent.              | 
**IsEncrypted** | **bool?** | Indicates whether the message is encrypted. Read only.              | 
**IsSigned** | **bool?** | Indicates whether the message is signed. Read only.              | 
**LinkedResources** | [**List&lt;LinkedResource&gt;**](/email/reference-model-linked-resource/) | Linked resources of message.              | [optional] 
**MessageId** | **string** | Message id.              | [optional] 
**OriginalIsTnef** | **bool?** | Indicates whether original EML message is in TNEF format. Read only.              | 
**PreferredTextEncoding** | **string** | Preferred encoding.              | [optional] 
**Priority** | **string** | Email priority status. Enum, available values: High, Low, Normal | 
**ReadReceiptTo** | [**List&lt;MailAddress&gt;**](/email/reference-model-mail-address/) | Read receipt addresses.              | [optional] 
**ReplyToList** | [**List&lt;MailAddress&gt;**](/email/reference-model-mail-address/) | The list of addresses to reply to for the mail message.              | [optional] 
**ReversePath** | [**MailAddress**](/email/reference-model-mail-address/) | ReversePath address.              | [optional] 
**Sender** | [**MailAddress**](/email/reference-model-mail-address/) | Sender address.              | [optional] 
**Sensitivity** | **string** | Specifies the sensitivity of a MailMessage. Enum, available values: None, Normal, Personal, Private, CompanyConfidential | 
**Subject** | **string** | Message subject.              | [optional] 
**SubjectEncoding** | **string** | Subject encoding.              | [optional] 
**TimeZoneOffset** | **long?** | Coordinated Universal Time (UTC) offset for the message dates. This property defines the time zone difference, between the local time and UTC represented as count of ticks (10 000 per millisecond).              | [optional] 
**To** | [**List&lt;MailAddress&gt;**](/email/reference-model-mail-address/) | The address collection that contains the recipients of message.              | [optional] 
**XMailer** | **string** | The X-Mailer the software that created the e-mail message.              | [optional] 


## Example

{{< tabs tabTotal="6" tabID="email_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var emailDto = new EmailDto
{
    Attachments = new List<Attachment>
    {
        new Attachment
        {
            Name = "some-file.txt",
            Base64Data = "U29tZSBmaWxlIGNvbnRlbnQ="
        }
    },
    Body = "Some body",
    BodyType = "Html",
    DeliveryNotificationOptions = new List<EmailDeliveryNotificationOptions>
    {
        "OnSuccess",
        "Delay"
    },
    From = new MailAddress
    {
        DisplayName = "From Address",
        Address = "from@aspose.com"
    },
    HtmlBody = "<b>Some body</b>",
    IsBodyHtml = true,
    IsDraft = true,
    Subject = "Re: Some subject",
    To = new List<MailAddress>
    {
        new MailAddress
        {
            DisplayName = "To Address",
            Address = "to@aspose.com"
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailDto emailDto = Models.emailDto()
    .attachments(Arrays.<Attachment>asList(
        Models.attachment()
            .name("some-file.txt")
            .base64Data("U29tZSBmaWxlIGNvbnRlbnQ=")
            .build()))
    .body("Some body")
    .bodyType("Html")
    .deliveryNotificationOptions(Arrays.<EmailDeliveryNotificationOptions>asList(
        "OnSuccess",
        "Delay"))
    .from(Models.mailAddress()
        .displayName("From Address")
        .address("from@aspose.com")
        .build())
    .htmlBody("<b>Some body</b>")
    .isBodyHtml(true)
    .isDraft(true)
    .subject("Re: Some subject")
    .to(Arrays.<MailAddress>asList(
        Models.mailAddress()
            .displayName("To Address")
            .address("to@aspose.com")
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
email_dto = models.EmailDto(
    attachments=[
        models.Attachment(
            name='some-file.txt',
            base64_data='U29tZSBmaWxlIGNvbnRlbnQ=')],
    body='Some body',
    body_type='Html',
    delivery_notification_options=[
        'OnSuccess',
        'Delay'],
    _from=models.MailAddress(
        display_name='From Address',
        address='from@aspose.com'),
    html_body='<b>Some body</b>',
    is_body_html=True,
    is_draft=True,
    subject='Re: Some subject',
    to=[
        models.MailAddress(
            display_name='To Address',
            address='to@aspose.com')])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
email_dto = EmailDto.new(
  attachments: [
    Attachment.new(
      name: 'some-file.txt',
      base64_data: 'U29tZSBmaWxlIGNvbnRlbnQ=')],
  body: 'Some body',
  body_type: 'Html',
  delivery_notification_options: [
    'OnSuccess',
    'Delay'],
  from: MailAddress.new(
    display_name: 'From Address',
    address: 'from@aspose.com'),
  html_body: '<b>Some body</b>',
  is_body_html: true,
  is_draft: true,
  subject: 'Re: Some subject',
  to: [
    MailAddress.new(
      display_name: 'To Address',
      address: 'to@aspose.com')])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let emailDto = Models.emailDto()
    .attachments([
        Models.attachment()
            .name('some-file.txt')
            .base64Data('U29tZSBmaWxlIGNvbnRlbnQ=')
            .build()])
    .body('Some body')
    .bodyType('Html')
    .deliveryNotificationOptions([
        'OnSuccess',
        'Delay'])
    .from(Models.mailAddress()
        .displayName('From Address')
        .address('from@aspose.com')
        .build())
    .htmlBody('<b>Some body</b>')
    .isBodyHtml(true)
    .isDraft(true)
    .subject('Re: Some subject')
    .to([
        Models.mailAddress()
            .displayName('To Address')
            .address('to@aspose.com')
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$emailDto = Models::emailDto()
    ->attachments(array(
        Models::attachment()
            ->name('some-file.txt')
            ->base64Data('U29tZSBmaWxlIGNvbnRlbnQ=')
            ->build()))
    ->body('Some body')
    ->bodyType('Html')
    ->deliveryNotificationOptions(array(
        'OnSuccess',
        'Delay'))
    ->from(Models::mailAddress()
        ->displayName('From Address')
        ->address('from@aspose.com')
        ->build())
    ->htmlBody('<b>Some body</b>')
    ->isBodyHtml(true)
    ->isDraft(true)
    ->subject('Re: Some subject')
    ->to(array(
        Models::mailAddress()
            ->displayName('To Address')
            ->address('to@aspose.com')
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

