---
title: "Email Message Files"
type: docs
url: /email-message-files/
description: " Aspose Email tutorial shows how to work with email files. Create emails, save emails, edit emails, send emails, receive emails and more."
weight: 20
---

## **How to Work With Email Message Files via Aspose.Email Cloud API**
[Aspose.Email Cloud API](https://products.aspose.cloud/email/family) supports email message files with EML, MSG, MHTML and HTML format. We have API for creating, editing, converting such files. Also, email message files can be used in the [built-in email client](/email-client/).

Our SDKs support two different ways of operating with email message files using MapiMessageDto and EmailDto. This tutorial shows how to use an **EmailDto**.

{{% alert color="primary" %}} To see how to setup SDKs use the [SDK setup tutorial](/sdk-setup/). {{% /alert %}} 
## **Email Message Files**
Simply put, email message files are the files using to exchanging messages between people using electronic devices. Sounds simple, isn’t it? 

You may already know this. In our time, it’s hard to find a person who doesn't use email message. We use emails everywhere at our work, in a friendly conversation, etc.

There are many ways to send and retrieve emails, so, there are many file formats for these purposes.

Let's find out which email formats exist:

- [**EML**](https://wiki.fileformat.com/email/eml/) — using in Microsoft Outlook Express as well as some other email programs. An email message saved to a file in the MIME RFC 822 standard format. **EML** files usually contain plain ASCII text for the main message body, headers and hyperlinks and attachments.
- [**MSG**](https://wiki.fileformat.com/email/msg/) — using in Microsoft Outlook and Exchange. An **MSG** file can contain plain ASCII text as in **EML** files.
- [**HTML**](https://wiki.fileformat.com/web/html/) — the extension for web pages created for display in browsers. The HTML file format is very convenient to display emails on the web sites. 

As we have mentioned before, email message files are using for exchanging messages. With Aspose.Email Cloud API you can easily change the email’s data, attachments and other information. The API can help you to simplify the development of your product and achieve your goals. The Cloud approach provides you with the processing power of our servers, using them you do not need to process messages on your servers, provide this to us. User-friendly API provides security and ease of development.
## **How to Create Email Object and Save It as File on Storage**
The best way to work with emails is to use **EmailDto** objects. **EmailDto** object contains all email’s data:

{{% alert color="primary" %}} 

Email’s data that is contained in EmailDto

- Collection of alternate views of the message.
- Email message attachments.
- BCC recipients.
- Message subject.
- Sender address.
- The address collection that contains the recipients of a message.
- Email message body as plain text.
- Body encoding.
- The content type of message body: PlainText, Html, Rtf.
- CC recipients.
- Message date.
- Delivery notification options.
- From address.
- Document headers.
- HTML body.
- Linked resources of a message.
- The list of addresses to reply to for the mail message.
- And other email’s data.

{{% /alert %}} 
## **Create Email File — EmailDto Object**
First, let's create an **EmailDto** object and save it as a file on the Storage.

To create an email file (EML, MSG, MHTML, HTML) you need to create [EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailDto.md) object. To initialize [EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailDto.md) object let’s define main fields: ***From*** (accepts [MailAddress](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/MailAddress.md) object which contains the email address of a sender), ***To*** (accepts List of [MailAddress](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/MailAddress.md) objects; parameter ***To*** can contain several email addresses), ***Subject*** (accepts a string with a subject of an email), ***Body*** (accepts a string with a body’s content).

After creating [EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailDto.md) object we save it to [Storage](https://dashboard.aspose.cloud/#/storages). To save it we need to choose storage and folder where we want to save our created email file. Also, we need to create a name for this email file. [EmailApi](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md) class has a function called [*SaveAsync*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#saveasync) which requires one parameter — [*EmailSaveRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailSaveRequest.md). 

[EmailSaveRequest](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailSaveRequest.md) has 3 fields:
- **Format** defines a file format.
- **Value** is an [EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailDto.md) object.
- **StorageFile** is an [StorageFileLocation](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/StorageFileLocation.md) object that defines the email file location on [Storage](https://dashboard.aspose.cloud/#/storages).

Look at the following code examples:

**How to create an EmailDto object and save it as a file on storage?**

{{< tabs tabTotal="6" tabID="1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var email = new EmailDto
{
    From = new MailAddress("From address", "organizer@aspose.com", "Accepted"),
    To = new List<MailAddress> {new MailAddress("To address", "attendee@aspose.com", null)},
    Subject = "Some subject",
    Body = "Some body"
};
var storage = "First storage";
var folder = "folder/on/storage";
var emailFile = "email.eml";
var format = "Eml";

await api.Email.SaveAsync(new EmailSaveRequest(
    new StorageFileLocation(storage, folder, emailFile), 
    email, format));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailDto email = new EmailDto()
    .from(new MailAddress("From Name", "organizer@aspose.com", null))
    .addToItem(new MailAddress("To Name", "attendee@aspose.com", null))
    .subject("Some subject")
    .body("Some body");
String emailFile = "email.eml";
String storage = "First storage";
String folder = "folder/on/storage";
String format = "Eml";

api.email().save(new EmailSaveRequest(
    new StorageFileLocation(storage, folder, emailFile),
    email, format));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
email = models.EmailDto(
    # 'from' is reserved, so from field is named '_from':
    _from=models.MailAddress('From Name', 'organizer@aspose.com'),
    to=[models.MailAddress('To Name', 'attendee@aspose.com')],
    subject='Some subject',
    body='Some body')
storage = 'First storage'
folder = 'folder/on/storage'
email_file = 'email.eml'
file_format = 'Eml'

api.email.save(models.EmailSaveRequest(
    models.StorageFileLocation(storage, folder, email_file),
    email, file_format))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
email = EmailDto.new(
  from: MailAddress.new(address: 'from@aspose.com'),
  to: [MailAddress.new(address: 'to@aspose.com')],
  subject: 'Some subject',
  body: 'Some body')
 
folder = 'folder/on/storage'
storage = 'First storage'
email_file = "email.eml"
format = "Eml"

api.email.save(
  EmailSaveRequest.new(
    storage_file: StorageFileLocation.new(
      storage: storage,
      folder_path: folder,
      file_name: email_file),
    value: email,
    format: format))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
var email = new EmailDto();
email.from = new MailAddress('From address', 'organizer@aspose.com');
email.to = [new MailAddress('To address', 'attendee@aspose.com')];
email.subject = 'Some subject';
email.body = 'Some body';
 
var storage = 'First storage';
var folder = 'folder/on/storage';
var emailFile = 'email.eml';
var format = 'Eml';

await api.email.save(new EmailSaveRequest(
    new StorageFileLocation(storage, folder, emailFile),
    email, format));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$email = (new EmailDto())
    ->setFrom(new MailAddress("Organizer Name", "organizer@aspose.com"))
    ->setTo(array(new MailAddress("Attendee Name", "attendee@aspose.com")))
    ->setSubject("Some subject")
    ->setBody("Some body");

$storage = "First storage";
$folder = "folder/on/storage"; 
$emailFile = "email.eml";
$format = "Eml";

$api->email()->save(new EmailSaveRequest(
    new StorageFileLocation($storage, $folder, $emailFile),
    $email, $format));
```

{{< /tab >}}

{{< /tabs >}}
 
  
You can edit the EmailDto object and save it again. If file name and location will be the same, the file will be overwritten.
## **How to Download Email File From Storage**
You can download files from the [Storage](https://dashboard.aspose.cloud/#/storages).

[FileApi](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/FileApi.md) class has [DownloadFileAsync](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/FileApi.md#downloadfileasync) function which allows to download files from [Storage](https://dashboard.aspose.cloud/#/storages) asynchronous as a Stream. This function has one required parameter —  [*DownloadFileRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/Model/DownloadFileRequest.cs). To define it you need to pass **2 parameters** into it: a file’s path as a string and a name of [Storage](https://dashboard.aspose.cloud/#/storages) you want to download from.

To download the file that we created in the previous step from the Storage, use the following steps:

**How to download a file from the Storage?**

{{< tabs tabTotal="6" tabID="2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var resultStream = await api.CloudStorage.File.DownloadFileAsync(
    new DownloadFileRequest($"{folder}/{emailFile}", storage));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.cloudStorage().file().downloadFile(
    new DownloadFileRequest(folder + "/" + emailFile, storage, null));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
downloaded_file_location = api.cloud_storage.file.download_file(
    models.DownloadFileRequest(folder + '/' + email_file, storage))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
downloaded_file_location = api.cloud_storage.file.download_file(
    DownloadFileRequest.new(folder + '/' + email_file, storage))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
var downloaded = await api.cloudStorage.file.downloadFile(
    new DownloadFileRequest(folder + '/' + emailFile, storage));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$downloaded = $api->cloudStorage()->file()->downloadFile(
    new DownloadFileRequest($folder.'/'.$emailFile, $storage));
$fileContent = $downloaded->fread($downloaded->getSize());
```

{{< /tab >}}

{{< /tabs >}}

**Also, you can download a file in another format.**

Aspose.Email Cloud allows you to download email messages from [Storage](https://dashboard.aspose.cloud/#/storages) in many different file formats. For example, you have an EML file, you want to download it but in MSG. You can download it immediately without separate converting.

To download email file from [Storage](https://dashboard.aspose.cloud/#/storages) you need to call [*GetAsFile*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#getasfile) function from EmailApi. [*GetAsFile*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#getasfile) accepts only one required parameter — [*EmailGetAsFileRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/Model/EmailGetAsFileRequest.cs). 

To initialize [*EmailGetAsFileRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/Model/EmailGetAsFileRequest.cs) you need to pass **4 parameters** into it: a name of an email file on [Storage](https://dashboard.aspose.cloud/#/storages) as a string, a result file’s extension as an Enum (EML, MSG, MsgUnicode, MHTML, HTML), storage’s name as a string and a path to a folder on [Storage](https://dashboard.aspose.cloud/#/storages) where email file is.

If you do everything right you will get the email file as a Stream.

**How to download a file from the Storage in a different format?**

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var file = await api.Email.GetAsFileAsync(new EmailGetAsFileRequest(
    emailFile, "Msg", storage, folder));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] file = api.email().getAsFile(new EmailGetAsFileRequest(
    emailFile, "Msg", storage, folder));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
file = api.email.get_as_file(models.EmailGetAsFileRequest(
    email_file, 'Msg', storage, folder))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
file = @api.email.get_as_file(EmailGetAsFileRequest.new(
  file_name: email_file, format: 'Msg', storage: storage, folder: folder))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
const file = await td.api().email.getAsFile(new EmailGetAsFileRequest(
    emailFile, 'Msg', storage, folder));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$file = $api->email()->getAsFile(new EmailGetAsFileRequest(
    $emailFile, 'Msg', $storage, $folder));
```

{{< /tab >}}

{{< /tabs >}}

**You can download the file as an EmailDto object:**

**EmailDto** provides you with an easier way to work with emails. It allows to change and get data from an email file in several code lines.

If you want to get an email from [Storage](https://dashboard.aspose.cloud/#/storages) as an [EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailDto.md) object — you need to use [GetAsync](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetAsync) from [EmailApi](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md). 

Unlike the previous case, here we need to pass [*EmailGetRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/Model/EmailGetRequest.cs) into [GetAsync](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetAsync). 

[*EmailGetRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/Model/EmailGetRequest.cs) accepts **2 required parameters**: an email document format as Enum (EML, MSG, MsgUnicode, MHTML, HTML), email document file name as a string; and 2 optional parameters: storage’s name as a string and a path to a folder on [Storage](https://dashboard.aspose.cloud/#/storages) where email file is as a string too.

After calling [GetAsync](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#GetAsync) you get [EmailDto](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailDto.md) object.

**How to download a file as EmailDto object?**

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var emailDto = await api.Email.GetAsync(new EmailGetRequest(
    "Eml", emailFile, folder, storage));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailDto emailDto = api.email().get(new EmailGetRequest(
    "Eml", emailFile, folder, storage));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
email_dto = api.email.get(models.EmailGetRequest(
    'Eml', email_file, folder, storage))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
email_dto = @api.email.get(EmailGetRequest.new(
  format: 'Eml', file_name: email_file, folder: folder, storage: storage))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
const emailDto = await td.api().email.get(new EmailGetRequest(
    'Eml', emailFile, folder, storage));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$emailDto = $api->email()->get(new EmailGetRequest(
    'Eml', $emailFile, $folder, $storage));
```

{{< /tab >}}

{{< /tabs >}}
## **How to Append Email Object to "INBOX" Folder of IMAP Account**
We can append this EmailDto object to the "INBOX" folder of an IMAP account:

{{% alert color="primary" %}} 

See how to setup and use email client in the [Quickstart with an email client](https://docs.aspose.cloud/display/LGIS/Quick+start+with+an+email+client)[ tutorial.](https://docs.aspose.cloud/display/LGIS/Quick+start+with+an+email+client)

{{% /alert %}} 

To append an email to the "INBOX" folder of an IMAP account, **you should create \*.account file with IMAP account credentials at first**. Then you need to call [*AppendAsync*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md#AppendAsync) function from [ClientMessageApi](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md).

[*AppendAsync*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md#AppendAsync) has only one required parameter — [*ClientMessageAppendRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageAppendRequest.md).

[*ClientMessageAppendRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageAppendRequest.md) object has 4 parameters:

1. Account location on storage represented as a [StorageFileLocation](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/StorageFileLocation.md) object.
1. Email account folder to store a message as a **string**. For example, "INBOX".
1. Mark message as sent. Nullable bool parameter.
1. Email document. In our case it should be represented as a [*MailMessageDto*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/MailMessageDto.md) object.

As a result, you will add an email from model to a specified folder in an email account. 

**How to append EmailDto object to the "INBOX" folder of an IMAP account?**

{{< tabs tabTotal="6" tabID="5" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var imapAccount = "imap.account";
var messageId = await api.Client.Message.AppendAsync(
    new ClientMessageAppendRequest(
        new StorageFileLocation(storage, folder, imapAccount),
        "INBOX",
        new MailMessageDto(emailDto),
        true));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String imapAccount = "imap.account";
ValueTOfString messageId = api.client().message().append(
    new ClientMessageAppendRequest(
        new StorageFileLocation(storage, folder, imapAccount),
        "INBOX",
        new MailMessageDto(emailDto),
        true));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
imap_account = 'imap.account'
message_id = api.client.message.append(
    models.ClientMessageAppendRequest(
        models.StorageFileLocation(storage, folder, imap_account),
        'INBOX',
        models.MailMessageDto(email_dto),
        True))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
imap_account = 'imap.account'
message_id = api.client.message.append(
  ClientMessageAppendRequest.new(
    account_location: StorageFileLocation.new(
      storage: storage,
      folder_path: folder,
      file_name: imap_account),
    folder: 'INBOX',
    message: MailMessageDto.new(email_dto),
    mark_as_sent: true))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
const imapAccount = 'imap.account';
var messageId = await api.client.message.append(
    new ClientMessageAppendRequest(
        new StorageFileLocation(storage, folder, imapAccount),
        'INBOX',
        new MailMessageDto(emailDto),
        true));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$imapAccount = 'imap.account';
$messageId = $api->client()->message()->append(
    new ClientMessageAppendRequest(
        new StorageFileLocation($storage, $folder, $imapAccount),
        'INBOX',
        new MailMessageDto($emailDto),
        true));
```

{{< /tab >}}

{{< /tabs >}}
## **How to Convert Email From One Format to Another**
If you don't want to use all these models and storages, and just want to convert email file from one format to another, use the fast and convenient Converter developed by Aspose.

To convert email file use [ConvertAsync](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md#ConvertAsync) from [EmailApi](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailApi.md). This function requires only one parameter — [*EmailConvertRequest*](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/Model/EmailConvertRequest.cs) which requests a file for converting.

It has **3 required parameters**:

1. Email file format to convert from. Possible values are: EML, MSG, MsgUnicode, MHTML, HTML.
1. Email file format to convert to.
1. File to convert as a Stream.

**How to convert an email from one format to another?**

{{< tabs tabTotal="6" tabID="6" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
using(var emlStream = File.OpenRead("email.eml"))
{
    var mapiStream = await api.Email.ConvertAsync(
        new EmailConvertRequest("Eml", "Msg", emlStream));
    //...
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] fileToConvert = IOUtils.toByteArray(
    new FileInputStream("email.eml"));
byte[] mapiBytes = api.email().convert(
    new EmailConvertRequest("Eml", "Msg", emlBytes));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
mapi = api.email.convert(
    models.EmailConvertRequest('Eml', 'Msg', 'email.eml'))
with open(mapi, 'r') as f:
    filedata = f.read()
    # ...
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
mapi_file = api.email.convert(
  EmailConvertRequest.new(
    from_format: 'Eml',
    to_format: 'Msg',
    file: File.new('email.eml')))
converted = File.open(mapi_file, 'rb') do |f|
  bin = f.read
  # ...
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let mapi = await api.email.convert(
    new EmailConvertRequest('Eml', 'Msg', fs.readFileSync('email.eml')));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$mapi = $api->email()->convert(
    new EmailConvertRequest('Eml', 'Msg', "email.eml"));
```

{{< /tab >}}

{{< /tabs >}}
## **More Tutorials**
See more Aspose Email tutorials: 
