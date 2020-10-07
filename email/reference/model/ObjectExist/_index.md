---
title: "ObjectExist"
type: docs
url: /reference-model-object-exist/
weight: 1
---
Object exists

Properties:

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**Exists** | **bool?** | Indicates that the file or folder exists. | 
**IsFolder** | **bool?** | True if it is a folder, false if it is a file. | 


{{< expand-list title="Example" >}}

{{< tabs tabTotal="6" tabID="object_exist_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var objectExist = new ObjectExist
{
    Exists = true
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ObjectExist objectExist = Models.objectExist()
    .exists(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
object_exist = models.ObjectExist(
    exists=True)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
object_exist = ObjectExist.new(
  exists: true)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let objectExist = Models.objectExist()
    .exists(true)
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$objectExist = Models::objectExist()
    ->exists(true)
    ->build();
```

{{< /tab >}}

{{< /tabs >}}
{{< /expand-list >}}

