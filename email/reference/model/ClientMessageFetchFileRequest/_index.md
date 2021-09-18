---
title: "ClientMessageFetchFileRequest"
type: docs
url: /reference-model-client-message-fetch-file-request/
weight: 2
---

Request model for [EmailCloud.Client.Message.FetchFile](/email/reference-client-message-api/#fetchfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**messageId** |**string**|Message identifier |
**account** |**string**|Email account |
**folder** |**string**|Account folder to fetch from (should be specified for some protocols such as IMAP)              |[optional] 
**storage** |**string**|Storage name where account file located. |[optional] 
**accountStorageFolder** |**string**|Folder in storage where account file located. |[optional] 
**format** |**string**|Fetched message file format./nEnum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft |[optional] [default to 0]

## Example

{{< tabs tabTotal="6" tabID="client_message_fetch_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

