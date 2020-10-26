---
title: "MoveFileRequest"
type: docs
url: /reference-model-move-file-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.File.MoveFile](/email/reference-file-api/#movefile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**srcPath** |**string**|Source file path e.g. '/src.ext' |
**destPath** |**string**|Destination file path e.g. '/dest.ext' |
**srcStorageName** |**string**|Source storage name |[optional] 
**destStorageName** |**string**|Destination storage name |[optional] 
**versionId** |**string**|File version ID to move |[optional] 

## Example

{{< tabs tabTotal="6" tabID="move_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

