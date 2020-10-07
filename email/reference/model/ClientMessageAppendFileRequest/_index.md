---
title: "ClientMessageAppendFileRequest"
type: docs
url: /reference-model-client-message-append-file-request/
weight: 2
---

Request model for [EmailCloud.Client.Message.AppendFile](/email/reference-client-message-api/#appendfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**account** |**string**|Email account. |
**file** |**System.IO.Stream**|Message file to append. |
**storage** |**string**|Storage name where account file located. |[optional] 
**accountStorageFolder** |**string**|Folder in storage where account file located. |[optional] 
**format** |**string**|Email file format. Enum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft |[optional] [default to 0]
**folder** |**string**|Path to folder on email server to append message to. |[optional] 
**markAsSent** |**bool?**|Determines that appended message should be market as sent or not. |[optional] [default to true]

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="client_message_append_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

