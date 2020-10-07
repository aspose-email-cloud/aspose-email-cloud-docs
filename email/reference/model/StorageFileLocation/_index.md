---
title: "StorageFileLocation"
type: docs
url: /reference-model-storage-file-location/
weight: 1
---
A storage file location information             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**FileName** | **string** | A file name in storage              | 

Parent class: [StorageFolderLocation](/email/reference-model-storage-folder-location/)

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="storage_file_location_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var storageFileLocation = new StorageFileLocation
{
    FileName = "fileOnStorage.txt",
    Storage = "First Storage",
    FolderPath = "file/location/folder/on/storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
StorageFileLocation storageFileLocation = Models.storageFileLocation()
    .fileName("fileOnStorage.txt")
    .storage("First Storage")
    .folderPath("file/location/folder/on/storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
storage_file_location = models.StorageFileLocation(
    file_name='fileOnStorage.txt',
    storage='First Storage',
    folder_path='file/location/folder/on/storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
storage_file_location = StorageFileLocation.new(
  file_name: 'fileOnStorage.txt',
  storage: 'First Storage',
  folder_path: 'file/location/folder/on/storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let storageFileLocation = Models.storageFileLocation()
    .fileName('fileOnStorage.txt')
    .storage('First Storage')
    .folderPath('file/location/folder/on/storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$storageFileLocation = Models::storageFileLocation()
    ->fileName('fileOnStorage.txt')
    ->storage('First Storage')
    ->folderPath('file/location/folder/on/storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

