---
title: "Message"
type: docs
url: /reference-client-message-api/
weight: 1
---

Email client message operations.


The most important part of the email client is Message management API.

Use this API to send, search, fetch, append, move, mark as read, or delete messages.

## Append

Add email message to specified folder in email account. 
Returns [**ValueTOfString**](/email/reference-model-value-t-of-string/) model. Requires:

{{< expand-list title="request" >}}

Append email request. Type: [**ClientMessageAppendRequest**](/email/reference-model-client-message-append-request/).

{{< tabs tabTotal="6" tabID="client_message_append_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientMessageAppendRequest
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
ClientMessageAppendRequest request = Models.clientMessageAppendRequest()
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
request = models.ClientMessageAppendRequest(
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
request = ClientMessageAppendRequest.new(
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
let request = Models.clientMessageAppendRequest()
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
$request = Models::clientMessageAppendRequest()
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

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="client_message_append_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Client.Message.AppendAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ValueTOfString result = api.client().message().append(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.client.message.append(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.client.message.append(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.client.message.append(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->client()->message()->append($request);
```

{{< /tab >}}

{{< /tabs >}}
## AppendFile

Add email message from file to specified folder in email account. 
Returns [**ValueTOfString**](/email/reference-model-value-t-of-string/) model. Requires:

{{< expand-list title="request" >}}

AppendFile method request. Type: [**ClientMessageAppendFileRequest**](/email/reference-model-client-message-append-file-request/).

{{< tabs tabTotal="6" tabID="client_message_append_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientMessageAppendFileRequest
{ 
    Account = "email.multi.account",
    File = new MemoryStream(File.ReadAllBytes("/path/to/message.eml")),
    Storage = "First Storage",
    AccountStorageFolder = "email/account/location/on/storage",
    Format = "Eml",
    Folder = "INBOX"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientMessageAppendFileRequest request = Models.clientMessageAppendFileRequest()
    .account("email.multi.account")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/message.eml")))
    .storage("First Storage")
    .accountStorageFolder("email/account/location/on/storage")
    .format("Eml")
    .folder("INBOX")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientMessageAppendFileRequest(
    account='email.multi.account',
    file='/path/to/message.eml',
    storage='First Storage',
    account_storage_folder='email/account/location/on/storage',
    format='Eml',
    folder='INBOX')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientMessageAppendFileRequest.new(
    account: 'email.multi.account',
    file: File.new('/path/to/message.eml'),
    storage: 'First Storage',
    account_storage_folder: 'email/account/location/on/storage',
    format: 'Eml',
    folder: 'INBOX')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ClientMessageAppendFileRequest()
    .account('email.multi.account')
    .file(fs.readFileSync('/path/to/message.eml'))
    .storage('First Storage')
    .accountStorageFolder('email/account/location/on/storage')
    .format('Eml')
    .folder('INBOX')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ClientMessageAppendFileRequest()
    ->account('email.multi.account')
    ->file(new SplFileObject('/path/to/message.eml'))
    ->storage('First Storage')
    ->account_storage_folder('email/account/location/on/storage')
    ->format('Eml')
    ->folder('INBOX')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="client_message_append_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Client.Message.AppendFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ValueTOfString result = api.client().message().appendFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.client.message.append_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.client.message.append_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.client.message.appendFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->client()->message()->appendFile($request);
```

{{< /tab >}}

{{< /tabs >}}
## Delete

Delete message. Requires:

{{< expand-list title="request" >}}

Delete message request. Type: [**ClientMessageDeleteRequest**](/email/reference-model-client-message-delete-request/).

{{< tabs tabTotal="6" tabID="client_message_delete_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientMessageDeleteRequest
{
    Folder = "INBOX",
    MessageId = "5",
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
ClientMessageDeleteRequest request = Models.clientMessageDeleteRequest()
    .folder("INBOX")
    .messageId("5")
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
request = models.ClientMessageDeleteRequest(
    folder='INBOX',
    message_id='5',
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientMessageDeleteRequest.new(
  folder: 'INBOX',
  message_id: '5',
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.clientMessageDeleteRequest()
    .folder('INBOX')
    .messageId('5')
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
$request = Models::clientMessageDeleteRequest()
    ->folder('INBOX')
    ->messageId('5')
    ->accountLocation(Models::storageFileLocation()
        ->fileName('email.account')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="client_message_delete_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Client.Message.DeleteAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().message().delete(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.client.message.delete(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.client.message.delete(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.client.message.delete(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->message()->delete($request);
```

{{< /tab >}}

{{< /tabs >}}
## Fetch

Fetch message from email account. 
Returns [**MailMessageBase**](/email/reference-model-mail-message-base/) model. Requires:

{{< expand-list title="request" >}}

Fetch method request. Type: [**ClientMessageFetchRequest**](/email/reference-model-client-message-fetch-request/).

{{< tabs tabTotal="6" tabID="client_message_fetch_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientMessageFetchRequest
{ 
    MessageId = "<put your message identifier here>",
    Account = "email.multi.account",
    Folder = "INBOX",
    Storage = "First Storage",
    AccountStorageFolder = "email/account/location/on/storage",
    Type = "Dto",
    Format = "Eml"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientMessageFetchRequest request = Models.clientMessageFetchRequest()
    .messageId("<put your message identifier here>")
    .account("email.multi.account")
    .folder("INBOX")
    .storage("First Storage")
    .accountStorageFolder("email/account/location/on/storage")
    .type("Dto")
    .format("Eml")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientMessageFetchRequest(
    message_id='<put your message identifier here>',
    account='email.multi.account',
    folder='INBOX',
    storage='First Storage',
    account_storage_folder='email/account/location/on/storage',
    type='Dto',
    format='Eml')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientMessageFetchRequest.new(
    message_id: '<put your message identifier here>',
    account: 'email.multi.account',
    folder: 'INBOX',
    storage: 'First Storage',
    account_storage_folder: 'email/account/location/on/storage',
    type: 'Dto',
    format: 'Eml')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ClientMessageFetchRequest()
    .messageId('<put your message identifier here>')
    .account('email.multi.account')
    .folder('INBOX')
    .storage('First Storage')
    .accountStorageFolder('email/account/location/on/storage')
    .type('Dto')
    .format('Eml')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ClientMessageFetchRequest()
    ->message_id('<put your message identifier here>')
    ->account('email.multi.account')
    ->folder('INBOX')
    ->storage('First Storage')
    ->account_storage_folder('email/account/location/on/storage')
    ->type('Dto')
    ->format('Eml')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="client_message_fetch_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Client.Message.FetchAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MailMessageBase result = api.client().message().fetch(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.client.message.fetch(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.client.message.fetch(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.client.message.fetch(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->client()->message()->fetch($request);
```

{{< /tab >}}

{{< /tabs >}}
## FetchFile

Fetch message as file from email account. 
Returns a **File**. Requires:

{{< expand-list title="request" >}}

FetchFile method request. Type: [**ClientMessageFetchFileRequest**](/email/reference-model-client-message-fetch-file-request/).

{{< tabs tabTotal="6" tabID="client_message_fetch_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientMessageFetchFileRequest
{ 
    MessageId = "<put your message identifier here>",
    Account = "email.multi.account",
    Folder = "INBOX",
    Storage = "First Storage",
    AccountStorageFolder = "email/account/location/on/storage",
    Format = "Eml"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientMessageFetchFileRequest request = Models.clientMessageFetchFileRequest()
    .messageId("<put your message identifier here>")
    .account("email.multi.account")
    .folder("INBOX")
    .storage("First Storage")
    .accountStorageFolder("email/account/location/on/storage")
    .format("Eml")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientMessageFetchFileRequest(
    message_id='<put your message identifier here>',
    account='email.multi.account',
    folder='INBOX',
    storage='First Storage',
    account_storage_folder='email/account/location/on/storage',
    format='Eml')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientMessageFetchFileRequest.new(
    message_id: '<put your message identifier here>',
    account: 'email.multi.account',
    folder: 'INBOX',
    storage: 'First Storage',
    account_storage_folder: 'email/account/location/on/storage',
    format: 'Eml')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ClientMessageFetchFileRequest()
    .messageId('<put your message identifier here>')
    .account('email.multi.account')
    .folder('INBOX')
    .storage('First Storage')
    .accountStorageFolder('email/account/location/on/storage')
    .format('Eml')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ClientMessageFetchFileRequest()
    ->message_id('<put your message identifier here>')
    ->account('email.multi.account')
    ->folder('INBOX')
    ->storage('First Storage')
    ->account_storage_folder('email/account/location/on/storage')
    ->format('Eml')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="client_message_fetch_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Client.Message.FetchFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.client().message().fetchFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.client.message.fetch_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.client.message.fetch_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.client.message.fetchFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->client()->message()->fetchFile($request);
```

{{< /tab >}}

{{< /tabs >}}
## List

Get messages from folder, filtered by query.


**The queryString should have the following view.**

The example of a simple expression:

&#x60;&#39;&lt;Field name&gt;&#39; &lt;Comparison operator&gt; &#39;&lt;Field value&gt;&#39;&#x60;

where
- &lt;Field Name&gt; - the name of a message field through which filtering is made,
- &lt;Comparison operator&gt; - comparison operators, as their name implies, allow to compare
message field and specified value,
- &lt;Field value&gt; - value to be compared with a message field.

The number of simple expressions can make a compound one, ex.:

&#x60;(&lt;Simple expression 1&gt; &amp; &lt;Simple expression 2&gt;) | &lt;Simple expression 3&gt;&#x60;

where
- &quot;&amp;&quot; - logical-AND operator,
- &quot;|&quot; - logical-OR operator

At present the following values are allowed as a field name (&lt;Field name&gt;):
- &quot;To&quot; - represents a TO field of message,
- &quot;Text&quot; - represents string in the header or body of the message,
- &quot;Bcc&quot; - represents a BCC field of message,
- &quot;Body&quot; - represents a string in the body of message,
- &quot;Cc&quot; - represents a CC field of message,
- &quot;From&quot; - represents a From field of message,
- &quot;Subject&quot; - represents a string in the subject of message,
- &quot;InternalDate&quot; - represents an internal date of message,
- &quot;SentDate&quot; - represents a sent date of message

Additionally, the following field names are allowed for IMAP-protocol:

- &quot;Answered&quot; - represents an /Answered flag of message
- &quot;Seen&quot; - represents a /Seen flag of message
- &quot;Flagged&quot; - represents a /Flagged flag of message
- &quot;Draft&quot; - represents a /Draft flag of message
- &quot;Deleted&quot; - represents a Deleted/ flag of message
- &quot;Recent&quot; - represents a Deleted/ flag of message
- &quot;MessageSize&quot; - represents a size (in bytes) of message

Additionally, the following field names are allowed for Exchange:

- &quot;IsRead&quot; - Indicates whether the message has been read
- &quot;HasAttachment&quot; - Indicates whether or not the message has attachments
- &quot;IsSubmitted&quot; - Indicates whether the message has been submitted to the Outbox
- &quot;ContentClass&quot; - represents a content class of item

The field value (&lt;Field value&gt;) can take the following values:
- For text fields - any string,
- For date type fields - the string of &quot;d-MMM-yyy&quot; format, ex. &quot;10-Feb-2009&quot;,
- For flags (fields of boolean type) - either &quot;True&quot;, or &quot;False&quot;

***Example:***

&#x60;((&#39;From&#39; Contains &#39;test@test.com&#39; | &#39;Seen&#39; &#x3D; &#39;True&#39;) &amp; &#39;SentDate&#39; &gt;&#x3D; &#39;12-May-2010&#39;)&#x60;


     
Returns [**MailMessageBaseList**](/email/reference-model-mail-message-base-list/) model. Requires:

{{< expand-list title="request" >}}

List method request. Type: [**ClientMessageListRequest**](/email/reference-model-client-message-list-request/).

{{< tabs tabTotal="6" tabID="client_message_list_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientMessageListRequest
{ 
    Folder = "INBOX",
    Account = "email.multi.account",
    QueryString = "('From' Contains '.com')",
    Storage = "First Storage",
    AccountStorageFolder = "email/account/location/on/storage",
    Recursive = true,
    Type = "Dto",
    Format = "Eml"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientMessageListRequest request = Models.clientMessageListRequest()
    .folder("INBOX")
    .account("email.multi.account")
    .queryString("('From' Contains '.com')")
    .storage("First Storage")
    .accountStorageFolder("email/account/location/on/storage")
    .recursive(true)
    .type("Dto")
    .format("Eml")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientMessageListRequest(
    folder='INBOX',
    account='email.multi.account',
    query_string='('From' Contains '.com')',
    storage='First Storage',
    account_storage_folder='email/account/location/on/storage',
    recursive=True,
    type='Dto',
    format='Eml')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientMessageListRequest.new(
    folder: 'INBOX',
    account: 'email.multi.account',
    query_string: '('From' Contains '.com')',
    storage: 'First Storage',
    account_storage_folder: 'email/account/location/on/storage',
    recursive: true,
    type: 'Dto',
    format: 'Eml')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ClientMessageListRequest()
    .folder('INBOX')
    .account('email.multi.account')
    .queryString('('From' Contains '.com')')
    .storage('First Storage')
    .accountStorageFolder('email/account/location/on/storage')
    .recursive(true)
    .type('Dto')
    .format('Eml')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ClientMessageListRequest()
    ->folder('INBOX')
    ->account('email.multi.account')
    ->query_string('('From' Contains '.com')')
    ->storage('First Storage')
    ->account_storage_folder('email/account/location/on/storage')
    ->recursive(true)
    ->type('Dto')
    ->format('Eml')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="client_message_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Client.Message.ListAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MailMessageBaseList result = api.client().message().list(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.client.message.list(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.client.message.list(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.client.message.list(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->client()->message()->list($request);
```

{{< /tab >}}

{{< /tabs >}}
## Move

Move message to another folder. Requires:

{{< expand-list title="request" >}}

Move message request. Type: [**ClientMessageMoveRequest**](/email/reference-model-client-message-move-request/).

{{< tabs tabTotal="6" tabID="client_message_move_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientMessageMoveRequest
{
    SourceFolder = "INBOX",
    DestinationFolder = "INBOX/SubFolder",
    MessageId = "5",
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
ClientMessageMoveRequest request = Models.clientMessageMoveRequest()
    .sourceFolder("INBOX")
    .destinationFolder("INBOX/SubFolder")
    .messageId("5")
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
request = models.ClientMessageMoveRequest(
    source_folder='INBOX',
    destination_folder='INBOX/SubFolder',
    message_id='5',
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientMessageMoveRequest.new(
  source_folder: 'INBOX',
  destination_folder: 'INBOX/SubFolder',
  message_id: '5',
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.clientMessageMoveRequest()
    .sourceFolder('INBOX')
    .destinationFolder('INBOX/SubFolder')
    .messageId('5')
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
$request = Models::clientMessageMoveRequest()
    ->sourceFolder('INBOX')
    ->destinationFolder('INBOX/SubFolder')
    ->messageId('5')
    ->accountLocation(Models::storageFileLocation()
        ->fileName('email.account')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="client_message_move_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Client.Message.MoveAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().message().move(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.client.message.move(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.client.message.move(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.client.message.move(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->message()->move($request);
```

{{< /tab >}}

{{< /tabs >}}
## Send

Send an email specified by model in request. Requires:

{{< expand-list title="request" >}}

Send email request. Type: [**ClientMessageSendRequest**](/email/reference-model-client-message-send-request/).

{{< tabs tabTotal="6" tabID="client_message_send_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientMessageSendRequest
{
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
ClientMessageSendRequest request = Models.clientMessageSendRequest()
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
request = models.ClientMessageSendRequest(
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
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientMessageSendRequest.new(
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
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.clientMessageSendRequest()
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
$request = Models::clientMessageSendRequest()
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
    ->accountLocation(Models::storageFileLocation()
        ->fileName('email.account')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="client_message_send_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Client.Message.SendAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().message().send(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.client.message.send(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.client.message.send(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.client.message.send(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->message()->send($request);
```

{{< /tab >}}

{{< /tabs >}}
## SendFile

Send an email file. Requires:

{{< expand-list title="request" >}}

SendFile method request. Type: [**ClientMessageSendFileRequest**](/email/reference-model-client-message-send-file-request/).

{{< tabs tabTotal="6" tabID="client_message_send_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientMessageSendFileRequest
{ 
    Account = "email.multi.account",
    File = new MemoryStream(File.ReadAllBytes("/path/to/message.eml")),
    Storage = "First Storage",
    AccountStorageFolder = "email/account/location/on/storage",
    Format = "Eml"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientMessageSendFileRequest request = Models.clientMessageSendFileRequest()
    .account("email.multi.account")
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/message.eml")))
    .storage("First Storage")
    .accountStorageFolder("email/account/location/on/storage")
    .format("Eml")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientMessageSendFileRequest(
    account='email.multi.account',
    file='/path/to/message.eml',
    storage='First Storage',
    account_storage_folder='email/account/location/on/storage',
    format='Eml')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientMessageSendFileRequest.new(
    account: 'email.multi.account',
    file: File.new('/path/to/message.eml'),
    storage: 'First Storage',
    account_storage_folder: 'email/account/location/on/storage',
    format: 'Eml')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ClientMessageSendFileRequest()
    .account('email.multi.account')
    .file(fs.readFileSync('/path/to/message.eml'))
    .storage('First Storage')
    .accountStorageFolder('email/account/location/on/storage')
    .format('Eml')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ClientMessageSendFileRequest()
    ->account('email.multi.account')
    ->file(new SplFileObject('/path/to/message.eml'))
    ->storage('First Storage')
    ->account_storage_folder('email/account/location/on/storage')
    ->format('Eml')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="client_message_send_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Client.Message.SendFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().message().sendFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.client.message.send_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.client.message.send_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.client.message.sendFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->message()->sendFile($request);
```

{{< /tab >}}

{{< /tabs >}}
## SetIsRead

Mark message as read or unread. Requires:

{{< expand-list title="request" >}}

Delete message request. Type: [**ClientMessageSetIsReadRequest**](/email/reference-model-client-message-set-is-read-request/).

{{< tabs tabTotal="6" tabID="client_message_set_is_read_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientMessageSetIsReadRequest
{
    IsRead = true,
    MessageId = "5",
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
ClientMessageSetIsReadRequest request = Models.clientMessageSetIsReadRequest()
    .isRead(true)
    .messageId("5")
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
request = models.ClientMessageSetIsReadRequest(
    is_read=True,
    message_id='5',
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientMessageSetIsReadRequest.new(
  is_read: true,
  message_id: '5',
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.clientMessageSetIsReadRequest()
    .isRead(true)
    .messageId('5')
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
$request = Models::clientMessageSetIsReadRequest()
    ->isRead(true)
    ->messageId('5')
    ->accountLocation(Models::storageFileLocation()
        ->fileName('email.account')
        ->storage('First Storage')
        ->folderPath('file/location/folder/on/storage')
        ->build())
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="client_message_set_is_read_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Client.Message.SetIsReadAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().message().setIsRead(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.client.message.set_is_read(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.client.message.set_is_read(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.client.message.setIsRead(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->message()->setIsRead($request);
```

{{< /tab >}}

{{< /tabs >}}

## More APIs

{{< list-of-articles-in-this-section >}}
