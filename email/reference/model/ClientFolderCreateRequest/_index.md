---
title: "ClientFolderCreateRequest"
type: docs
url: /reference-model-client-folder-create-request/
weight: 1
---
Email Client create folder request.             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**ParentFolder** | **string** | Path to parent folder.              | [optional] 
**FolderName** | **string** | Folder name.              | 

Parent class: [ClientAccountBaseRequest](/email/reference-model-client-account-base-request/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="client_folder_create_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var clientFolderCreateRequest = new ClientFolderCreateRequest
{
    ParentFolder = "INBOX/SubFolder/ParentFolder",
    FolderName = "NewFolder",
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
ClientFolderCreateRequest clientFolderCreateRequest = Models.clientFolderCreateRequest()
    .parentFolder("INBOX/SubFolder/ParentFolder")
    .folderName("NewFolder")
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
client_folder_create_request = models.ClientFolderCreateRequest(
    parent_folder='INBOX/SubFolder/ParentFolder',
    folder_name='NewFolder',
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
client_folder_create_request = ClientFolderCreateRequest.new(
  parent_folder: 'INBOX/SubFolder/ParentFolder',
  folder_name: 'NewFolder',
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let clientFolderCreateRequest = Models.clientFolderCreateRequest()
    .parentFolder('INBOX/SubFolder/ParentFolder')
    .folderName('NewFolder')
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
$clientFolderCreateRequest = Models::clientFolderCreateRequest()
    ->parentFolder('INBOX/SubFolder/ParentFolder')
    ->folderName('NewFolder')
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

