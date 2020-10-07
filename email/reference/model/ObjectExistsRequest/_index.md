---
title: "ObjectExistsRequest"
type: docs
url: /reference-model-object-exists-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.Storage.ObjectExists](/email/reference-storage-api/#objectexists) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**path** |**string**|File or folder path e.g. '/file.ext' or '/folder' |
**storageName** |**string**|Storage name |[optional] 
**versionId** |**string**|File version ID |[optional] 

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="object_exists_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ObjectExistsRequest
{ 
    Path = "/storage/path/to/folder/or/file.ext",
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ObjectExistsRequest request = Models.objectExistsRequest()
    .path("/storage/path/to/folder/or/file.ext")
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ObjectExistsRequest(
    path='/storage/path/to/folder/or/file.ext',
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ObjectExistsRequest.new(
    path: '/storage/path/to/folder/or/file.ext',
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ObjectExistsRequest()
    .path('/storage/path/to/folder/or/file.ext')
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ObjectExistsRequest()
    ->path('/storage/path/to/folder/or/file.ext')
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

