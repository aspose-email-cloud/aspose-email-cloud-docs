---
title: "Message"
type: docs
url: /reference-mapi-message-api/
weight: 1
---

MAPI message operations



## AsEmailDto

Converts MAPI message model to EmailDto model. 
Returns [**EmailDto**](/email/reference-model-email-dto/) model. Requires:

{{< expand-list title="mapiMessage" >}}

MAPI message model to convert. Type: [**MapiMessageDto**](/email/reference-model-mapi-message-dto/).

{{< tabs tabTotal="6" tabID="mapi_message_as_email_dto_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var mapiMessage = new MapiMessageDto
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
MapiMessageDto mapiMessage = Models.mapiMessageDto()
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
mapi_message = models.MapiMessageDto(
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
mapi_message = MapiMessageDto.new(
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
let mapiMessage = Models.mapiMessageDto()
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
$mapi_message = Models::mapiMessageDto()
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

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="mapi_message_as_email_dto_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Mapi.Message.AsEmailDtoAsync(mapiMessage);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailDto result = api.mapi().message().asEmailDto(mapiMessage);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.mapi.message.as_email_dto(mapi_message)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.mapi.message.as_email_dto(mapi_message)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.mapi.message.asEmailDto(mapiMessage);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->mapi()->message()->asEmailDto($mapi_message);
```

{{< /tab >}}

{{< /tabs >}}
## AsFile

Converts MAPI message model to specified format and returns as file. 
Returns a **File**. Requires:

{{< expand-list title="request" >}}

MAPI message model to convert. Type: [**MapiMessageAsFileRequest**](/email/reference-model-mapi-message-as-file-request/).

{{< tabs tabTotal="6" tabID="mapi_message_as_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiMessageAsFileRequest
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
MapiMessageAsFileRequest request = Models.mapiMessageAsFileRequest()
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
request = models.MapiMessageAsFileRequest(
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
request = MapiMessageAsFileRequest.new(
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
let request = Models.mapiMessageAsFileRequest()
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
$request = Models::mapiMessageAsFileRequest()
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

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="mapi_message_as_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Mapi.Message.AsFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.mapi().message().asFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.mapi.message.as_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.mapi.message.as_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.mapi.message.asFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->mapi()->message()->asFile($request);
```

{{< /tab >}}

{{< /tabs >}}
## FromFile

Converts email file to a MAPI model representation. 
Returns [**MapiMessageDto**](/email/reference-model-mapi-message-dto/) model. Requires:

{{< expand-list title="request" >}}

FromFile method request. Type: [**MapiMessageFromFileRequest**](/email/reference-model-mapi-message-from-file-request/).

{{< tabs tabTotal="6" tabID="mapi_message_from_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiMessageFromFileRequest
{ 
    Format = "Msg",
    File = new MemoryStream(File.ReadAllBytes("/path/to/message.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiMessageFromFileRequest request = Models.mapiMessageFromFileRequest()
    .format("Msg")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/message.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MapiMessageFromFileRequest(
    format='Msg',
    file='/path/to/message.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MapiMessageFromFileRequest.new(
    format: 'Msg',
    file: File.new('/path/to/message.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.MapiMessageFromFileRequest()
    .format('Msg')
    .file(fs.readFileSync('/path/to/message.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::MapiMessageFromFileRequest()
    ->format('Msg')
    ->file(new SplFileObject('/path/to/message.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="mapi_message_from_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Mapi.Message.FromFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiMessageDto result = api.mapi().message().fromFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.mapi.message.from_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.mapi.message.from_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.mapi.message.fromFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->mapi()->message()->fromFile($request);
```

{{< /tab >}}

{{< /tabs >}}
## Get

Get MAPI message document. 
Returns [**MapiMessageDto**](/email/reference-model-mapi-message-dto/) model. Requires:

{{< expand-list title="request" >}}

Get method request. Type: [**MapiMessageGetRequest**](/email/reference-model-mapi-message-get-request/).

{{< tabs tabTotal="6" tabID="mapi_message_get_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiMessageGetRequest
{ 
    Format = "Eml",
    FileName = "email.eml",
    Folder = "folder/on/storage",
    Storage = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiMessageGetRequest request = Models.mapiMessageGetRequest()
    .format("Eml")
    .fileName("email.eml")
    .folder("folder/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MapiMessageGetRequest(
    format='Eml',
    file_name='email.eml',
    folder='folder/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MapiMessageGetRequest.new(
    format: 'Eml',
    file_name: 'email.eml',
    folder: 'folder/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.MapiMessageGetRequest()
    .format('Eml')
    .fileName('email.eml')
    .folder('folder/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::MapiMessageGetRequest()
    ->format('Eml')
    ->file_name('email.eml')
    ->folder('folder/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="mapi_message_get_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Mapi.Message.GetAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiMessageDto result = api.mapi().message().get(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.mapi.message.get(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.mapi.message.get(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.mapi.message.get(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->mapi()->message()->get($request);
```

{{< /tab >}}

{{< /tabs >}}
## Save

Save MAPI message to storage. Requires:

{{< expand-list title="request" >}}

Message create/update request. Type: [**MapiMessageSaveRequest**](/email/reference-model-mapi-message-save-request/).

{{< tabs tabTotal="6" tabID="mapi_message_save_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MapiMessageSaveRequest
{
    Format = "Msg",
    StorageFile = new StorageFileLocation
    {
        FileName = "message.msg",
        Storage = "First Storage",
        FolderPath = "file/location/folder/on/storage"
    },
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
MapiMessageSaveRequest request = Models.mapiMessageSaveRequest()
    .format("Msg")
    .storageFile(Models.storageFileLocation()
        .fileName("message.msg")
        .storage("First Storage")
        .folderPath("file/location/folder/on/storage")
        .build())
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
request = models.MapiMessageSaveRequest(
    format='Msg',
    storage_file=models.StorageFileLocation(
        file_name='message.msg',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'),
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
request = MapiMessageSaveRequest.new(
  format: 'Msg',
  storage_file: StorageFileLocation.new(
    file_name: 'message.msg',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'),
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
let request = Models.mapiMessageSaveRequest()
    .format('Msg')
    .storageFile(Models.storageFileLocation()
        .fileName('message.msg')
        .storage('First Storage')
        .folderPath('file/location/folder/on/storage')
        .build())
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
$request = Models::mapiMessageSaveRequest()
    ->format('Msg')
    ->storageFile(Models::storageFileLocation()
        ->fileName('message.msg')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
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

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="mapi_message_save_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Mapi.Message.SaveAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.mapi().message().save(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.mapi.message.save(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.mapi.message.save(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.mapi.message.save(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->mapi()->message()->save($request);
```

{{< /tab >}}

{{< /tabs >}}

## More APIs

{{< list-of-articles-in-this-section >}}
