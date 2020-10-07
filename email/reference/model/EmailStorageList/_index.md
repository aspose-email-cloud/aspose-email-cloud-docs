---
title: "EmailStorageList"
type: docs
url: /reference-model-email-storage-list/
weight: 1
---
Email models list with corresponding storage locations.             

Properties:

Class has no properties

Parent class: [ListResponseOfStorageModelOfEmailDto](/email/reference-model-list-response-of-storage-model-of-email-dto/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="email_storage_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var emailStorageList = new EmailStorageList
{
    Value = new List<StorageModelOfEmailDto>
    {
        new EmailSaveRequest
        {
            StorageFile = new StorageFileLocation
            {
                FileName = "message.eml",
                Storage = "First Storage",
                FolderPath = "file/location/folder/on/storage"
            },
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
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailStorageList emailStorageList = Models.emailStorageList()
    .value(Arrays.<StorageModelOfEmailDto>asList(
        Models.emailSaveRequest()
            .storageFile(Models.storageFileLocation()
                .fileName("message.eml")
                .storage("First Storage")
                .folderPath("file/location/folder/on/storage")
                .build())
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
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
email_storage_list = models.EmailStorageList(
    value=[
        models.EmailSaveRequest(
            storage_file=models.StorageFileLocation(
                file_name='message.eml',
                storage='First Storage',
                folder_path='file/location/folder/on/storage'),
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
                        address='to@aspose.com')]))])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
email_storage_list = EmailStorageList.new(
  value: [
    EmailSaveRequest.new(
      storage_file: StorageFileLocation.new(
        file_name: 'message.eml',
        storage: 'First Storage',
        folder_path: 'file/location/folder/on/storage'),
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
            address: 'to@aspose.com')]))])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let emailStorageList = Models.emailStorageList()
    .value([
        Models.emailSaveRequest()
            .storageFile(Models.storageFileLocation()
                .fileName('message.eml')
                .storage('First Storage')
                .folderPath('file/location/folder/on/storage')
                .build())
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
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$emailStorageList = Models::emailStorageList()
    ->value(array(
        Models::emailSaveRequest()
            ->storageFile(Models::storageFileLocation()
                ->fileName('message.eml')
                ->storage('First Storage')
                ->folderPath('file/location/folder/on/storage')
                ->build())
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
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

