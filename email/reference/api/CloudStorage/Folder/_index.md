---
title: "Folder"
type: docs
url: /reference-folder-api/
weight: 1
---

Folder operations controller

## CopyFolder

Copy folder

{{< tabs tabTotal="6" tabID="copy_folder_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.CloudStorage.Folder.CopyFolderAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.cloudStorage().folder().copyFolder(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.cloud_storage.folder.copy_folder(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.cloud_storage.folder.copy_folder(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.cloudStorage.folder.copyFolder(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->cloudStorage()->folder()->copyFolder($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: CopyFolder method request.

Type: [**CopyFolderRequest**](/email/reference-model-copy-folder-request/).

{{< tabs tabTotal="6" tabID="copy_folder_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CopyFolderRequest
{ 
    SrcPath = "/storage/path/to/source/folder",
    DestPath = "/storage/path/to/destination/folder",
    SrcStorageName = "First Storage",
    DestStorageName = "Other Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CopyFolderRequest request = Models.copyFolderRequest()
    .srcPath("/storage/path/to/source/folder")
    .destPath("/storage/path/to/destination/folder")
    .srcStorageName("First Storage")
    .destStorageName("Other Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CopyFolderRequest(
    src_path='/storage/path/to/source/folder',
    dest_path='/storage/path/to/destination/folder',
    src_storage_name='First Storage',
    dest_storage_name='Other Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CopyFolderRequest.new(
    src_path: '/storage/path/to/source/folder',
    dest_path: '/storage/path/to/destination/folder',
    src_storage_name: 'First Storage',
    dest_storage_name: 'Other Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CopyFolderRequest()
    .srcPath('/storage/path/to/source/folder')
    .destPath('/storage/path/to/destination/folder')
    .srcStorageName('First Storage')
    .destStorageName('Other Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CopyFolderRequest()
    ->src_path('/storage/path/to/source/folder')
    ->dest_path('/storage/path/to/destination/folder')
    ->src_storage_name('First Storage')
    ->dest_storage_name('Other Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## CreateFolder

Create the folder

{{< tabs tabTotal="6" tabID="create_folder_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.CloudStorage.Folder.CreateFolderAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.cloudStorage().folder().createFolder(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.cloud_storage.folder.create_folder(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.cloud_storage.folder.create_folder(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.cloudStorage.folder.createFolder(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->cloudStorage()->folder()->createFolder($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: CreateFolder method request.

Type: [**CreateFolderRequest**](/email/reference-model-create-folder-request/).

{{< tabs tabTotal="6" tabID="create_folder_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CreateFolderRequest
{ 
    Path = "/storage/path/to/new/folder",
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CreateFolderRequest request = Models.createFolderRequest()
    .path("/storage/path/to/new/folder")
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CreateFolderRequest(
    path='/storage/path/to/new/folder',
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CreateFolderRequest.new(
    path: '/storage/path/to/new/folder',
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CreateFolderRequest()
    .path('/storage/path/to/new/folder')
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CreateFolderRequest()
    ->path('/storage/path/to/new/folder')
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## DeleteFolder

Delete folder

{{< tabs tabTotal="6" tabID="delete_folder_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.CloudStorage.Folder.DeleteFolderAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.cloudStorage().folder().deleteFolder(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.cloud_storage.folder.delete_folder(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.cloud_storage.folder.delete_folder(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.cloudStorage.folder.deleteFolder(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->cloudStorage()->folder()->deleteFolder($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: DeleteFolder method request.

Type: [**DeleteFolderRequest**](/email/reference-model-delete-folder-request/).

{{< tabs tabTotal="6" tabID="delete_folder_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new DeleteFolderRequest
{ 
    Path = "/storage/path/to/folder",
    StorageName = "First Storage",
    Recursive = true
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
DeleteFolderRequest request = Models.deleteFolderRequest()
    .path("/storage/path/to/folder")
    .storageName("First Storage")
    .recursive(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.DeleteFolderRequest(
    path='/storage/path/to/folder',
    storage_name='First Storage',
    recursive=True)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = DeleteFolderRequest.new(
    path: '/storage/path/to/folder',
    storage_name: 'First Storage',
    recursive: true)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.DeleteFolderRequest()
    .path('/storage/path/to/folder')
    .storageName('First Storage')
    .recursive(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::DeleteFolderRequest()
    ->path('/storage/path/to/folder')
    ->storage_name('First Storage')
    ->recursive(true)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## GetFilesList

Get all files and folders within a folder

Returns [**FilesList**](/email/reference-model-files-list/) model.

{{< tabs tabTotal="6" tabID="get_files_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.CloudStorage.Folder.GetFilesListAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
FilesList result = api.cloudStorage().folder().getFilesList(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.cloud_storage.folder.get_files_list(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.cloud_storage.folder.get_files_list(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.cloudStorage.folder.getFilesList(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->cloudStorage()->folder()->getFilesList($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: GetFilesList method request.

Type: [**GetFilesListRequest**](/email/reference-model-get-files-list-request/).

{{< tabs tabTotal="6" tabID="get_files_list_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new GetFilesListRequest
{ 
    Path = "/storage/path/to/folder",
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
GetFilesListRequest request = Models.getFilesListRequest()
    .path("/storage/path/to/folder")
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.GetFilesListRequest(
    path='/storage/path/to/folder',
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = GetFilesListRequest.new(
    path: '/storage/path/to/folder',
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.GetFilesListRequest()
    .path('/storage/path/to/folder')
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::GetFilesListRequest()
    ->path('/storage/path/to/folder')
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## MoveFolder

Move folder

{{< tabs tabTotal="6" tabID="move_folder_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.CloudStorage.Folder.MoveFolderAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.cloudStorage().folder().moveFolder(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.cloud_storage.folder.move_folder(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.cloud_storage.folder.move_folder(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.cloudStorage.folder.moveFolder(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->cloudStorage()->folder()->moveFolder($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: MoveFolder method request.

Type: [**MoveFolderRequest**](/email/reference-model-move-folder-request/).

{{< tabs tabTotal="6" tabID="move_folder_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MoveFolderRequest
{ 
    SrcPath = "/storage/path/to/source/folder",
    DestPath = "/storage/path/to/destination/folder",
    SrcStorageName = "First Storage",
    DestStorageName = "Other Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MoveFolderRequest request = Models.moveFolderRequest()
    .srcPath("/storage/path/to/source/folder")
    .destPath("/storage/path/to/destination/folder")
    .srcStorageName("First Storage")
    .destStorageName("Other Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MoveFolderRequest(
    src_path='/storage/path/to/source/folder',
    dest_path='/storage/path/to/destination/folder',
    src_storage_name='First Storage',
    dest_storage_name='Other Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MoveFolderRequest.new(
    src_path: '/storage/path/to/source/folder',
    dest_path: '/storage/path/to/destination/folder',
    src_storage_name: 'First Storage',
    dest_storage_name: 'Other Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.MoveFolderRequest()
    .srcPath('/storage/path/to/source/folder')
    .destPath('/storage/path/to/destination/folder')
    .srcStorageName('First Storage')
    .destStorageName('Other Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::MoveFolderRequest()
    ->src_path('/storage/path/to/source/folder')
    ->dest_path('/storage/path/to/destination/folder')
    ->src_storage_name('First Storage')
    ->dest_storage_name('Other Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

## More APIs
See more APIs:
{{< list-of-articles-in-this-section >}}
