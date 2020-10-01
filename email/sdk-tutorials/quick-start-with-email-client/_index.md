---
title: "Quick Start With Email Client"
type: docs
url: /quick-start-with-email-client/
description: " Aspose Email tutorial shows how to work with your email clients using Aspose.Email Cloud API. Send emails, receive emails, process emails in your way."
weight: 30
---

## **Built-In Email Client**
[Aspose.Email Cloud API ](https://products.aspose.cloud/email/family)contains a built-in email client.

{{% alert color="primary" %}} 

To get more information about the built-in email client, take a look at the [Email Client](/email/email-client/) article. 

{{% /alert %}} 



The built-in email client supports:

- **SMTP**
- **POP3**
- **IMAP**
- **EWS**
- **WebDav**
- **Virtual multi-account**

Virtual multi-account is a fast and convenient way to set up multiple email accounts and use them as a single one.

{{% alert color="primary" %}} 

To see how to setup SDKs use the [SDK setup](/email/sdk-setup/) tutorial.

{{% /alert %}} 


## **How to Work With Email Client**
Before we start, we should set up an email account. This allows you to process your messages with [built-in Email Client](/email/email-client/) which is developed by [Aspose.Email Cloud](https://products.aspose.cloud/email/family).

The **created email account will be saved on storage**, so you don't have to repeat this operation later.
### **Create Email Account File**
You can create an email account online using the instructions from these guides: [Single Email Account Setup](/email/single-email-account-setup/) and [Multi Email Account Setup](/email/multi-email-account-setup/).

### **Setup email account**
First of all, you need to set up your email account’s credentials with [**EmailClientAccountPasswordCredentials**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailClientAccountPasswordCredentials.md) class. Define two fields: *Login* (Email client account login) and *Password* (Email client account password).

Then you need to initialize [**EmailClientAccount**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailClientAccount.md) object. Let’s define the following parameters:

- *Host* — Mail server hostname or IP address.
- *Port* — Mail server port.
- *ProtocolType* — Type of connection protocol. Enum, available values: IMAP, POP3, SMTP, EWS, WebDav.
- *SecurityOptions* — Email account security mode Enum, available values: None, SSLExplicit, SSLImplicit, SSLAuto, Auto.
- *Credentials* — Email client account credentials that we have created before.

To save your email account use [**SaveAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientAccountApi.md#SaveAsync) from [**ClientAccountApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientAccountApi.md). You should create a request for this operation using [**ClientAccountSaveRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientAccountSaveRequest.md), which has **2 parameters**:

- *Value* — Object we want to save on Storage.
- StorageFile — [**StorageFileLocation**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/StorageFileLocation.md) object, which contains IMAP account’s file location information, including **storage name**, a path to an **account folder**, name of the file with **IMAP account’s** configurations.

{{< tabs tabTotal="6" tabID="3" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var credentials = new EmailClientAccountPasswordCredentials { 
    Login = "example@gmail.com", 
    Password = "password" 
};

var receiveAccountDto = new EmailClientAccount {
    Host = "imap.gmail.com", 
    Port = 993, 
    ProtocolType = "IMAP", 
    SecurityOptions = "SSLAuto", 
    Credentials = credentials
};

var imapAccount = "imap.account"; 
var accountFolder = "folder/on/storage";
var storageName = "First storage";
var imapLocation = new StorageFileLocation(storageName, accountFolder, imapAccount);

await api.Client.Account.SaveAsync(new ClientAccountSaveRequest(
    imapLocation, receiveAccountDto));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailClientAccountPasswordCredentials credentials =
    new EmailClientAccountPasswordCredentials(
        "example@gmail.com", "password");
EmailClientAccount receiveAccountDto = new EmailClientAccount(
    "imap.gmail.com", 993, "SSLAuto", "IMAP", credentials, null);

String imapAccount = "imap.account";
String accountFolder = "folder/on/storage";
String storageName = "First Storage";
StorageFileLocation imapLocation = new StorageFileLocation(
    storageName, accountFolder, imapAccount);

api.client().account().save(new ClientAccountSaveRequest(
  imapLocation, receiveAccountDto));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
credentials = models.EmailClientAccountPasswordCredentials(
    'example@gmail.com', 'password')

receive_account_dto = models.EmailClientAccount(
    'imap.gmail.com', 993, 'SSLAuto', 'IMAP', credentials)

imap_account = 'imap.account'
storage_name = 'First storage'
account_folder = 'folder/on/storage'
imap_location = models.StorageFileLocation(
    storage_name, account_folder, imap_account)

api.client.account.save(models.ClientAccountSaveRequest(
    imap_location, receive_account_dto))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
credentials = EmailClientAccountPasswordCredentials.new(
  login: 'example@gmail.com', password: 'password')
receive_account_dto = EmailClientAccount.new(
  host: 'imap.gmail.com',
  port: 993,
  security_options: 'SSLAuto',
  protocol_type: 'IMAP',
  credentials: credentials)

imap_account = 'imap.account'
storage_name = 'First Storage'
account_folder = 'folder/on/storage'
imap_location = StorageFileLocation.new(
  storage: storage_name,
  folder_path: account_folder,
  file_name: imap_account)

api.client.account.save(ClientAccountSaveRequest.new(
  storage_file: imap_location, value: receive_account_dto))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const credentials = new EmailClientAccountPasswordCredentials(
    'example@gmail.com', 'password');
const receiveAccountDto = new EmailClientAccount(
    'imap.gmail.com', 993, 'SSLAuto', 'IMAP', credentials);

const imapAccount = 'imap.account';
const storageName = 'First storage';
const accountFolder = 'folder/on/storage';
const imapLocation = new StorageFileLocation(
    storageName, accountFolder, imapAccount);

await api.client.account.save(
    new ClientAccountSaveRequest(imapLocation, receiveAccountDto));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$credentials = new EmailClientAccountPasswordCredentials(
    "example@gmail.com", "password");
$receiveAccountDto = new EmailClientAccount(
    "imap.gmail.com", 993, "SSLAuto", "IMAP", $credentials);

$imapAccount = "imap.account";
$storageName = "First storage";
$accountFolder = "folder/on/storage";
$imapLocation = new StorageFileLocation(
    $storageName, $accountFolder, $imapAccount);

$api->client()->account()->save(new ClientAccountSaveRequest(
    $imapLocation, $receiveAccountDto));
```

{{< /tab >}}

{{< /tabs >}}


### **Search Emails**

To search for emails in your email account’s folders you need to call [**ListAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md#listasync) from [**ClientMessageApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md). This method has one parameter — **ClientMessageListRequest**, which is a request model for this operation. In this model you should define the following fields:

- *Folder* — A folder in email account.
- *Account* — Email account.
- *QueryString* — A MailQuery search string.
- *Storage* — Storage name where account file(s) located.
- *AccountStorageFolder* — Folder in storage where account file(s) located.
- *Recursive* [**optional**] — Specifies that should message be searched in subfolders recursively.
- *Type* - Using this property you can get messages in different formats (as EmailDto, MapiMessageDto or a file represented as Base64 string).
- *Format* - Base64 data format. Used only if *Type* is set to Base64.

After that, you will get a list of messages matching your search criteria as [**MailMessageBaseList**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/MailMessageBaseList.md).

**Now you can search emails**

{{< tabs tabTotal="6" tabID="5" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
const string imapFolderName = "INBOX";
MailMessageBaseList messages = await api.Client.Message.ListAsync(
    new ClientMessageListRequest(
        imapFolderName, imapAccount, "('From' Contains '.com')",
        storageName, accountFolder, true, "Dto"));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
String imapFolderName = "INBOX";
MailMessageBaseList messages = api.client().message().list(new ClientMessageListRequest(
    imapFolderName , imapAccount, "('From' Contains '.com')", storageName,
    accountFolder, true, "Dto", null));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
imap_folder_name = 'INBOX'
messages = api.client.message.list(models.ClientMessageListRequest(
    imap_folder_name, imap_account, "('From' Contains '.com')",
    storage_name, account_folder, True, 'Dto'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
imap_folder_name = 'INBOX'
messages = api.client.message.list(ClientMessageListRequest.new(
  folder: imap_folder_name,
  account: imap_account,
  query_string: "('From' Contains '.com')",
  storage: storage_name,
  account_storage_folder: account_folder,
  recursive: true,
  type: 'Dto'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const imapFolderName = 'INBOX';
const messages = await api.client.message.list(new ClientMessageListRequest(
    imapFolderName, imapAccount, "('From' Contains '.com')",
    storageName, accountFolder, true, 'Dto'));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$imapFolderName = 'INBOX';
$messages = $api->client()->message()->list(new ClientMessageListRequest(
    $imapFolderName, $imapAccount, "('From' Contains '.com')",
    $storageName, $accountFolder, true, 'Dto'));
```

{{< /tab >}}

{{< /tabs >}}


### **Fetch Message By Id**
In the previous step, we have got a list of emails. Let’s fetch one of them by its Id.

To do this you should use the **email’s Id**, obviously, and [**FetchAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md#FetchAsync) method from [**ClientMessageApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md). This method requires **1 parameter** — **ClientMessageFetchRequest**, which is a request model for this operation. 
**ClientMessageFetchRequest** has the following parameters:
- *MessageId* — Message identifier. 
- *Account* — Email account.
- *Folder* — Account folder to fetch from (should be specified for some protocols such as IMAP).
- *Storage* — Storage name where account file(s) located.
- *AccountStorageFolder* — Folder in storage where account file(s) located.
- *Type* - Using this property you can get messages in different formats (as EmailDto, MapiMessageDto or a file represented as Base64 string).
- *Format* - Base64 data format. Used only if *Type* is set to Base64.

Аfter this operation you will receive an email as an object inherited from [**MailMessageBase**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/MailMessageBase.md).

**Fetch found message by id**

{{< tabs tabTotal="6" tabID="7" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var foundMessage = messages.Value.First() as MailMessageDto;
var id = foundMessage.Value.MessageId;
var message = await Api.Client.Message.FetchAsync(new ClientMessageFetchRequest(
    id, imapAccount, null, storageName, accountFolder));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MailMessageDto foundMessage = (MailMessageDto) messages.getValue().get(0);
String id = foundMessage.getValue().getMessageId();
MailMessageDto message = (MailMessageDto) api.client().message().fetch(
    new ClientMessageFetchRequest(
        id, imapAccount, null,
        storageName, accountFolder, "Dto", null));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
found_message = messages.value[0]   # type: models.MailMessageDto
id = found_message.value.message_id
message = api.client.message.fetch(models.ClientMessageFetchRequest(
    id, imap_account, None, storage_name, account_folder, 'Dto'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
found_message = messages.value[0]
id = found_message.value.message_id
message = api.client.message.fetch(
  ClientMessageFetchRequest.new(
    message_id: id,
    account: imap_account,
    storage: storage_name,
    account_storage_folder: account_folder,
    type: 'Dto'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const foundMessage = messages.value[0] as MailMessageDto;
const id = foundMessage.value.messageId;
const message = await api.client.message.fetch(new ClientMessageFetchRequest(
    id, imapAccount, undefined, storageName, accountFolder, 'Dto'));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$id = $messages->getValue()[0]->getValue()->getMessageId();
$message = $api->client()->message()->fetch(new ClientMessageFetchRequest(
    $id, $imapAccount, null, $storageName, $accountFolder, 'Dto'));
```

{{< /tab >}}

{{< /tabs >}}


### **Mark Message as Read**

You need to know message’s Id to mark it as read. We have done it in previous steps.

To mark a message as read use [**SetIsReadAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md#SetIsReadAsync) from [**ClientMessageApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md). This method requires **1 parameter** — [**ClientMessageSetIsReadRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageSetIsReadRequest.md), which is a request model for this operation.

[**ClientMessageSetIsReadRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageSetIsReadRequest.md) has **3 parameters**:

- *AccountLocation* — Account location on storage.
- *MessageId* — Message identifier.
- *IsRead* — Specifies that message should be marked read or unread.

**Mark message as read**

{{< tabs tabTotal="6" tabID="10" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
await api.Client.Message.SetIsReadAsync(
    new ClientMessageSetIsReadRequest(
        imapLocation, id, true));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().message().setIsRead(
    new ClientMessageSetIsReadRequest(
        imapLocation, id, true));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
api.client.message.set_is_read(
    models.ClientMessageSetIsReadRequest(
        imap_location, id, True))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
api.client.message.set_is_read(
  ClientMessageSetIsReadRequest.new(
    account_location: imap_location,
    message_id: id,
    is_read: true))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
await api.client.message.setIsRead(
    new ClientMessageSetIsReadRequest(
        imapLocation, id, true));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->message()->setIsRead(
    new ClientMessageSetIsReadRequest(
        $imapLocation, $id, true));
```

{{< /tab >}}

{{< /tabs >}}


### **Delete Message**
In an attempt to manage your messages, you may need to delete some of them.
To remove a message, you should know the Id of the email you want to delete.

To delete email use [**DeleteAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md#deleteasync) from [**ClientMessageApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md). This method requires **1 parameter** — [**ClientMessageDeleteRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageDeleteRequest.md), which is a request model for this operation.

[**ClientMessageDeleteRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageDeleteRequest.md) requires the following parameters:

- *AccountLocation* — Account location on storage.
- *MessageId* — Message identifier.
- *Folder* — Folder to delete message from.

{{< tabs tabTotal="6" tabID="13" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
await api.Client.Message.DeleteAsync(
    new ClientMessageDeleteRequest(
        imapLocation, id, imapFolderName));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().message().delete(
    new ClientMessageDeleteRequest(
        imapLocation, id, imapFolderName));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
api.client.message.delete(models.ClientMessageDeleteRequest(
    imap_location, id, imap_folder_name))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
api.client.message.delete(
  ClientMessageDeleteRequest.new(
    account_location: imap_location,
    message_id: id,
    folder: imap_folder_name))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
await api.client.message.delete(new ClientMessageDeleteRequest(
    imapLocation, id, imapFolderName));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->message()->delete(
    new ClientMessageDeleteRequest(
        $imapLocation, $id, $imapFolderName));
```

{{< /tab >}}

{{< /tabs >}}


### **Append new message**
To append a new message to your email account — use [**AppendAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md#appendasync) from [**ClientMessageApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md). This method requires **1 parameter** — [**ClientMessageAppendRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageAppendRequest.md), which is a request model for this operation.

[**ClientMessageAppendRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageAppendRequest.md) requires the following parameters:

- *AccountLocation* — Account location on storage.
- *Folder* — Path to folder on email server to append message to.
- *MarkAsSent* — Mark message as sent.
- *Message* — Email document.

{{< tabs tabTotal="6" tabID="16" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var emailToAppend = new EmailDto
{
    From = new MailAddress{Address = "example@gmail.com"},
    To = new List<MailAddress> {new MailAddress{Address = "to@aspose.com"}},
    Subject = "Some subject",
    Body = "Some body"
};

var appendedMessageId = await api.Client.Message.AppendAsync(
    new ClientMessageAppendRequest(
        imapLocation, imapFolderName,
        new MailMessageDto(emailToAppend), true));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailDto emailToAppend = new EmailDto()
    .from(new MailAddress().address("example@gmail.com"))
    .addToItem(new MailAddress().address("to@aspose.com"))
    .subject("Some subject")
    .body("Some body");
ValueTOfString appendedMessageId = api.client().message().append(
    new ClientMessageAppendRequest(
        imapLocation, imapFolderName,
        new MailMessageDto(emailToAppend), true));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
email_document = models.EmailDto(
    _from=models.MailAddress('From Name', 'example@gmail.com'),
    to=[models.MailAddress('To Name', 'to@aspose.com')],
    subject='Some subject',
    body='Some body')
appended_message_id = api.client.message.append(
    models.ClientMessageAppendRequest(
        imap_location, imap_folder_name,
        models.MailMessageDto(email_document), True))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
email = EmailDto.new(
  from: MailAddress.new(address: 'example@gmail.com'),
  to: [MailAddress.new(address: 'to@aspose.com')],
  subject: 'Some subject',
  body: 'Some body'
)
appended_message_id = api.client.message.append(
  ClientMessageAppendRequest.new(
    account_location: imap_location,
    folder: imap_folder_name,
    message: MailMessageDto.new(value: email),
    mark_as_sent: true))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const email = new EmailDto();
email.from = new MailAddress('From address', 'example@gmail.com');
email.to = [new MailAddress('To address', 'to@aspose.com')];
email.subject = 'Some subject';
email.body = 'Some body';
const appendedMessageId = await api.client.message.append(
    new ClientMessageAppendRequest(
        imapLocation, imapFolderName,
        new MailMessageDto(email), true));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$email = (new EmailDto())
    ->setFrom(new MailAddress("Organizer Name", "example@gmail.com"))
    ->setTo(array(new MailAddress("Attendee Name", "to@aspose.com")))
    ->setSubject("Some subject")
    ->setBody("Some body");
$appendedMessageId = $api->client()->message()->append(
    new ClientMessageAppendRequest(
        $imapLocation, $imapFolderName,
        new MailMessageDto($email), true));
```

{{< /tab >}}

{{< /tabs >}}


### **Setup email account for sending messages**

All you have to do to setup your email account for sending messages is to use [**SaveAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientAccountApi.md#SaveAsync) from [**ClientAccountApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientAccountApi.md). This method requires **1 parameter** — [**ClientAccountSaveRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientAccountSaveRequest.md), which is a request model for this operation.

[**ClientAccountSaveRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientAccountSaveRequest.md) requires the following parameters:

- Value — [**EmailClientAccount**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/EmailClientAccount.md) object.
- StorageFile — [**StorageFileLocation**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/StorageFileLocation.md) object.

{{< tabs tabTotal="6" tabID="19" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var sendAccountDto = new EmailClientAccount
{
    Host = "smtp.gmail.com",
    Port = 465,
    ProtocolType = "SMTP",
    SecurityOptions = "SSLAuto",
    Credentials = credentials
};
var smtpAccount = "smtp.account";
var smtpLocation = new StorageFileLocation(
    storageName, accountFolder, smtpAccount);

await Api.Client.Account.SaveAsync(new ClientAccountSaveRequest(
    smtpLocation, sendAccountDto));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailClientAccount sendAccountDto = new EmailClientAccount(
    "smtp.gmail.com", 465, "SSLAuto", "SMTP", credentials);
String smtpAccount = "smtp.account";
String smtpLocation = new StorageFileLocation(
    storageName, accountFolder, smtpAccount);
api.client().account().save(new ClientAccountSaveRequest(
    smtpLocation, sendAccountDto));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
send_account_dto = models.EmailClientAccount(
    'smtp.gmail.com', 465, 'SSLAuto', 'SMTP', credentials)
smtp_account = 'smtp.account'
smtp_location = models.StorageFileLocation(
    storage_name, account_folder, smtp_account)

api.client.account.save(
    models.ClientAccountSaveRequest(
        smtp_location, send_account_dto))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```rb
send_account_dto = EmailClientAccount.new(
  host: 'smtp.gmail.com',
  port: 465,
  security_options: 'SSLAuto',
  protocol_type: 'SMTP',
  credentials: credentials)
smtp_account = 'smtp.account'
smtp_location = StorageFileLocation.new(
  storage: storage_name,
  folder_path: account_folder,
  file_name: smtp_account)
# Save account
api.client.account.save(ClientAccountSaveRequest.new(
  storage_file: smtp_location, value: send_account_dto))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```ts
const sendAccountDto = new EmailClientAccount(
    'smtp.gmail.com', 465, 'SSLAuto', 'SMTP', credentials);
const smtpAccount = 'smtp.account';
const smtpLocation = new StorageFileLocation(
    storageName, accountFolder, smtpAccount);

await td.api().client.account.save(
    new ClientAccountSaveRequest(smtpLocation, sendAccountDto));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$sendAccountDto = new EmailClientAccount(
    "smtp.gmail.com", 465, "SSLAuto", "SMTP", $credentials);
$smtpAccount = "smtp.account";
$smtpLocation = new StorageFileLocation(
    $storageName, $accountFolder, $smtpAccount);

$api->client()->account()->save(
    new ClientAccountSaveRequest($smtpLocation, $sendAccountDto));
```

{{< /tab >}}

{{< /tabs >}}


### **Send Email**

To send a message using your email account — use [**SendAsync**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md#sendasync) from [**ClientMessageApi**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageApi.md). This method requires **1 parameter** — [**ClientMessageSendRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageSendRequest.md), which is a request model for this operation.

[**ClientMessageSendRequest**](https://github.com/aspose-email-cloud/aspose-email-cloud-dotnet/blob/master/docs/ClientMessageSendRequest.md) requires the following parameters:

- *AccountLocation* — Account location on storage.
- *Message* — Email document to send.

{{< tabs tabTotal="6" tabID="22" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```cs
var email = new EmailDto
{
    From = new MailAddress {Address = "example@gmail.com"},
    To = new List<MailAddress> {new MailAddress {Address = "to@aspose.com"}},
    Subject = "Some subject",
    Body = "Some body"
};
await api.Client.Message.SendAsync(
    new ClientMessageSendRequest(
        smtpLocation, new MailMessageDto(email)));
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
EmailDto email = new EmailDto()
    .from(new MailAddress().address("example@gmail.com"))
    .addToItem(new MailAddress().address("to@aspose.com"))
    .subject("Some subject")
    .body("Some body");
api.client().message().send(
    new ClientMessageSendRequest(
        smtpLocation, new MailMessageDto(email)));
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```py
email_document = models.EmailDto(
    _from=models.MailAddress('From Name', 'example@gmail.com'),
    to=[models.MailAddress('To Name', 'to@aspose.com')],
    subject='Some subject',
    body='Some body')
api.client.message.send(
    models.ClientMessageSendRequest(
        smtp_location, models.MailMessageDto(email_document)))
```

{{< /tab >}}

{{< tab tabNum="4" >}}



```rb
email = EmailDto.new(
  from: MailAddress.new(address: 'example@gmail.com'),
  to: [MailAddress.new(address: 'to@aspose.com')],
  subject: 'Some subject',
  body: 'Some body'
)

api.client.message.send(
  ClientMessageSendRequest.new(
    account_location: smtp_location,
    message: MailMessageDto.new(value: email)))
```

{{< /tab >}}

{{< tab tabNum="5" >}}



```ts
const email = new EmailDto();
email.from = new MailAddress('From address', 'example@gmail.com');
email.to = [new MailAddress('To address', 'to@aspose.com')];
email.subject = 'Some subject';
email.body = 'Some body';
await api.client.message.send(
    new ClientMessageSendRequest(
        smtpLocation, new MailMessageDto(email)));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$email = (new EmailDto())
    ->setFrom(new MailAddress("Organizer Name", "example@gmail.com"))
    ->setTo(array(new MailAddress("Attendee Name", "to@aspose.com")))
    ->setSubject("Some subject")
    ->setBody("Some body");
$api->client()->message()->send(
    new ClientMessageSendRequest(
        $smtpLocation, new MailMessageDto($email)));
```

{{< /tab >}}

{{< /tabs >}}


## **More Tutorials**
See more Aspose Email tutorials: 
{{< list-of-articles-in-this-section >}}
