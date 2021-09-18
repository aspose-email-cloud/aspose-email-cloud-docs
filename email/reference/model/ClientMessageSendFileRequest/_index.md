---
title: "ClientMessageSendFileRequest"
type: docs
url: /reference-model-client-message-send-file-request/
weight: 2
---

Request model for [EmailCloud.Client.Message.SendFile](/email/reference-client-message-api/#sendfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**account** |**string**|Email account |
**file** |**System.IO.Stream**|File to send |
**storage** |**string**|Storage name where account file located. |[optional] 
**accountStorageFolder** |**string**|Folder in storage where account file located. |[optional] 
**format** |**string**|Email file format./nEnum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft |[optional] [default to 0]

## Example

{{< tabs tabTotal="6" tabID="client_message_send_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

