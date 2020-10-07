---
title: "FilesList"
type: docs
url: /reference-model-files-list/
weight: 1
---
Files list

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Value** | [**List&lt;StorageFile&gt;**](/email/reference-model-storage-file/) | Files and folders contained by folder StorageFile. | [optional] 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="files_list_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var filesList = new FilesList
{
    Value = new List<StorageFile>
    {
        new StorageFile
        {
            Name = "file.ext",
            ModifiedDate = DateTime.Today,
            Size = 1024,
            Path = "/path/to/file/on/storage"
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
FilesList filesList = Models.filesList()
    .value(Arrays.<StorageFile>asList(
        Models.storageFile()
            .name("file.ext")
            .modifiedDate(Calendar.getInstance().getTime())
            .size(1024)
            .path("/path/to/file/on/storage")
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
files_list = models.FilesList(
    value=[
        models.StorageFile(
            name='file.ext',
            modified_date=datetime.today(),
            size=1024,
            path='/path/to/file/on/storage')])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
files_list = FilesList.new(
  value: [
    StorageFile.new(
      name: 'file.ext',
      modified_date: DateTime.now,
      size: 1024,
      path: '/path/to/file/on/storage')])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let filesList = Models.filesList()
    .value([
        Models.storageFile()
            .name('file.ext')
            .modifiedDate(new Date())
            .size(1024)
            .path('/path/to/file/on/storage')
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$filesList = Models::filesList()
    ->value(array(
        Models::storageFile()
            ->name('file.ext')
            ->modifiedDate(new DateTime())
            ->size(1024)
            ->path('/path/to/file/on/storage')
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

