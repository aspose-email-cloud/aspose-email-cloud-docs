---
title: "ClientMessageListRequest"
type: docs
url: /reference-model-client-message-list-request/
weight: 2
---

Request model for [EmailCloud.Client.Message.List](/email/reference-client-message-api/#list) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**folder** |**string**|A folder in email account |
**account** |**string**|Email account |
**queryString** |**string**|A MailQuery search string |[optional] 
**storage** |**string**|Storage name where account file located |[optional] 
**accountStorageFolder** |**string**|Folder in storage where account file located |[optional] 
**recursive** |**bool?**|Specifies that should message be searched in subfolders recursively |[optional] [default to false]
**type** |**string**|MailMessageBase type. Using this property you can get messages in different formats (as EmailDto, MapiMessageDto or a file represented as Base64 string).              Enum, available values: Dto, Mapi, Base64 |[optional] [default to 0]
**format** |**string**|Base64 data format. Used only if type is set to Base64. Enum, available values: Eml, Msg, MsgUnicode, Mhtml, Html, Tnef, Oft |[optional] [default to 0]

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="client_message_list_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

