---
title: "DiscUsage"
type: docs
url: /reference-model-disc-usage/
weight: 1
---
Class for disc space information.

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**UsedSize** | **long?** | Application used disc space. | 
**TotalSize** | **long?** | Total disc space. | 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="disc_usage_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var discUsage = new DiscUsage
{
    UsedSize = 1048576,
    TotalSize = 3145728
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
DiscUsage discUsage = Models.discUsage()
    .usedSize(1048576)
    .totalSize(3145728)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
disc_usage = models.DiscUsage(
    used_size=1048576,
    total_size=3145728)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
disc_usage = DiscUsage.new(
  used_size: 1048576,
  total_size: 3145728)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let discUsage = Models.discUsage()
    .usedSize(1048576)
    .totalSize(3145728)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$discUsage = Models::discUsage()
    ->usedSize(1048576)
    ->totalSize(3145728)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

