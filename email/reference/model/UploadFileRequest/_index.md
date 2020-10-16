---
title: "UploadFileRequest"
type: docs
url: /reference-model-upload-file-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.File.UploadFile](/email/reference-file-api/#uploadfile) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**path** |**string**|Path where to upload including filename and extension e.g. /file.ext or /Folder 1/file.ext             If the content is multipart and path does not contains the file name it tries to get them from filename parameter             from Content-Disposition header.              |
**file** |**System.IO.Stream**|File to upload |
**storageName** |**string**|Storage name |[optional] 

## Example

{{< tabs tabTotal="6" tabID="upload_file_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

