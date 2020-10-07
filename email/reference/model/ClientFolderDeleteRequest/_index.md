---
title: "ClientFolderDeleteRequest"
type: docs
url: /reference-model-client-folder-delete-request/
weight: 1
---
Email client delete folder request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Folder** | **string** | Path to folder to delete.              | 

Parent class: [ClientAccountBaseRequest](/email/reference-model-client-account-base-request/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="client_folder_delete_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var clientFolderDeleteRequest = new ClientFolderDeleteRequest
{
    Folder = "INBOX/SubFolder/FolderToDelete",
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
ClientFolderDeleteRequest clientFolderDeleteRequest = Models.clientFolderDeleteRequest()
    .folder("INBOX/SubFolder/FolderToDelete")
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
client_folder_delete_request = models.ClientFolderDeleteRequest(
    folder='INBOX/SubFolder/FolderToDelete',
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
client_folder_delete_request = ClientFolderDeleteRequest.new(
  folder: 'INBOX/SubFolder/FolderToDelete',
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let clientFolderDeleteRequest = Models.clientFolderDeleteRequest()
    .folder('INBOX/SubFolder/FolderToDelete')
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
$clientFolderDeleteRequest = Models::clientFolderDeleteRequest()
    ->folder('INBOX/SubFolder/FolderToDelete')
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

