---
title: "StorageExist"
type: docs
url: /reference-model-storage-exist/
weight: 1
---
Storage exists

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Exists** | **bool?** | Shows that the storage exists.              | 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="storage_exist_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var storageExist = new StorageExist
{
    Exists = true
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
StorageExist storageExist = Models.storageExist()
    .exists(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
storage_exist = models.StorageExist(
    exists=True)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
storage_exist = StorageExist.new(
  exists: true)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let storageExist = Models.storageExist()
    .exists(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$storageExist = Models::storageExist()
    ->exists(true)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

