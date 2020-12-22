---
title: "Email"
type: docs
url: /reference-email-api/
weight: 1
---

Email document (*.eml) operations.



## AsFile

Converts Email model to a specified format and returns as a file. 
Returns a **File**. Requires:

{{< expand-list title="request" >}}

Email model and format to convert. Type: [**EmailAsFileRequest**](/email/reference-model-email-as-file-request/).

{{< tabs tabTotal="6" tabID="email_as_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailAsFileRequest
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
EmailAsFileRequest request = Models.emailAsFileRequest()
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
request = models.EmailAsFileRequest(
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
request = EmailAsFileRequest.new(
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
let request = Models.emailAsFileRequest()
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
$request = Models::emailAsFileRequest()
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

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="email_as_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Email.AsFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.email().asFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.email.as_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.email.as_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.email.asFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->email()->asFile($request);
```

{{< /tab >}}

{{< /tabs >}}
## AsMapi

Converts EmailDto to MapiMessageDto. 
Returns [**MapiMessageDto**](/email/reference-model-mapi-message-dto/) model. Requires:

{{< expand-list title="emailDto" >}}

Email model to convert. Type: [**EmailDto**](/email/reference-model-email-dto/).

{{< tabs tabTotal="6" tabID="email_as_mapi_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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
$email_dto = Models::emailDto()
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

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="email_as_mapi_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Email.AsMapiAsync(emailDto);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MapiMessageDto result = api.email().asMapi(emailDto);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.email.as_mapi(email_dto)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.email.as_mapi(email_dto)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.email.asMapi(emailDto);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->email()->asMapi($email_dto);
```

{{< /tab >}}

{{< /tabs >}}
## Convert

Converts email document to specified format and returns as file.


Email documents could be stored in different formats including EML, and Outlook MSG formats.
Also sometimes users need to convert email messages to HTML format, to view them in a web browser.

     
Returns a **File**. Requires:

{{< expand-list title="request" >}}

Convert method request. Type: [**EmailConvertRequest**](/email/reference-model-email-convert-request/).

{{< tabs tabTotal="6" tabID="email_convert_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailConvertRequest
{ 
    FromFormat = "Msg",
    ToFormat = "Mhtml",
    File = new MemoryStream(File.ReadAllBytes("/path/to/message.msg"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailConvertRequest request = Models.emailConvertRequest()
    .fromFormat("Msg")
    .toFormat("Mhtml")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/message.msg")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailConvertRequest(
    from_format='Msg',
    to_format='Mhtml',
    file='/path/to/message.msg')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailConvertRequest.new(
    from_format: 'Msg',
    to_format: 'Mhtml',
    file: File.new('/path/to/message.msg'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.EmailConvertRequest()
    .fromFormat('Msg')
    .toFormat('Mhtml')
    .file(fs.readFileSync('/path/to/message.msg'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::EmailConvertRequest()
    ->from_format('Msg')
    ->to_format('Mhtml')
    ->file(new SplFileObject('/path/to/message.msg'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="email_convert_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Email.ConvertAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.email().convert(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.email.convert(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.email.convert(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.email.convert(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->email()->convert($request);
```

{{< /tab >}}

{{< /tabs >}}
## FromFile

Converts email document to a model representation. 
Returns [**EmailDto**](/email/reference-model-email-dto/) model. Requires:

{{< expand-list title="request" >}}

FromFile method request. Type: [**EmailFromFileRequest**](/email/reference-model-email-from-file-request/).

{{< tabs tabTotal="6" tabID="email_from_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailFromFileRequest
{ 
    Format = "Eml",
    File = new MemoryStream(File.ReadAllBytes("/path/to/message.eml"))
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailFromFileRequest request = Models.emailFromFileRequest()
    .format("Eml")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/message.eml")))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailFromFileRequest(
    format='Eml',
    file='/path/to/message.eml')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailFromFileRequest.new(
    format: 'Eml',
    file: File.new('/path/to/message.eml'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.EmailFromFileRequest()
    .format('Eml')
    .file(fs.readFileSync('/path/to/message.eml'))
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::EmailFromFileRequest()
    ->format('Eml')
    ->file(new SplFileObject('/path/to/message.eml'))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="email_from_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Email.FromFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailDto result = api.email().fromFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.email.from_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.email.from_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.email.fromFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->email()->fromFile($request);
```

{{< /tab >}}

{{< /tabs >}}
## Get

Get email document from storage. 
Returns [**EmailDto**](/email/reference-model-email-dto/) model. Requires:

{{< expand-list title="request" >}}

Get method request. Type: [**EmailGetRequest**](/email/reference-model-email-get-request/).

{{< tabs tabTotal="6" tabID="email_get_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailGetRequest
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
EmailGetRequest request = Models.emailGetRequest()
    .format("Eml")
    .fileName("email.eml")
    .folder("folder/on/storage")
    .storage("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailGetRequest(
    format='Eml',
    file_name='email.eml',
    folder='folder/on/storage',
    storage='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailGetRequest.new(
    format: 'Eml',
    file_name: 'email.eml',
    folder: 'folder/on/storage',
    storage: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.EmailGetRequest()
    .format('Eml')
    .fileName('email.eml')
    .folder('folder/on/storage')
    .storage('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::EmailGetRequest()
    ->format('Eml')
    ->file_name('email.eml')
    ->folder('folder/on/storage')
    ->storage('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="email_get_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Email.GetAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailDto result = api.email().get(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.email.get(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.email.get(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.email.get(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->email()->get($request);
```

{{< /tab >}}

{{< /tabs >}}
## GetAsFile

Converts email document from storage to specified format and returns as file. 
Returns a **File**. Requires:

{{< expand-list title="request" >}}

GetAsFile method request. Type: [**EmailGetAsFileRequest**](/email/reference-model-email-get-as-file-request/).

{{< tabs tabTotal="6" tabID="email_get_as_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailGetAsFileRequest
{ 
    FileName = "email.eml",
    Format = "Mhtml",
    Storage = "First Storage",
    Folder = "folder/on/storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailGetAsFileRequest request = Models.emailGetAsFileRequest()
    .fileName("email.eml")
    .format("Mhtml")
    .storage("First Storage")
    .folder("folder/on/storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailGetAsFileRequest(
    file_name='email.eml',
    format='Mhtml',
    storage='First Storage',
    folder='folder/on/storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailGetAsFileRequest.new(
    file_name: 'email.eml',
    format: 'Mhtml',
    storage: 'First Storage',
    folder: 'folder/on/storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.EmailGetAsFileRequest()
    .fileName('email.eml')
    .format('Mhtml')
    .storage('First Storage')
    .folder('folder/on/storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::EmailGetAsFileRequest()
    ->file_name('email.eml')
    ->format('Mhtml')
    ->storage('First Storage')
    ->folder('folder/on/storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="email_get_as_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Email.GetAsFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.email().getAsFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.email.get_as_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.email.get_as_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.email.getAsFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->email()->getAsFile($request);
```

{{< /tab >}}

{{< /tabs >}}
## GetList

Get email list from storage folder. 
Returns [**EmailStorageList**](/email/reference-model-email-storage-list/) model. Requires:

{{< expand-list title="request" >}}

GetList method request. Type: [**EmailGetListRequest**](/email/reference-model-email-get-list-request/).

{{< tabs tabTotal="6" tabID="email_get_list_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailGetListRequest
{ 
    Format = "Eml",
    Folder = "folder/on/storage",
    Storage = "First Storage",
    ItemsPerPage = 10,
    PageNumber = 0
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailGetListRequest request = Models.emailGetListRequest()
    .format("Eml")
    .folder("folder/on/storage")
    .storage("First Storage")
    .itemsPerPage(10)
    .pageNumber(0)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailGetListRequest(
    format='Eml',
    folder='folder/on/storage',
    storage='First Storage',
    items_per_page=10,
    page_number=0)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailGetListRequest.new(
    format: 'Eml',
    folder: 'folder/on/storage',
    storage: 'First Storage',
    items_per_page: 10,
    page_number: 0)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.EmailGetListRequest()
    .format('Eml')
    .folder('folder/on/storage')
    .storage('First Storage')
    .itemsPerPage(10)
    .pageNumber(0)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::EmailGetListRequest()
    ->format('Eml')
    ->folder('folder/on/storage')
    ->storage('First Storage')
    ->items_per_page(10)
    ->page_number(0)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="email_get_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Email.GetListAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailStorageList result = api.email().getList(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.email.get_list(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.email.get_list(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.email.getList(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->email()->getList($request);
```

{{< /tab >}}

{{< /tabs >}}
## Save

Save email document to storage. Requires:

{{< expand-list title="request" >}}

Email document create/update request. Type: [**EmailSaveRequest**](/email/reference-model-email-save-request/).

{{< tabs tabTotal="6" tabID="email_save_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new EmailSaveRequest
{
    Format = "Msg",
    StorageFile = new StorageFileLocation
    {
        FileName = "email.eml",
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
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailSaveRequest request = Models.emailSaveRequest()
    .format("Msg")
    .storageFile(Models.storageFileLocation()
        .fileName("email.eml")
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
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.EmailSaveRequest(
    format='Msg',
    storage_file=models.StorageFileLocation(
        file_name='email.eml',
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
                address='to@aspose.com')]))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = EmailSaveRequest.new(
  format: 'Msg',
  storage_file: StorageFileLocation.new(
    file_name: 'email.eml',
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
        address: 'to@aspose.com')]))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.emailSaveRequest()
    .format('Msg')
    .storageFile(Models.storageFileLocation()
        .fileName('email.eml')
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
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::emailSaveRequest()
    ->format('Msg')
    ->storageFile(Models::storageFileLocation()
        ->fileName('email.eml')
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
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="email_save_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Email.SaveAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.email().save(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.email.save(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.email.save(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.email.save(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->email()->save($request);
```

{{< /tab >}}

{{< /tabs >}}

## More APIs

{{< list-of-articles-in-this-section >}}
