---
title: "ClientThreadGetMessagesRequest"
type: docs
url: /reference-model-client-thread-get-messages-request/
weight: 2
---

Request model for [EmailCloud.Client.Thread.GetMessages](/email/reference-client-thread-api/#getmessages) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**threadId** |**string**|Thread identifier |
**account** |**string**|Email account |
**folder** |**string**|Specifies account folder to get thread from              |[optional] 
**storage** |**string**|Storage name where account file located |[optional] 
**accountStorageFolder** |**string**|Folder in storage where account file located |[optional] 

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="client_thread_get_messages_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientThreadGetMessagesRequest
{ 
    ThreadId = "5",
    Account = "email.account",
    Folder = "INBOX",
    Storage = "First Storage",
    AccountStorageFolder = "email/account/location/on/storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientThreadGetMessagesRequest request = Models.clientThreadGetMessagesRequest()
    .threadId("5")
    .account("email.account")
    .folder("INBOX")
    .storage("First Storage")
    .accountStorageFolder("email/account/location/on/storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientThreadGetMessagesRequest(
    thread_id='5',
    account='email.account',
    folder='INBOX',
    storage='First Storage',
    account_storage_folder='email/account/location/on/storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientThreadGetMessagesRequest.new(
    thread_id: '5',
    account: 'email.account',
    folder: 'INBOX',
    storage: 'First Storage',
    account_storage_folder: 'email/account/location/on/storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ClientThreadGetMessagesRequest()
    .threadId('5')
    .account('email.account')
    .folder('INBOX')
    .storage('First Storage')
    .accountStorageFolder('email/account/location/on/storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ClientThreadGetMessagesRequest()
    ->thread_id('5')
    ->account('email.account')
    ->folder('INBOX')
    ->storage('First Storage')
    ->account_storage_folder('email/account/location/on/storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

