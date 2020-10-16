---
title: "StorageFileLocationList"
type: docs
url: /reference-model-storage-file-location-list/
weight: 1
---
List of files located on storage.             

Properties:

Class has no properties

Parent class: [ListResponseOfStorageFileLocation](/email/reference-model-list-response-of-storage-file-location/)

## Example

{{< tabs tabTotal="6" tabID="storage_file_location_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var storageFileLocationList = new StorageFileLocationList
{
    Value = new List<StorageFileLocation>
    {
        new StorageFileLocation
        {
            FileName = "fileOnStorage.txt",
            Storage = "First Storage",
            FolderPath = "file/location/folder/on/storage"
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
StorageFileLocationList storageFileLocationList = Models.storageFileLocationList()
    .value(Arrays.<StorageFileLocation>asList(
        Models.storageFileLocation()
            .fileName("fileOnStorage.txt")
            .storage("First Storage")
            .folderPath("file/location/folder/on/storage")
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
storage_file_location_list = models.StorageFileLocationList(
    value=[
        models.StorageFileLocation(
            file_name='fileOnStorage.txt',
            storage='First Storage',
            folder_path='file/location/folder/on/storage')])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
storage_file_location_list = StorageFileLocationList.new(
  value: [
    StorageFileLocation.new(
      file_name: 'fileOnStorage.txt',
      storage: 'First Storage',
      folder_path: 'file/location/folder/on/storage')])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let storageFileLocationList = Models.storageFileLocationList()
    .value([
        Models.storageFileLocation()
            .fileName('fileOnStorage.txt')
            .storage('First Storage')
            .folderPath('file/location/folder/on/storage')
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$storageFileLocationList = Models::storageFileLocationList()
    ->value(array(
        Models::storageFileLocation()
            ->fileName('fileOnStorage.txt')
            ->storage('First Storage')
            ->folderPath('file/location/folder/on/storage')
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

