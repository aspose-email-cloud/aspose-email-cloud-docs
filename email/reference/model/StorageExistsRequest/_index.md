---
title: "StorageExistsRequest"
type: docs
url: /reference-model-storage-exists-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.Storage.Exists](/email/reference-storage-api/#exists) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**storageName** |**string**|Storage name |

## Example

{{< tabs tabTotal="6" tabID="storage_exists_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new StorageExistsRequest
{ 
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
StorageExistsRequest request = Models.storageExistsRequest()
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.StorageExistsRequest(
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = StorageExistsRequest.new(
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.StorageExistsRequest()
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::StorageExistsRequest()
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}


