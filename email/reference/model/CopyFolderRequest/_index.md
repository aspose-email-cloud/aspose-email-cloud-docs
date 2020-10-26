---
title: "CopyFolderRequest"
type: docs
url: /reference-model-copy-folder-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.Folder.CopyFolder](/email/reference-folder-api/#copyfolder) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**srcPath** |**string**|Source folder path e.g. '/src' |
**destPath** |**string**|Destination folder path e.g. '/dst' |
**srcStorageName** |**string**|Source storage name |[optional] 
**destStorageName** |**string**|Destination storage name |[optional] 

## Example

{{< tabs tabTotal="6" tabID="copy_folder_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

