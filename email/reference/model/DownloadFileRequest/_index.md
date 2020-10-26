---
title: "DownloadFileRequest"
type: docs
url: /reference-model-download-file-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.File.DownloadFile](/email/reference-file-api/#downloadfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**path** |**string**|File path e.g. '/folder/file.ext' |
**storageName** |**string**|Storage name |[optional] 
**versionId** |**string**|File version ID to download |[optional] 

## Example

{{< tabs tabTotal="6" tabID="download_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

