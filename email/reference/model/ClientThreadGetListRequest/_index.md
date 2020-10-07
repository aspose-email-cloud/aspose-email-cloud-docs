---
title: "ClientThreadGetListRequest"
type: docs
url: /reference-model-client-thread-get-list-request/
weight: 2
---

Request model for [EmailCloud.Client.Thread.GetList](/email/reference-client-thread-api/#getlist) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**folder** |**string**|A folder in email account.              |
**account** |**string**|Email account |
**storage** |**string**|Storage name where account file located |[optional] 
**accountStorageFolder** |**string**|Folder in storage where account file located |[optional] 
**updateFolderCache** |**bool?**|This parameter is only used in accounts with CacheFile. If true - get new messages and update threads cache for given folder. If false, get only threads from cache without any calls to an email account              |[optional] [default to true]
**messagesCacheLimit** |**int?**|Limit messages cache size if CacheFile is used. Ignored in accounts without limits support              |[optional] [default to 200]

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="client_thread_get_list_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientThreadGetListRequest
{ 
    Folder = "INBOX/SubFolder",
    Account = "email.account",
    Storage = "First Storage",
    AccountStorageFolder = "email/account/location/on/storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientThreadGetListRequest request = Models.clientThreadGetListRequest()
    .folder("INBOX/SubFolder")
    .account("email.account")
    .storage("First Storage")
    .accountStorageFolder("email/account/location/on/storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientThreadGetListRequest(
    folder='INBOX/SubFolder',
    account='email.account',
    storage='First Storage',
    account_storage_folder='email/account/location/on/storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientThreadGetListRequest.new(
    folder: 'INBOX/SubFolder',
    account: 'email.account',
    storage: 'First Storage',
    account_storage_folder: 'email/account/location/on/storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ClientThreadGetListRequest()
    .folder('INBOX/SubFolder')
    .account('email.account')
    .storage('First Storage')
    .accountStorageFolder('email/account/location/on/storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ClientThreadGetListRequest()
    ->folder('INBOX/SubFolder')
    ->account('email.account')
    ->storage('First Storage')
    ->account_storage_folder('email/account/location/on/storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

