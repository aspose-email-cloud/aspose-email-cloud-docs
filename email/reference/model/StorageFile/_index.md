---
title: "StorageFile"
type: docs
url: /reference-model-storage-file/
weight: 1
---
File or folder information

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Name** | **string** | File or folder name. | [optional] 
**IsFolder** | **bool?** | True if it is a folder. | 
**ModifiedDate** | **DateTime?** | File or folder last modified DateTime. | [optional] 
**Size** | **long?** | File or folder size. | 
**Path** | **string** | File or folder path. | [optional] 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="storage_file_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var storageFile = new StorageFile
{
    Name = "file.ext",
    ModifiedDate = DateTime.Today,
    Size = 4096,
    Path = "/storage/path/to"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
StorageFile storageFile = Models.storageFile()
    .name("file.ext")
    .modifiedDate(Calendar.getInstance().getTime())
    .size(4096)
    .path("/storage/path/to")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
storage_file = models.StorageFile(
    name='file.ext',
    modified_date=datetime.today(),
    size=4096,
    path='/storage/path/to')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
storage_file = StorageFile.new(
  name: 'file.ext',
  modified_date: DateTime.now,
  size: 4096,
  path: '/storage/path/to')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let storageFile = Models.storageFile()
    .name('file.ext')
    .modifiedDate(new Date())
    .size(4096)
    .path('/storage/path/to')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$storageFile = Models::storageFile()
    ->name('file.ext')
    ->modifiedDate(new DateTime())
    ->size(4096)
    ->path('/storage/path/to')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

