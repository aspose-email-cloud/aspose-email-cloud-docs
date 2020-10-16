---
title: "DeleteFileRequest"
type: docs
url: /reference-model-delete-file-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.File.DeleteFile](/email/reference-file-api/#deletefile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**path** |**string**|File path e.g. '/folder/file.ext' |
**storageName** |**string**|Storage name |[optional] 
**versionId** |**string**|File version ID to delete |[optional] 

## Example

{{< tabs tabTotal="6" tabID="delete_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

