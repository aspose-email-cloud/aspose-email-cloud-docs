---
title: "GetFilesListRequest"
type: docs
url: /reference-model-get-files-list-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.Folder.GetFilesList](/email/reference-folder-api/#getfileslist) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**path** |**string**|Folder path e.g. '/folder' |
**storageName** |**string**|Storage name |[optional] 

## Example

{{< tabs tabTotal="6" tabID="get_files_list_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

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

