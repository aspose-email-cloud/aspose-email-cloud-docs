---
title: "GetFileVersionsRequest"
type: docs
url: /reference-model-get-file-versions-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.Storage.GetFileVersions](/email/reference-storage-api/#getfileversions) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**path** |**string**|File path e.g. '/file.ext' |
**storageName** |**string**|Storage name |[optional] 

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="get_file_versions_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new GetFileVersionsRequest
{ 
    Path = "/storage/path/to/file.ext",
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
GetFileVersionsRequest request = Models.getFileVersionsRequest()
    .path("/storage/path/to/file.ext")
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.GetFileVersionsRequest(
    path='/storage/path/to/file.ext',
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = GetFileVersionsRequest.new(
    path: '/storage/path/to/file.ext',
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.GetFileVersionsRequest()
    .path('/storage/path/to/file.ext')
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::GetFileVersionsRequest()
    ->path('/storage/path/to/file.ext')
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

