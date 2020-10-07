---
title: "DeleteFolderRequest"
type: docs
url: /reference-model-delete-folder-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.Folder.DeleteFolder](/email/reference-folder-api/#deletefolder) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**path** |**string**|Folder path e.g. '/folder' |
**storageName** |**string**|Storage name |[optional] 
**recursive** |**bool?**|Enable to delete folders, subfolders and files |[optional] [default to false]

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="delete_folder_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new DeleteFolderRequest
{ 
    Path = "/storage/path/to/folder",
    StorageName = "First Storage",
    Recursive = true
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
DeleteFolderRequest request = Models.deleteFolderRequest()
    .path("/storage/path/to/folder")
    .storageName("First Storage")
    .recursive(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.DeleteFolderRequest(
    path='/storage/path/to/folder',
    storage_name='First Storage',
    recursive=True)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = DeleteFolderRequest.new(
    path: '/storage/path/to/folder',
    storage_name: 'First Storage',
    recursive: true)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.DeleteFolderRequest()
    .path('/storage/path/to/folder')
    .storageName('First Storage')
    .recursive(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::DeleteFolderRequest()
    ->path('/storage/path/to/folder')
    ->storage_name('First Storage')
    ->recursive(true)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

