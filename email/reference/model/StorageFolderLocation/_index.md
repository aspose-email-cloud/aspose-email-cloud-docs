---
title: "StorageFolderLocation"
type: docs
url: /reference-model-storage-folder-location/
weight: 1
---
A storage folder location information             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Storage** | **string** | A storage name              | [optional] 
**FolderPath** | **string** | A path to a folder in specified storage              | [optional] 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="storage_folder_location_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var storageFolderLocation = new StorageFolderLocation
{
    Storage = "First Storage",
    FolderPath = "folder/on/storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
StorageFolderLocation storageFolderLocation = Models.storageFolderLocation()
    .storage("First Storage")
    .folderPath("folder/on/storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
storage_folder_location = models.StorageFolderLocation(
    storage='First Storage',
    folder_path='folder/on/storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
storage_folder_location = StorageFolderLocation.new(
  storage: 'First Storage',
  folder_path: 'folder/on/storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let storageFolderLocation = Models.storageFolderLocation()
    .storage('First Storage')
    .folderPath('folder/on/storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$storageFolderLocation = Models::storageFolderLocation()
    ->storage('First Storage')
    ->folderPath('folder/on/storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

