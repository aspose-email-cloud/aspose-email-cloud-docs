---
title: "ClientMessageAppendRequest"
type: docs
url: /reference-model-client-message-append-request/
weight: 1
---
Email client append message request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Folder** | **string** | Path to folder on email server to append message to.              | [optional] 
**Message** | [**MailMessageBase**](/email/reference-model-mail-message-base/) | Message to append.              | 
**MarkAsSent** | **bool?** | Determines that appended message should be market as sent or not.              | 

Parent class: [ClientAccountBaseRequest](/email/reference-model-client-account-base-request/)

## Example

{{< tabs tabTotal="6" tabID="client_message_append_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var clientMessageAppendRequest = new ClientMessageAppendRequest
{
    Folder = "INBOX/SubFolder",
    Message = new MailMessageDto
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
    },
    MarkAsSent = true,
    AccountLocation = new StorageFileLocation
    {
        FileName = "email.account",
        Storage = "First Storage",
        FolderPath = "file/location/folder/on/storage"
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientMessageAppendRequest clientMessageAppendRequest = Models.clientMessageAppendRequest()
    .folder("INBOX/SubFolder")
    .message(Models.mailMessageDto()
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
        .build())
    .markAsSent(true)
    .accountLocation(Models.storageFileLocation()
        .fileName("email.account")
        .storage("First Storage")
        .folderPath("file/location/folder/on/storage")
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
client_message_append_request = models.ClientMessageAppendRequest(
    folder='INBOX/SubFolder',
    message=models.MailMessageDto(
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
                    address='to@aspose.com')])),
    mark_as_sent=True,
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
client_message_append_request = ClientMessageAppendRequest.new(
  folder: 'INBOX/SubFolder',
  message: MailMessageDto.new(
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
          address: 'to@aspose.com')])),
  mark_as_sent: true,
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let clientMessageAppendRequest = Models.clientMessageAppendRequest()
    .folder('INBOX/SubFolder')
    .message(Models.mailMessageDto()
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
        .build())
    .markAsSent(true)
    .accountLocation(Models.storageFileLocation()
        .fileName('email.account')
        .storage('First Storage')
        .folderPath('file/location/folder/on/storage')
        .build())
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$clientMessageAppendRequest = Models::clientMessageAppendRequest()
    ->folder('INBOX/SubFolder')
    ->message(Models::mailMessageDto()
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
        ->build())
    ->markAsSent(true)
    ->accountLocation(Models::storageFileLocation()
        ->fileName('email.account')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

