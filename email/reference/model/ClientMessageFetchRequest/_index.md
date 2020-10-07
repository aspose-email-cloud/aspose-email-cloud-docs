---
title: "ClientMessageFetchRequest"
type: docs
url: /reference-model-client-message-fetch-request/
weight: 2
---

Request model for [EmailCloud.Client.Message.Fetch](/email/reference-client-message-api/#fetch) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**messageId** |**string**|Message identifier |
**account** |**string**|Email account |
**folder** |**string**|Account folder to fetch from (should be specified for some protocols such as IMAP)              |[optional] 
**storage** |**string**|Storage name where account file located. |[optional] 
**accountStorageFolder** |**string**|Folder in storage where account file located. |[optional] 
**type** |**string**|MailMessageBase type. Using this property you can fetch message in different formats (as EmailDto, MapiMessageDto or a file represented as Base64 string).              Enum, available values: Dto, Mapi, Base64 |[optional] [default to 0]
**format** |**string**|Base64 data format. Used only if type is set to Base64. Enum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft |[optional] [default to 0]

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="client_message_fetch_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

