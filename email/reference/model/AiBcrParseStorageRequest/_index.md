---
title: "AiBcrParseStorageRequest"
type: docs
url: /reference-model-ai-bcr-parse-storage-request/
weight: 1
---
Parse business card images from Storage request             

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**OutFolder** | [**StorageFolderLocation**](/email/reference-model-storage-folder-location/) | Parse output folder location on storage              | 
**Images** | [**List&lt;AiBcrImageStorageFile&gt;**](/email/reference-model-ai-bcr-image-storage-file/) | Images to parse.              | 
**Options** | [**AiBcrOptions**](/email/reference-model-ai-bcr-options/) | Recognition options.              | [optional] 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="ai_bcr_parse_storage_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var aiBcrParseStorageRequest = new AiBcrParseStorageRequest
{
    OutFolder = new StorageFolderLocation
    {
        Storage = "First Storage",
        FolderPath = "VCard/files/produced/by/parser/will/be/placed/here"
    },
    Images = new List<AiBcrImageStorageFile>
    {
        new AiBcrImageStorageFile
        {
            File = new StorageFileLocation
            {
                FileName = "VCardScanImage.jpg",
                Storage = "First Storage",
                FolderPath = "image/location/on/storage"
            },
            IsSingle = true
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiBcrParseStorageRequest aiBcrParseStorageRequest = Models.aiBcrParseStorageRequest()
    .outFolder(Models.storageFolderLocation()
        .storage("First Storage")
        .folderPath("VCard/files/produced/by/parser/will/be/placed/here")
        .build())
    .images(Arrays.<AiBcrImageStorageFile>asList(
        Models.aiBcrImageStorageFile()
            .file(Models.storageFileLocation()
                .fileName("VCardScanImage.jpg")
                .storage("First Storage")
                .folderPath("image/location/on/storage")
                .build())
            .isSingle(true)
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
ai_bcr_parse_storage_request = models.AiBcrParseStorageRequest(
    out_folder=models.StorageFolderLocation(
        storage='First Storage',
        folder_path='VCard/files/produced/by/parser/will/be/placed/here'),
    images=[
        models.AiBcrImageStorageFile(
            file=models.StorageFileLocation(
                file_name='VCardScanImage.jpg',
                storage='First Storage',
                folder_path='image/location/on/storage'),
            is_single=True)])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
ai_bcr_parse_storage_request = AiBcrParseStorageRequest.new(
  out_folder: StorageFolderLocation.new(
    storage: 'First Storage',
    folder_path: 'VCard/files/produced/by/parser/will/be/placed/here'),
  images: [
    AiBcrImageStorageFile.new(
      file: StorageFileLocation.new(
        file_name: 'VCardScanImage.jpg',
        storage: 'First Storage',
        folder_path: 'image/location/on/storage'),
      is_single: true)])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let aiBcrParseStorageRequest = Models.aiBcrParseStorageRequest()
    .outFolder(Models.storageFolderLocation()
        .storage('First Storage')
        .folderPath('VCard/files/produced/by/parser/will/be/placed/here')
        .build())
    .images([
        Models.aiBcrImageStorageFile()
            .file(Models.storageFileLocation()
                .fileName('VCardScanImage.jpg')
                .storage('First Storage')
                .folderPath('image/location/on/storage')
                .build())
            .isSingle(true)
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$aiBcrParseStorageRequest = Models::aiBcrParseStorageRequest()
    ->outFolder(Models::storageFolderLocation()
        ->storage('First Storage')
        ->folderPath('VCard/files/produced/by/parser/will/be/placed/here')
        ->build())
    ->images(array(
        Models::aiBcrImageStorageFile()
            ->file(Models::storageFileLocation()
                ->fileName('VCardScanImage.jpg')
                ->storage('First Storage')
                ->folderPath('image/location/on/storage')
                ->build())
            ->isSingle(true)
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

