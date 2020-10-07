---
title: "GetDiscUsageRequest"
type: docs
url: /reference-model-get-disc-usage-request/
weight: 2
---

Request model for [EmailCloud.CloudStorage.Storage.GetDiscUsage](/email/reference-storage-api/#getdiscusage) method.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**storageName** |**string**|Storage name |[optional] 

{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="get_disc_usage_request_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new GetDiscUsageRequest
{ 
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
GetDiscUsageRequest request = Models.getDiscUsageRequest()
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.GetDiscUsageRequest(
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = GetDiscUsageRequest.new(
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.GetDiscUsageRequest()
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::GetDiscUsageRequest()
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

