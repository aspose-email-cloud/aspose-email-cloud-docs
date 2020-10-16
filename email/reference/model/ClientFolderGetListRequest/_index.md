---
title: "ClientFolderGetListRequest"
type: docs
url: /reference-model-client-folder-get-list-request/
weight: 2
---

Request model for [EmailCloud.Client.Folder.GetList](/email/reference-client-folder-api/#getlist) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**account** |**string**|Email account |
**storage** |**string**|Storage name where account file located |[optional] 
**accountStorageFolder** |**string**|Folder in storage where account file located |[optional] 
**parentFolder** |**string**|Folder in which subfolders should be listed |[optional] 

## Example

{{< tabs tabTotal="6" tabID="client_folder_get_list_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientFolderGetListRequest
{ 
    Account = "email.multi.account",
    Storage = "First Storage",
    AccountStorageFolder = "email/account/location/on/storage",
    ParentFolder = "INBOX"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ClientFolderGetListRequest request = Models.clientFolderGetListRequest()
    .account("email.multi.account")
    .storage("First Storage")
    .accountStorageFolder("email/account/location/on/storage")
    .parentFolder("INBOX")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ClientFolderGetListRequest(
    account='email.multi.account',
    storage='First Storage',
    account_storage_folder='email/account/location/on/storage',
    parent_folder='INBOX')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientFolderGetListRequest.new(
    account: 'email.multi.account',
    storage: 'First Storage',
    account_storage_folder: 'email/account/location/on/storage',
    parent_folder: 'INBOX')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ClientFolderGetListRequest()
    .account('email.multi.account')
    .storage('First Storage')
    .accountStorageFolder('email/account/location/on/storage')
    .parentFolder('INBOX')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ClientFolderGetListRequest()
    ->account('email.multi.account')
    ->storage('First Storage')
    ->account_storage_folder('email/account/location/on/storage')
    ->parent_folder('INBOX')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

