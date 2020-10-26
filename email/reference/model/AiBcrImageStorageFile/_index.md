---
title: "AiBcrImageStorageFile"
type: docs
url: /reference-model-ai-bcr-image-storage-file/
weight: 1
---
Image from storage for recognition             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**File** | [**StorageFileLocation**](/email/reference-model-storage-file-location/) | Image location              | 

Parent class: [AiBcrImage](/email/reference-model-ai-bcr-image/)

## Example

{{< tabs tabTotal="6" tabID="ai_bcr_image_storage_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var aiBcrImageStorageFile = new AiBcrImageStorageFile
{
    File = new StorageFileLocation
    {
        FileName = "VCardScanImage.jpg",
        Storage = "First Storage",
        FolderPath = "image/location/on/storage"
    },
    IsSingle = true
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiBcrImageStorageFile aiBcrImageStorageFile = Models.aiBcrImageStorageFile()
    .file(Models.storageFileLocation()
        .fileName("VCardScanImage.jpg")
        .storage("First Storage")
        .folderPath("image/location/on/storage")
        .build())
    .isSingle(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
ai_bcr_image_storage_file = models.AiBcrImageStorageFile(
    file=models.StorageFileLocation(
        file_name='VCardScanImage.jpg',
        storage='First Storage',
        folder_path='image/location/on/storage'),
    is_single=True)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
ai_bcr_image_storage_file = AiBcrImageStorageFile.new(
  file: StorageFileLocation.new(
    file_name: 'VCardScanImage.jpg',
    storage: 'First Storage',
    folder_path: 'image/location/on/storage'),
  is_single: true)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let aiBcrImageStorageFile = Models.aiBcrImageStorageFile()
    .file(Models.storageFileLocation()
        .fileName('VCardScanImage.jpg')
        .storage('First Storage')
        .folderPath('image/location/on/storage')
        .build())
    .isSingle(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$aiBcrImageStorageFile = Models::aiBcrImageStorageFile()
    ->file(Models::storageFileLocation()
        ->fileName('VCardScanImage.jpg')
        ->storage('First Storage')
        ->folderPath('image/location/on/storage')
        ->build())
    ->isSingle(true)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

