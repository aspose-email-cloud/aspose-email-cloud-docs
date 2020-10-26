---
title: "MoveFolderRequest"
type: docs
url: /reference-model-move-folder-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.Folder.MoveFolder](/email/reference-folder-api/#movefolder) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**srcPath** |**string**|Folder path to move e.g. '/folder' |
**destPath** |**string**|Destination folder path to move to e.g '/dst' |
**srcStorageName** |**string**|Source storage name |[optional] 
**destStorageName** |**string**|Destination storage name |[optional] 

## Example

{{< tabs tabTotal="6" tabID="move_folder_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

