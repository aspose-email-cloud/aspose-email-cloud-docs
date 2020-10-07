---
title: "CopyFileRequest"
type: docs
url: /reference-model-copy-file-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.File.CopyFile](/email/reference-file-api/#copyfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**srcPath** |**string**|Source file path e.g. '/folder/file.ext' |
**destPath** |**string**|Destination file path |
**srcStorageName** |**string**|Source storage name |[optional] 
**destStorageName** |**string**|Destination storage name |[optional] 
**versionId** |**string**|File version ID to copy |[optional] 

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="copy_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

