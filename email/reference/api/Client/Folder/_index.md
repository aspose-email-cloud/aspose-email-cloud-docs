---
title: "Folder"
type: docs
url: /reference-client-folder-api/
weight: 1
---

Email client folder operations.

## Create

Create new folder in email account             

{{< tabs tabTotal="6" tabID="client_folder_create_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Client.Folder.CreateAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().folder().create(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.client.folder.create(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.client.folder.create(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.client.folder.create(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->folder()->create($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: Create folder request

Type: [**ClientFolderCreateRequest**](/email/reference-model-client-folder-create-request/).

{{< tabs tabTotal="6" tabID="client_folder_create_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientFolderCreateRequest
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
ClientFolderCreateRequest request = Models.clientFolderCreateRequest()
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
request = models.ClientFolderCreateRequest(
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
request = ClientFolderCreateRequest.new(
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
let request = Models.clientFolderCreateRequest()
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
$request = Models::clientFolderCreateRequest()
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
## Delete

Delete a folder in email account             

{{< tabs tabTotal="6" tabID="client_folder_delete_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.Client.Folder.DeleteAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.client().folder().delete(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.client.folder.delete(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.client.folder.delete(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.client.folder.delete(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->client()->folder()->delete($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: Delete folder request

Type: [**ClientFolderDeleteRequest**](/email/reference-model-client-folder-delete-request/).

{{< tabs tabTotal="6" tabID="client_folder_delete_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ClientFolderDeleteRequest
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
ClientFolderDeleteRequest request = Models.clientFolderDeleteRequest()
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
request = models.ClientFolderDeleteRequest(
    folder='INBOX/SubFolder/FolderToDelete',
    account_location=models.StorageFileLocation(
        file_name='email.account',
        storage='First Storage',
        folder_path='file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ClientFolderDeleteRequest.new(
  folder: 'INBOX/SubFolder/FolderToDelete',
  account_location: StorageFileLocation.new(
    file_name: 'email.account',
    storage: 'First Storage',
    folder_path: 'file/location/folder/on/storage'))
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.clientFolderDeleteRequest()
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
$request = Models::clientFolderDeleteRequest()
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
## GetList

Get folders list in email account             

Returns [**MailServerFolderList**](/email/reference-model-mail-server-folder-list/) model.

{{< tabs tabTotal="6" tabID="client_folder_get_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Client.Folder.GetListAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MailServerFolderList result = api.client().folder().getList(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.client.folder.get_list(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.client.folder.get_list(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.client.folder.getList(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->client()->folder()->getList($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: GetList method request.

Type: [**ClientFolderGetListRequest**](/email/reference-model-client-folder-get-list-request/).

{{< tabs tabTotal="6" tabID="client_folder_get_list_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

{{< /expand-list >}}

## More APIs
See more APIs:
{{< list-of-articles-in-this-section >}}
