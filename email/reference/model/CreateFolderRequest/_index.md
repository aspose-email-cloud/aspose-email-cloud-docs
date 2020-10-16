---
title: "CreateFolderRequest"
type: docs
url: /reference-model-create-folder-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.Folder.CreateFolder](/email/reference-folder-api/#createfolder) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**path** |**string**|Folder path to create e.g. 'folder_1/folder_2/' |
**storageName** |**string**|Storage name |[optional] 

## Example

{{< tabs tabTotal="6" tabID="create_folder_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new CreateFolderRequest
{ 
    Path = "/storage/path/to/new/folder",
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
CreateFolderRequest request = Models.createFolderRequest()
    .path("/storage/path/to/new/folder")
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.CreateFolderRequest(
    path='/storage/path/to/new/folder',
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = CreateFolderRequest.new(
    path: '/storage/path/to/new/folder',
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.CreateFolderRequest()
    .path('/storage/path/to/new/folder')
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::CreateFolderRequest()
    ->path('/storage/path/to/new/folder')
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

