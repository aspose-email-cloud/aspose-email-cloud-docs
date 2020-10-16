---
title: "EmailAsFileRequest"
type: docs
url: /reference-model-email-as-file-request/
weight: 1
---
Convert email model to file request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Format** | **string** | Email document format. Enum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft | 
**Value** | [**EmailDto**](/email/reference-model-email-dto/) | Email model.              | 


## Example

{{< tabs tabTotal="6" tabID="email_as_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var emailAsFileRequest = new EmailAsFileRequest
{
    Value = new EmailDto
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
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailAsFileRequest emailAsFileRequest = Models.emailAsFileRequest()
    .value(Models.emailDto()
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
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
email_as_file_request = models.EmailAsFileRequest(
    value=models.EmailDto(
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
                address='to@aspose.com')]))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
email_as_file_request = EmailAsFileRequest.new(
  value: EmailDto.new(
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
        address: 'to@aspose.com')]))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let emailAsFileRequest = Models.emailAsFileRequest()
    .value(Models.emailDto()
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
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$emailAsFileRequest = Models::emailAsFileRequest()
    ->value(Models::emailDto()
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
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

