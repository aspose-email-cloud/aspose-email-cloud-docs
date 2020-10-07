---
title: "File"
type: docs
url: /reference-file-api/
weight: 1
---

File operations controller

## CopyFile

Copy file

{{< tabs tabTotal="6" tabID="copy_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.CloudStorage.File.CopyFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.cloudStorage().file().copyFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.cloud_storage.file.copy_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.cloud_storage.file.copy_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.cloudStorage.file.copyFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->cloudStorage()->file()->copyFile($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: CopyFile method request.

Type: [**CopyFileRequest**](/email/reference-model-copy-file-request/).

{{< tabs tabTotal="6" tabID="copy_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CopyFileRequest
{ 
    SrcPath = "/storage/path/to/source/file.ext",
    DestPath = "/storage/path/to/destination/file.ext",
    SrcStorageName = "First Storage",
    DestStorageName = "Other Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CopyFileRequest request = Models.copyFileRequest()
    .srcPath("/storage/path/to/source/file.ext")
    .destPath("/storage/path/to/destination/file.ext")
    .srcStorageName("First Storage")
    .destStorageName("Other Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CopyFileRequest(
    src_path='/storage/path/to/source/file.ext',
    dest_path='/storage/path/to/destination/file.ext',
    src_storage_name='First Storage',
    dest_storage_name='Other Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CopyFileRequest.new(
    src_path: '/storage/path/to/source/file.ext',
    dest_path: '/storage/path/to/destination/file.ext',
    src_storage_name: 'First Storage',
    dest_storage_name: 'Other Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CopyFileRequest()
    .srcPath('/storage/path/to/source/file.ext')
    .destPath('/storage/path/to/destination/file.ext')
    .srcStorageName('First Storage')
    .destStorageName('Other Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CopyFileRequest()
    ->src_path('/storage/path/to/source/file.ext')
    ->dest_path('/storage/path/to/destination/file.ext')
    ->src_storage_name('First Storage')
    ->dest_storage_name('Other Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## DeleteFile

Delete file

{{< tabs tabTotal="6" tabID="delete_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.CloudStorage.File.DeleteFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.cloudStorage().file().deleteFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.cloud_storage.file.delete_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.cloud_storage.file.delete_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.cloudStorage.file.deleteFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->cloudStorage()->file()->deleteFile($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: DeleteFile method request.

Type: [**DeleteFileRequest**](/email/reference-model-delete-file-request/).

{{< tabs tabTotal="6" tabID="delete_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new DeleteFileRequest
{ 
    Path = "/storage/path/to/file.ext",
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
DeleteFileRequest request = Models.deleteFileRequest()
    .path("/storage/path/to/file.ext")
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.DeleteFileRequest(
    path='/storage/path/to/file.ext',
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = DeleteFileRequest.new(
    path: '/storage/path/to/file.ext',
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.DeleteFileRequest()
    .path('/storage/path/to/file.ext')
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::DeleteFileRequest()
    ->path('/storage/path/to/file.ext')
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## DownloadFile

Download file

Returns a file.

{{< tabs tabTotal="6" tabID="download_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.CloudStorage.File.DownloadFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
byte[] result = api.cloudStorage().file().downloadFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.cloud_storage.file.download_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.cloud_storage.file.download_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.cloudStorage.file.downloadFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->cloudStorage()->file()->downloadFile($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: DownloadFile method request.

Type: [**DownloadFileRequest**](/email/reference-model-download-file-request/).

{{< tabs tabTotal="6" tabID="download_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new DownloadFileRequest
{ 
    Path = "/storage/path/to/file.ext",
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
DownloadFileRequest request = Models.downloadFileRequest()
    .path("/storage/path/to/file.ext")
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.DownloadFileRequest(
    path='/storage/path/to/file.ext',
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = DownloadFileRequest.new(
    path: '/storage/path/to/file.ext',
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.DownloadFileRequest()
    .path('/storage/path/to/file.ext')
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::DownloadFileRequest()
    ->path('/storage/path/to/file.ext')
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## MoveFile

Move file

{{< tabs tabTotal="6" tabID="move_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
await api.CloudStorage.File.MoveFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
api.cloudStorage().file().moveFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
api.cloud_storage.file.move_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
api.cloud_storage.file.move_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
await api.cloudStorage.file.moveFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$api->cloudStorage()->file()->moveFile($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: MoveFile method request.

Type: [**MoveFileRequest**](/email/reference-model-move-file-request/).

{{< tabs tabTotal="6" tabID="move_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new MoveFileRequest
{ 
    SrcPath = "/storage/path/to/source/file.ext",
    DestPath = "/storage/path/to/destination/file.ext",
    SrcStorageName = "First Storage",
    DestStorageName = "Other Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
MoveFileRequest request = Models.moveFileRequest()
    .srcPath("/storage/path/to/source/file.ext")
    .destPath("/storage/path/to/destination/file.ext")
    .srcStorageName("First Storage")
    .destStorageName("Other Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.MoveFileRequest(
    src_path='/storage/path/to/source/file.ext',
    dest_path='/storage/path/to/destination/file.ext',
    src_storage_name='First Storage',
    dest_storage_name='Other Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = MoveFileRequest.new(
    src_path: '/storage/path/to/source/file.ext',
    dest_path: '/storage/path/to/destination/file.ext',
    src_storage_name: 'First Storage',
    dest_storage_name: 'Other Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.MoveFileRequest()
    .srcPath('/storage/path/to/source/file.ext')
    .destPath('/storage/path/to/destination/file.ext')
    .srcStorageName('First Storage')
    .destStorageName('Other Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::MoveFileRequest()
    ->src_path('/storage/path/to/source/file.ext')
    ->dest_path('/storage/path/to/destination/file.ext')
    ->src_storage_name('First Storage')
    ->dest_storage_name('Other Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}
## UploadFile

Upload file

Returns [**FilesUploadResult**](/email/reference-model-files-upload-result/) model.

{{< tabs tabTotal="6" tabID="upload_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.CloudStorage.File.UploadFileAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
FilesUploadResult result = api.cloudStorage().file().uploadFile(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.cloud_storage.file.upload_file(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.cloud_storage.file.upload_file(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.cloudStorage.file.uploadFile(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->cloudStorage()->file()->uploadFile($request);
```

{{< /tab >}}

{{< /tabs >}}

Input parameters:

{{< expand-list title="request" >}}

Description: UploadFile method request.

Type: [**UploadFileRequest**](/email/reference-model-upload-file-request/).

{{< tabs tabTotal="6" tabID="upload_file_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new UploadFileRequest
{ 
    Path = "/storage/path/to/file.ext",
    File = new MemoryStream(File.ReadAllBytes("/local/file/system/path/to/file.ext")),
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
UploadFileRequest request = Models.uploadFileRequest()
    .path("/storage/path/to/file.ext")
    .file(IOUtils.toByteArray(new FileInputStream("/local/file/system/path/to/file.ext")))
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.UploadFileRequest(
    path='/storage/path/to/file.ext',
    file='/local/file/system/path/to/file.ext',
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = UploadFileRequest.new(
    path: '/storage/path/to/file.ext',
    file: File.new('/local/file/system/path/to/file.ext'),
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.UploadFileRequest()
    .path('/storage/path/to/file.ext')
    .file(fs.readFileSync('/local/file/system/path/to/file.ext'))
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::UploadFileRequest()
    ->path('/storage/path/to/file.ext')
    ->file(new SplFileObject('/local/file/system/path/to/file.ext'))
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

## More APIs
See more APIs:
{{< list-of-articles-in-this-section >}}
