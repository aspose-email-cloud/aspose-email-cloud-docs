---
title: "FileVersions"
type: docs
url: /reference-model-file-versions/
weight: 1
---
File versions FileVersion.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Value** | [**List&lt;FileVersion&gt;**](/email/reference-model-file-version/) | File versions FileVersion. | [optional] 


## Example

{{< tabs tabTotal="6" tabID="file_versions_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var fileVersions = new FileVersions
{
    Value = new List<FileVersion>
    {
        new FileVersion
        {
            VersionId = "d5afd857-8797-4ca0-b806-a03fdfc3831f",
            IsLatest = true,
            Name = "file.ext",
            ModifiedDate = DateTime.Today,
            Size = 4096,
            Path = "/storage/path/to"
        }
    }
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
FileVersions fileVersions = Models.fileVersions()
    .value(Arrays.<FileVersion>asList(
        Models.fileVersion()
            .versionId("d5afd857-8797-4ca0-b806-a03fdfc3831f")
            .isLatest(true)
            .name("file.ext")
            .modifiedDate(Calendar.getInstance().getTime())
            .size(4096)
            .path("/storage/path/to")
            .build()))
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
file_versions = models.FileVersions(
    value=[
        models.FileVersion(
            version_id='d5afd857-8797-4ca0-b806-a03fdfc3831f',
            is_latest=True,
            name='file.ext',
            modified_date=datetime.today(),
            size=4096,
            path='/storage/path/to')])
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
file_versions = FileVersions.new(
  value: [
    FileVersion.new(
      version_id: 'd5afd857-8797-4ca0-b806-a03fdfc3831f',
      is_latest: true,
      name: 'file.ext',
      modified_date: DateTime.now,
      size: 4096,
      path: '/storage/path/to')])
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let fileVersions = Models.fileVersions()
    .value([
        Models.fileVersion()
            .versionId('d5afd857-8797-4ca0-b806-a03fdfc3831f')
            .isLatest(true)
            .name('file.ext')
            .modifiedDate(new Date())
            .size(4096)
            .path('/storage/path/to')
            .build()])
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$fileVersions = Models::fileVersions()
    ->value(array(
        Models::fileVersion()
            ->versionId('d5afd857-8797-4ca0-b806-a03fdfc3831f')
            ->isLatest(true)
            ->name('file.ext')
            ->modifiedDate(new DateTime())
            ->size(4096)
            ->path('/storage/path/to')
            ->build()))
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

