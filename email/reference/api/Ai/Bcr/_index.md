---
title: "Bcr"
type: docs
url: /reference-ai-bcr-api/
weight: 1
---

AI Business card recognition operations.

## Parse

Parse images to vCard document models. 
Returns [**ContactList**](/email/reference-model-contact-list/) model. Requires:

{{< expand-list title="request" >}}

Parse method request. Type: [**AiBcrParseRequest**](/email/reference-model-ai-bcr-parse-request/).

{{< tabs tabTotal="6" tabID="ai_bcr_parse_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiBcrParseRequest
{ 
    File = new MemoryStream(File.ReadAllBytes("/path/to/image.png")),
    Countries = "us",
    Languages = "en",
    IsSingle = true
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
AiBcrParseRequest request = Models.aiBcrParseRequest()
    .file(IOUtils.toByteArray(new FileInputStream("/path/to/image.png")))
    .countries("us")
    .languages("en")
    .isSingle(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.AiBcrParseRequest(
    file='/path/to/image.png',
    countries='us',
    languages='en',
    is_single=True)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = AiBcrParseRequest.new(
    file: File.new('/path/to/image.png'),
    countries: 'us',
    languages: 'en',
    is_single: true)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.AiBcrParseRequest()
    .file(fs.readFileSync('/path/to/image.png'))
    .countries('us')
    .languages('en')
    .isSingle(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::AiBcrParseRequest()
    ->file(new SplFileObject('/path/to/image.png'))
    ->countries('us')
    ->languages('en')
    ->is_single(true)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="ai_bcr_parse_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Ai.Bcr.ParseAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ContactList result = api.ai().bcr().parse(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.bcr.parse(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.ai.bcr.parse(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.ai.bcr.parse(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->ai()->bcr()->parse($request);
```

{{< /tab >}}

{{< /tabs >}}
## ParseStorage

Parse images from storage to vCard files. 
Returns [**StorageFileLocationList**](/email/reference-model-storage-file-location-list/) model. Requires:

{{< expand-list title="request" >}}

Request with images located on storage. Type: [**AiBcrParseStorageRequest**](/email/reference-model-ai-bcr-parse-storage-request/).

{{< tabs tabTotal="6" tabID="ai_bcr_parse_storage_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new AiBcrParseStorageRequest
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
AiBcrParseStorageRequest request = Models.aiBcrParseStorageRequest()
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
request = models.AiBcrParseStorageRequest(
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
request = AiBcrParseStorageRequest.new(
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
let request = Models.aiBcrParseStorageRequest()
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
$request = Models::aiBcrParseStorageRequest()
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

{{< tabs tabTotal="6" tabID="ai_bcr_parse_storage_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.Ai.Bcr.ParseStorageAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
StorageFileLocationList result = api.ai().bcr().parseStorage(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.ai.bcr.parse_storage(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.ai.bcr.parse_storage(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.ai.bcr.parseStorage(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->ai()->bcr()->parseStorage($request);
```

{{< /tab >}}

{{< /tabs >}}

## More APIs

{{< list-of-articles-in-this-section >}}
